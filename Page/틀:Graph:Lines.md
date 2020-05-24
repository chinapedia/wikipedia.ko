> This article is converted from Wikipedia: [틀:Graph:Lines](https://ko.wikipedia.org/wiki/틀:Graph:Lines).


<includeonly>{{\#tag:{{\#if:|syntaxhighlight|graph}}|</includeonly><noinclude>

``` html
<graph>
```

{{\#tag:syntaxhighlight|</noinclude> {

` //`
` // ATTENTION: This code is maintained at `<https://www.mediawiki.org/wiki/Template:Graph:Lines>
` //            Please do not modify it anywhere else, as it may get copied and override your changes.`
` //            Suggestions can be made at `<https://www.mediawiki.org/wiki/Template_talk:Graph:Lines>
` //`
` // Template translation is in `<https://commons.wikimedia.org/wiki/Data:Original/Template:Graphs.tab>
` //`

` "version": 2,`
` "width": ``,`
` "height": ``,`
` "padding": "strict",`

` "signals": [{"name": "rightwidth", "expr": "width + padding.right"}],`
` "data": [{`
`   "name": "chart",`

{{\#switch:  |tab= "url": "tabular:///", |query= "url": "wikidatasparql:///?query=", }}

`   "format": {"type": "json"`

{{\#ifeq:|tab|

`     , "property": "data"`

}} {{\#ifeq:|time|

`     , "parse": {"``": "date"}`

}}

`   },`
`   "transform": [`
`     // Convert xField parameter into a field "_xfield"`
`     {"type": "formula", "field": "_xfield", "expr":`

{{\#switch:  | year= "datetime(datum., 0, 1)" | "datum." }}

`     },`
`     {"type": "sort", "by": ["_xfield"]},`

{{\#if: | {"type": "fold", "fields": \[\]} }}

`   ]`
` },`

{{\#if:|{{\#ifeq:  | tab |

` {`
`   "name": "labels",`
`   "url": "tabular:///``",`
`   "format": {"type": "json", "property": "fields"}`
` }`

}}}}

` ],`
` "scales": [`
`   {`
`     "name": "x",`
`     "type": {{#switch: `

| year= "time" | "" }},

`     "domain": {"data": "chart", "field": "_xfield"},`
`     "range": "width",`

{{\#if:|"zero": ,}} {{\#if:|"domainMin": ,}} {{\#if:|"domainMax": ,}}

`   },`
`   {`
`     "name": "y",`
`     "type": "linear",`
`     "range": "height",`
`     "domain": {"data": "chart", "field": "``"},`

{{\#if:|"zero": ,}} {{\#if:|"domainMin": ,}} {{\#if:|"domainMax": ,}}

`   },`
`   {`
`     "name": "color",`
`     "type": "ordinal",`
`     "domain": {"data": "chart", "field": "``"},`
`     "range": "category10"`
`   },`

{{\#if:|

`   {`
`     "name": "labels",`
`     "type": "ordinal",`

{{\#ifeq:  | tab | "domain": {"data": "labels", "field": "name"},

`     "range": {"data": "labels", "field": "title"},`

| "domain": \[\],

`     "range": [``],`

}}

`   }`

}}

` ],`

{{\#if:|

` "legends": [{`
`   "fill": "color",`
`   "stroke": "color",`

{{\#ifeq: |-|| "title": "", }} {{\#if: | "properties": { "labels": { "text": {"scale": "labels", "field": "data"} } } }}

` }],`

}}

` "axes": [`
`   {"scale": "x", "type": "x", "tickSizeEnd": 0`

{{\#ifeq:|-||, "ticks": }} {{\#if:|, "title": ""}} {{\#if:|, "grid": true}} },

`   {"scale": "y", "type": "y", "tickSizeEnd": 0`

{{\#ifeq:|-||, "ticks": }} {{\#if:|, "title": ""}} {{\#if:|, "grid": true}} }

` ],`

` "marks": [`
`   // Group data by the group parameter or "key", and draw lines, one line per group`
`   {`
`     "type": "group",`
`     "from": {`
`       "data": "chart",`
`       "transform": [{"type": "facet", "groupby": ["``"]}]`
`     },`
`     "marks": [`
`       {`
`         "type": "line",`
`         "properties": {`
`           "enter": {`
`             "y": {"scale": "y", "field": "``"},`
`             "x": {"scale": "x", "field": "_xfield"},`
`             "stroke": {"scale": "color", "field": "``"},`
`             "interpolate": {"value": "monotone"},`
`             "strokeWidth": {"value": 2.5}`
`           }`
`         }`
`       }`
`     ],`
`   }`

{{\#if:|

`   // Draw title at the top of the graph`

, {

`     "type": "text",`
`     "properties": {`
`       "enter": {`
`         "x": {"signal": "rightwidth", "mult": 0.5},`
`         "y": {"value": -15},`
`         "text": {"value": "``"},`
`         "fontWeight": {"value": "bold"},`
`         "align": {"value": "center"},`
`         "baseline": {"value": "bottom"},`
`         "fill": {"value": "#000"}`
`       }`
`     }`
`   }`

}}

` ]`

} <includeonly>}} <small>{{\#switch:  |tab= {{\#invoke:TNT|msg|I18n/Template:Graphs.tab|source_table|{{\#invoke:TNT|link|}}}}. |query= {{\#invoke:TNT|msg|I18n/Template:Graphs.tab|source_wdqs|<https://query.wikidata.org/#>}}. }}</small> </includeonly><noinclude>|lang=javascript}}

``` html
</graph>
```

</noinclude>