> This article is converted from Wikipedia: [틀:Graph:Street map with marks](https://ko.wikipedia.org/wiki/틀:Graph:Street_map_with_marks).


<includeonly>{{\#tag:{{\#if:|syntaxhighlight|graph}}|</includeonly><noinclude>

``` html
<graph>
```

{{\#tag:syntaxhighlight|</noinclude> {

` //`
` // ATTENTION: This code is maintained at `<https://www.mediawiki.org/wiki/Template:Graph:Street_map_with_marks>
` //            Please do not modify it anywhere else, as it may get copied and override your changes.`
` //            Suggestions can be made at `<https://www.mediawiki.org/wiki/Template_talk:Graph:Street_map_with_marks>
` //`
` // Template translation is in `<https://commons.wikimedia.org/wiki/Data:Original/Template:Graphs.tab>
` //`
` "version": 2, "width":``, "height": ``}}}, "padding": ``,`
` "signals":[`
`   // These signals allow us to quickly move the map within the image, e.g. to leave space for the legend`

{{\#if:|

`   {"name":"legendWidth", "init": {"expr": "``"} },`

|

`   {"name":"legendWidth", "init": {"expr": "0"} },`

}}

`   {"name":"legendHeight", "init": {"expr": "height"} },`
`   {"name":"imgWidth", "init": {"expr": "width-legendWidth"} },`
`   {"name":"imgHeight", "init": {"expr": "height"} },`
`   {"name":"imgXC", "init": {"expr": "imgWidth/2"} },`
`   {"name":"imgYC", "init": {"expr": "imgHeight/2"} },`
`   {"name":"imgTileSize", "init": {"expr": "256"} },`
`   {"name":"imgLat", "init": {"expr": "``"} },`
`   {"name":"imgLon", "init": {"expr": "``"} },`
`   {"name":"imgZoom", "init": {"expr": "``"} },`
`   {"name":"picWidth", "init": {"expr": "180"} },`
`   {"name":"picHeight", "init": {"expr": "picWidth/2"} },`
`   {"name":"picXC", "init": {"expr": "imgWidth-(picWidth/2)"} },`
`   {"name":"picYC", "init": {"expr": "imgHeight-(picHeight/2)"} },`
`   {"name":"showMiniMap", "init": {"expr": "``"} },`
` ],`
` "data": [`
`   {`
`     "name": "data",`

{{\#if:|

`     // If query parameter is given, use it to get data from Wikidata Query service`
`     // Assume that it contains "coord" field with the geo coordinates`
`     "url": "wikidatasparql:///?query=``",`
`     "format": {"type": "json"},`

|{{\#if:|

`     // Use tabular data source`
`     "url": "tabular:///``",`
`     "format": {"type": "json", "property": "data"},`

| // Otherwise use the first unnamed argument for source values

`     "values": [ `
`     ],`

}}}}

`     "transform": [`

{{\#if: |

`       // If query is given, translate geo coordinate [longitude, latitude] array into two values`
`       { "type": "formula", "field":"lon", "expr": "datum.coord[0]" },`
`       { "type": "formula", "field":"lat", "expr": "datum.coord[1]" },`

}}

`       {`
`         "type": "geo",`
`         "projection": "mercator",`
`         "scale": {"expr": "imgTileSize/PI/2*pow(2,imgZoom)"},`
`         "translate": [{"expr": "imgXC"}, {"expr": "imgYC"}],`
`         "center": [{"expr": "imgLon"}, {"expr": "imgLat"}],`
`         "lon": "lon", "lat": "lat"`
`       },`
`       { "type": "formula", "field":"layout_x", "expr": "datum.layout_x + (datum.offsetX {{!}}{{!}} 0)" },`
`       { "type": "formula", "field":"layout_y", "expr": "datum.layout_y + (datum.offsetY {{!}}{{!}} 0)" },`
`       { "type": "formula", "field":"color", "expr": "datum.color {{!}}{{!}} '#c33'" },`
`       { "type": "formula", "field":"textColor", "expr": "datum.textColor {{!}}{{!}} datum.color" },`
`       { "type": "formula", "field":"strokeColor", "expr": "datum.strokeColor {{!}}{{!}} '#ffe7e6'" }`
`     ]`
`   },`
`   {`
`     // Hack: single value data source for drawing/hiding images and other non-series elements`
`     "name": "dummyData",`
`     "values": [{}]`
`   }`
` ],`

{{\#if:|

` "scales": [`
`   {`
`     "name": "sColor",`
`     "type": "ordinal",`
`     "range": "category10",`
`     "domain": {"data": "data", "field": "``"}`
`   },`
` ],`

}} // Legend only works if showLegend and colorScaleField are set {{\#if:|

` "legends": [`
`   {`
`     "title": "Legend",`
`     "fill": "sColor",`
`     "properties": {`
`      "legend": {`
`        "x": {"value": {{#expr: `` - `` }} },`
`        "width": {"value": `` },`
`        "stroke": {"value": "#ddd"},`
`        "fill": {"value": "#fff"},`
`        "strokeWidth": {"value": 2}`
`      }`
`     }`
`   }`
` ],`

}}

` "marks": [`
`   {`
`     "type": "image",`
`     "from": {`
`       "data": "dummyData",`
`       "transform": [`
`         { "type": "formula", "field":"url", "expr": "'mapsnapshot:///?width='+imgWidth+'&height='+imgHeight+'&zoom='+imgZoom+'&lat='+imgLat+'&lon='+imgLon{{#if:``|+'&style=``'}}" }`
`       ]`
`     },`
`     "properties": {`
`       "enter": {`
`         "url": {"field": "url"},`
`         "xc": {"signal": "imgXC"}, "yc": {"signal": "imgYC"},`
`         "width": {"signal": "imgWidth"}, "height": {"signal": "imgHeight"}`
`       }`
`     }`
`   },`
`   {`
`     // Places an image of a given name and size at the [lan,lon] location`
`     "type": "image",`
`     "from": {`
`       "data": "data",`
`       "transform": [`
`         { "type": "filter", "test": "datum.img" },`
`         { "type": "formula", "field":"iconWidth", "expr": "datum.width {{!}}{{!}} 0" },`
`         { "type": "formula", "field":"iconHeight", "expr": "datum.height {{!}}{{!}} 0" },`
`         { "type": "formula", "field":"img",`
`           "expr": "if(!test(/^[a-z]+:\\/\\//, datum.img), 'wikifile:///'+datum.img, datum.img)" },`
`         // Ensure that either width or height parameter is passed to wikifile:// request`
`         { "type": "formula", "field":"img",`
`           "expr": "if((datum.iconWidth {{!}}{{!}} datum.iconHeight) && !test(/[?&](width{{!}}height)=\\d/, datum.img),if(datum.iconWidth,datum.img+'?width='+datum.iconWidth,datum.img+'?height='+datum.iconHeight), datum.img)" },`
`     ]},`
`     "properties": {`
`       "enter": {`
`         "url": {"field": "img"},`
`         "xc": {"field": "layout_x"}, "yc": {"field": "layout_y"},`
`         "width": {"field": "iconWidth"}, "height": {"field": "iconHeight"}`
`       }`
`     }`
`   },`
`   {`
`     // Draw marks of a given color, shape, and size at the [lan,lon] location`
`     "type": "symbol",`
`     "from": {`
`       "data": "data",`
`       "transform": [{ "type": "filter", "test": "!datum.img" }]`
`     },`
`     "properties": {`
`       "enter": {`
`         "x": {"field": "layout_x"},`
`         "y": {"field": "layout_y"},`
`         // If colorScaleField is set, use color scaling, otherwise use the preset color value`
`         "fill": { {{#if:``| "field": "type", "scale": "sColor" | "field": "color" }} },`
`         "size": {"field": "size"},`
`         "shape": {"field": "shape"},`
`         "stroke": {"field": "strokeColor"}`
`       }`
`     }`
`   },`
`   {`
`     // Draw text with the given color and size at the [lan,lon] location`
`     // See `<https://github.com/vega/vega/wiki/Marks#text>` for all parameter description (prepend "text" and capitalize them)`
`     "type": "text",`
`     "from": {`
`       "data": "data",`
`       "transform": [`
`         { "type": "filter", "test": "datum.text" },`
`         // Figure out if this is an LTR or RTL page. For LTR, show label to the right of the icon, left-aligned. For RTL, reverse.`
`         { "type": "formula", "field":"isLTR", "expr": "'``' == '\\u200E'" },`
`         // If these values are not defined ("undefined" is not allowed, so test for truthiness and not 0)`
`         { "type": "formula", "field":"textDx", "expr": "if(!datum.textDx && datum.textDx != 0, if(datum.isLTR,8,-8), datum.textDx)" },`
`         { "type": "formula", "field":"textAlign", "expr": "if(!datum.textAlign, if(datum.isLTR,'left','right'), datum.textAlign)" },`
`         { "type": "formula", "field":"textBaseline", "expr": "datum.textBaseline {{!}}{{!}} 'middle'" }`
`     ]},`
`     "properties": {`
`       "enter": {`
`         "text": {"field": "text"},`
`         "x": {"field": "layout_x" },`
`         "y": {"field": "layout_y"},`
`         "dx": {"field": "textDx" },`
`         "dy": {"field": "textDy"},`
`         "fill": {"field": "textColor"},`
`         "align": {"field": "textAlign"},`
`         "baseline": {"field": "textBaseline"},`
`         "radius": {"field": "textRadius"},`
`         "theta": {"field": "textTheta"},`
`         "angle": {"field": "textAngle"},`
`         "font": {"field": "textFont"},`
`         "fontSize": {"field": "textFontSize"},`
`         "fontWeight": {"field": "textFontWeight"},`
`         "fontStyle": {"field": "textFontStyle"}`
`       }`
`     }`
`   },`
`   {`
`     // Draw a low-zoom locator map frame`
`     "type": "rect",`
`     "from": {`
`       "data": "dummyData",`
`       "transform": [`
`         { "type": "filter", "test": "showMiniMap" }`
`       ]`
`     },`
`     "properties": {`
`       "enter": {`
`         "xc": {"signal": "picXC"}, "yc": {"signal": "picYC"},`
`         "width": {"signal": "picWidth", "offset":2}, "height": {"signal": "picHeight"},`
`         "stroke": {"value":"#fff"},"strokeWidth": {"value":6},`
`       }`
`     }`
`   },`
`   {`
`     // Draw a low-zoom locator map by using a premade world map image`
`     "type": "image",`
`     "from": {`
`       "data": "dummyData",`
`       "transform": [`
`         { "type": "filter", "test": "showMiniMap" },`
`         { "type": "formula", "field":"url", "expr": "1" }`
`       ]`
`     },`
`     "properties": {`
`       "enter": {`
`         "url": {"value": "wikirawupload:``"},`
`         "xc": {"signal": "picXC"}, "yc": {"signal": "picYC"},`
`         "width": {"signal": "picWidth"}, "height": {"signal": "picHeight"}`
`       }`
`     }`
`   },`
`   {`
`     // Draw a zoom-out mark at the [lan,lon] location`
`     "type": "symbol",`
`     "from": {`
`       "data": "dummyData",`
`       "transform": [`
`         { "type": "filter", "test": "showMiniMap" },`
`         { "type": "formula", "field":"lat", "expr": "imgLat" },`
`         { "type": "formula", "field":"lon", "expr": "imgLon" },`
`         {`
`           "type": "geo",`
`           "projection": "equirectangular",`
`           "scale": {"expr": "180/2/PI"},`
`           "translate": [{"expr": "picXC"}, {"expr": "picYC"}],`
`           "center": [{"expr": "0"}, {"expr": "0"}],`
`           "lon": "lon", "lat": "lat"`
`         }`
`       ]`
`     },`
`     "properties": {`
`       "enter": {`
`         "x": {"field": "layout_x"}, "y": {"field": "layout_y"},`
`         "fill": {"value": "#c33"},`
`         "stroke": {"value": "#ffe7e6"},`
`         "size": {"value": 40}`
`       }`
`     }`
`   }`
` ]`

} <includeonly>}} {{\#if:| <small>{{\#invoke:TNT|msg|Original/Template:Graphs.tab|source-wdqs|<https://query.wikidata.org/#>}}.</small> |{{\#if:| <small>{{\#invoke:TNT|msg|Original/Template:Graphs.tab|source-table|{{\#invoke:TNT|link|}}}}.</small> }}}}</includeonly><noinclude>|lang=javascript}}

``` html
</graph>
```

</noinclude>