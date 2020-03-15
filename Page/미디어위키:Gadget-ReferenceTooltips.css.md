> This article is converted from Wikipedia: [:Gadget-ReferenceTooltips.css](https://ko.wikipedia.org/wiki/:Gadget-ReferenceTooltips.css).


/\* Copied from [en:MediaWiki:Gadget-ReferenceTooltips.css](https://ko.wikipedia.org/wiki/en:MediaWiki:Gadget-ReferenceTooltips.css "wikilink") \*/ /\* See [mw:Reference Tooltips](https://ko.wikipedia.org/wiki/mw:Reference_Tooltips "wikilink") \*/

.referencetooltip {

`       position: absolute;`
`       list-style: none;`
`       list-style-image: none;`
`       opacity: 0;`
`       font-size: 12px;`
`       margin: 0;`
`       z-index: 5;`
`       padding: 0;`

} .referencetooltip li {

`       border: #080086 2px solid;`
`       max-width: 260px;`
`       padding: 10px 8px 13px 8px;`
`       margin: 0px;`
`       background-color: #F7F7F7;`
`       -webkit-box-shadow: 2px 4px 2px rgba(0,0,0,0.3);`
`       -moz-box-shadow: 2px 4px 2px rgba(0,0,0,0.3);`
`       box-shadow: 2px 4px 2px rgba(0,0,0,0.3);`

} .referencetooltip li+li {

`       margin-left: 7px;`
`       margin-top: -2px;`
`       border: 0;`
`       padding: 0;`
`       height: 3px;`
`       width: 0px;`
`       background-color: transparent;`
`       -webkit-box-shadow: none;`
`       -moz-box-shadow: none;`
`       box-shadow: none;`
`       border-top: 12px #080086 solid;`
`       border-right: 7px transparent solid;`
`       border-left: 7px transparent solid;`

} .referencetooltip\>li+li::after {

`       content: '';`
`       border-top: 8px #F7F7F7 solid;`
`       border-right: 5px transparent solid;`
`       border-left: 5px transparent solid;`
`       margin-top: -12px;`
`       margin-left: -5px;`
`       z-index: 1;`
`       height: 0px;`
`       width: 0px;`
`       display: block;`

} .client-js body .referencetooltip li li {

`       border: none;`
`       -webkit-box-shadow: none;`
`       -moz-box-shadow: none;`
`       box-shadow: none;`
`       height: auto;`
`       width: auto;`
`       margin: auto;`
`       padding: 0;`
`       position: static;`

} .RTflipped {

`       padding-top: 13px;`

} .referencetooltip.RTflipped li+li {

`       position: absolute;`
`       top: 2px;`
`       border-top: 0;`
`       border-bottom: 12px #080086 solid;`

} .referencetooltip.RTflipped li+li::after {

`       border-top: 0;`
`       border-bottom: 8px #F7F7F7 solid;`
`       position: absolute;`
`       margin-top: 7px;`

} .RTsettings {

`       float: right;`
`       height: 24px;`
`       width: 24px;`
`       cursor: pointer;`
`       background-image: url(//upload.wikimedia.org/wikipedia/commons/thumb/0/05/OOjs_UI_icon_advanced.svg/24px-OOjs_UI_icon_advanced.svg.png);`
`       background-image: linear-gradient(transparent, transparent), url(//upload.wikimedia.org/wikipedia/commons/0/05/OOjs_UI_icon_advanced.svg);`
`       margin-top: -9px;`
`       margin-right: -7px;`
`       -webkit-transition: opacity 0.15s;`
`       -moz-transition: opacity 0.15s;`
`       -ms-transition: opacity 0.15s;`
`       -o-transition: opacity 0.15s;`
`       transition: opacity 0.15s;`
`       opacity: 0.6;`
`       filter: alpha(opacity=60);`

} .RTsettings:hover {

`       opacity: 1;`
`       filter: alpha(opacity=100);`

} .RTTarget {

`       border: #080086 2px solid;`

}