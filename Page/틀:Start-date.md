> This article is converted from Wikipedia: [틀:Start-date](https://ko.wikipedia.org/wiki/틀:Start-date).


{{\#iferror:<span style="display:none">{{\#time: Y|}}</span>|Not recognized as a date. Years must have 4 digits (use leading zeros for years \< 1000).|{{\#iferror:}|}}|}}}|timezone=}}}

`  |up-date={{#ifeq:"``"|"``}}"| {{#time:Y|{{#expr:``+3000}}}}//{{#if:``}}}|-1 year, |+1 year, }}|{{#iferror:{{#ifexpr:((abs(``))< 1900) and  ({{#time:Y|``}} >1900)  | {{#ifexpr:({{#time:Y|``}}) <2000|{{#expr:{{#time:Y|``}}+1100}}|{{#expr:{{#time:Y|``}}+1000}} }} |{{#expr:{{#time:Y|``}}+3000}}}}|{{#expr:{{#time:Y|``}}+3000}}}} {{#ifeq:{{#time:d H:i:s|`` }}|{{#iferror:{{#ifexpr:``|{{#time:d}}}}|01}} 00:00:00|{{#time:-m|``}}/-m/+1 month, |{{#ifeq:{{#time:H:i:s|``}}|00:00:00|{{#time:-m-d|``}}/-m-d/+1 day, |{{#ifeq:{{#time:i:s|``}}|00:00|{{#time:-m-d H:00|``}}/-m-dTH/+1 hour, |{{#ifeq:{{#time:s|``}}|00|{{#time:-m-d H:i|``}}/-m-dTH:i/+1 minute, |{{#time:-m-d H:i:s|``}}/-m-dTH:i:s/+1 second, }}}}}}}}}}`
`  |BCE=``}}}`
`  |ISO8601=``}}}`
`  |class-extra=`
`  |class=dtstart`
`  |test=`

}}|Did not recognize date. Try slightly modifying the date in the first parameter.}}}}{{\#invoke:check for unknown parameters|check|unknown= |preview=unknown parameter "_VALUE_"|1|2|ISO8601|dt|display|timezone|tz|BCE|BC|class-extra|test}}