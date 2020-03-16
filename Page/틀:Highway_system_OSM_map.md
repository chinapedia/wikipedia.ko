> This article is converted from Wikipedia: [:Highway system OSM map](https://ko.wikipedia.org/wiki/:Highway_system_OSM_map).


<includeonly>

` },`
` "query": "`

SELECT ?id ?length

` (if(?id = wd:``, '#C12838', '#07c63e') as ?stroke)`
` (concat('총연장 ', str(?length), ' km') as ?description)`
` (if(BOUND(?link),`
`     concat('`[`',``   ``substr(str(?link),31,500),``   ``'{{!}}',``   ``?idLabel,``   ``'`](https://ko.wikipedia.org/wiki/',_substr\(str\(?link\),31,500\),_'{{!}}',_?idLabel,_' "wikilink")`'),`
`     ?idLabel)`
`  as ?title)`

WHERE {

` {?id wdt:P16 wd:{{#if:``|``|``}}.}`
` {{#if:``| OPTIONAL { ?id wdt:P2043 ?length. } }}`
` SERVICE wikibase:label {`
`   bd:serviceParam wikibase:language 'ko' .`
`   ?id rdfs:label ?idLabel .`
` }`
` OPTIONAL {?link schema:about ?id.`
` ?link schema:isPartOf <`<https://ko.wikipedia.org/>`>.}`

} GROUP BY ?id ?link ?idLabel ?length

"}|plain=|zoom=|type=|id=|stroke-color=|stroke-width=|frame-lat=|frame-long=|frame-width=|frame-height=|text=|frame-align= }}</includeonly><noinclude> </noinclude>