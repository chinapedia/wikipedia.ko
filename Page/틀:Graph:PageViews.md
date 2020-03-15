> This article is converted from Wikipedia: [:Graph:PageViews](https://ko.wikipedia.org/wiki/:Graph:PageViews).


{{\#tag:graph| {

` //`
` // ATTENTION: This code is maintained at `<https://www.mediawiki.org/wiki/Template:Graph:PageViews>
` //            Please do not modify it anywhere else, as it may get copied and override your changes.`
` //            Suggestions can be made at `<https://www.mediawiki.org/wiki/Template_talk:Graph:PageViews>
` //            The graph uses PageViews API `<https://wikitech.wikimedia.org/wiki/Analytics/PageviewAPI>
` //`

` "version": 2,`
` "width": ``,`
` "height": ``,`

` // The data for this graph comes from the PageView API.  The request is made for N days back up to now.`
` "data": [`
`   {`
`     "name": "pageviews",`
`     "url": "wikirest://wikimedia.org/api/rest_v1/metrics/pageviews/{{#ifeq: {{#iferror: {{#expr: `` + 1 }} | `` | `` }} | _ | aggregate | per-article }}/`` | {{#iferror: {{#expr: `` + 1 }} | ``}} | ``}} }} | ``}} }} | www.mediawiki.org | mediawiki.org | {{#iferror: {{#expr: `` + 1 }} | {{#iferror: {{#expr: `` + 1 }} | ``}} | ``}} }} | ``}} }} }}}}/``/user/{{#ifeq: {{#iferror: {{#expr: `` + 1 }} | `` | `` }} | _`

|  |  | }} | }} }} }}|PATH}}/daily }}/ | {{\#iferror: {{\#expr:  + 1 }} |  |  }} |  }} days }}|R}}00/|R}}00",

`     "format": {`
`       "type": "json",`
`       "property": "items"`
`     },`

`     // The response is parsed here, converting date strings of form "20160223" into date 2016-02-23`
`     "transform": [`
`       { "type": "formula", "field": "year", "expr": "parseInt(substring(datum.timestamp,0,4))" },`
`       { "type": "formula", "field": "month", "expr": "parseInt(substring(datum.timestamp,4,6))" },`
`       { "type": "formula", "field": "day", "expr": "parseInt(substring(datum.timestamp,6,8))" },`
`       { "type": "formula", "field": "date", "expr": "datetime(datum.year,datum.month-1,datum.day)" }`
`     ]`
`   }`
` ],`

` "scales": [`
`   // The dates are scaled to the "x" axis - the width of the graph`
`   {`
`     "name": "x",`
`     "type": "time",`
`     "range": "width",`
`     "domain": {"data": "pageviews","field": "date"}`
`   },`
`   // The pageviews are scaled to the "y" axis - the height of the graph`
`   // Optional scale parameter can change "linear" to other scales like log`
`   // Optional max parameter can fix the upper bound of the graph`
`   {`
`     "name": "y",`
`     "type": "``",`
`     "range": "height",`
`     "domain": {"data": "pageviews","field": "views"},`
`     "clamp": true,`

{{ \#if:  | "domainMax": , }}

`     "nice": true`
`   }`
` ],`

` // Simple axis with horizontal grid lines`
` "axes": [`
`   {`
`     "type": "x",`
`     "scale": "x",`
`     "ticks": 5,`
`     "properties": {`
`       "ticks": {"stroke": {"value": "#666666"} },`
`       "labels": {"fill": {"value": "#666666"} },`
`       "axis": {"stroke": {"value": "#666666"}, "strokeWidth": {"value": 2} }`
`     }`
`   },`
`   {`
`     "type": "y",`
`     "scale": "y",`
`     "ticks": 5,`
`     "grid": true,`
`     "properties": {`
`       "ticks": {"stroke": {"value": "#666666"} },`
`       "labels": {"fill": {"value": "#666666"} },`
`       "grid": {"stroke": {"value": "#666666"}, "strokeWidth": {"value": 2} },`
`       "axis": {"stroke": {"value": "#666666"}, "strokeWidth": {"value": 2} }`
`     }`
`   }`
` ],`

` // The graph is drawn with two elements a thick line at the top, and a semi-transparent area below`
` "marks": [`
`   {`
`     "type": "line",`
`     "from": {"data": "pageviews"},`
`     "properties": {`
`       "enter": {`
`         "x": {"scale": "x","field": "date"},`
`         "y": {"scale": "y","field": "views"},`
`         "stroke": {"value": "``"},`
`         "strokeWidth": {"value": 3},`
`         "interpolate": {"value": "``"}`
`       }`
`     }`
`   },`
`   {`
`     "type": "area",`
`     "from": {"data": "pageviews"},`
`     "properties": {`
`       "enter": {`
`         "x": {"scale": "x","field": "date"},`
`         "y": {"scale": "y","value": 0},`
`         "y2": {"scale": "y","field": "views"},`
`         "fill": {"value": "``"},`
`         "fillOpacity": {"value": 0.35},`
`         "interpolate": {"value": "``"}`
`       }`
`     }`
`   }`
` ]`

} }}<noinclude></noinclude>