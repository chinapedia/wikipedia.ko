> This article is converted from Wikipedia: [틀:Collapsible option](https://ko.wikipedia.org/wiki/틀:Collapsible_option).


**이 틀의 가시성 관리법**
이 틀이 처음 나타날 때의 가시성을 관리하려면, [매개변수를 추가하세요](https://ko.wikipedia.org/wiki/위키백과:틀#매개변수 "wikilink").

  -

    로 설정하면 기본적으로 접힌 상태로 표시됩니다. `{{`<includeonly>`{{`</includeonly>`BASEPAGENAME`<includeonly>`}}`</includeonly>`  |state=collapsed}} `

    로 설정하면 기본적으로 펼친 상태로 표시됩니다. `{{`<includeonly>`{{`</includeonly>`BASEPAGENAME`<includeonly>`}}`</includeonly>`  |state=expanded}} `

    로 설정하면 기본적으로 펼친 상태로 표시지만, 여러개인 경우 접힌 상태로 표시됩니다. `{{`<includeonly>`{{`</includeonly>`BASEPAGENAME`<includeonly>`}}`</includeonly>`  |state=autocollapse}} `

매개변수()를 생략한 경우 `{{#switch:``|collapsed=collapsed|expanded=expanded|autocollapse|#default=autocollapse}}`가 기본값입니다. {{\#if:|

  -

    is also available; where *value* can be either `right` or `left`. The default is `center`

}}{{\#if:|: is also available; where *value* can be either `navbox` or a `color`. The default is `none` and `navbox` defaults to the default navbox color. }}{{\#if:|

  -

    is also available; where *value* can be either `N [em/%/px]` or `auto`. The default is `100%`

}}

`  }} }}`<noinclude>

</noinclude>