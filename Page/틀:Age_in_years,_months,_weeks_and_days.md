> This article is converted from Wikipedia: [틀:Age in years, months, weeks and days](https://ko.wikipedia.org/wiki/틀:Age_in_years,_months,_weeks_and_days).


} -  }}} }}} - {{\#ifexpr:  }}} \>  }}} }}}

` |0`
` |{{#ifexpr: `` }}} < `` }}} }}}`
`  |1`
`  |{{#ifexpr: `` }}} >= `` }}} }}}`
`   |0`
`   |1`
`  }}`
` }}`
`}}}}`
`|months={{#expr: `` }}} - `` }}} }}} + {{#ifexpr: `` }}} >= `` }}} }}}`
` |{{#ifexpr: `` }}} >= `` }}} }}}`
`  |0`
`  |12`
` }}`
` |{{#ifexpr: `` }}} > `` }}} }}}`
`  |-1`
`  |11`
` }}`
`}}}}`
`|weeks={{#ifexpr: (`` }}} < `` }}} }}})`
`  |``} }}}`
`    |month1 = {{#expr:((`` }}} + 10) mod 12) + 1}}`
`    |year1  = {{#expr:`` }}} - (`` }}} = 1)}}`
`    |day2   = `` }}} `
`    |month2 = `` }}}`
`    |year2  = `` }}} `
`    }}`
`  |``} }}}`
`    |month1 = `` }}}`
`    |year1  = `` }}}`
`    |day2   = `` }}} `
`    |month2 = `` }}}`
`    |year2  = `` }}} `
`}}}}`
`|days={{#expr: (`` }}} - `` }}} }}} + {{#ifexpr: `` }}} >= `` }}} }}}`
` |0`
` |{{#switch: `` }}}`
`  |5|7|10|12 = 30`
`  |1|2|4|6|8|9|11 = 31`
`  |3={{#ifexpr: `` }}} mod 4 = 0`
`   |{{#ifexpr: (`` }}} mod 100 = 0) and  (`` }}} mod 400 != 0) `
`    |28`
`    |29`
`    }}`
`   |28`
`  }}`
` }}`
`}}) mod 7}}`

|type= }}<noinclude> [분류:날짜 계산용 틀](https://ko.wikipedia.org/wiki/분류:날짜_계산용_틀 "wikilink") </noinclude>