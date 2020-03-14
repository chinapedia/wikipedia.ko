> This article is converted from Wikipedia: [:Gadget-removeAccessKeys.js](https://ko.wikipedia.org/wiki/:Gadget-removeAccessKeys.js).


jQuery( document ).ready( function( $ ) {

`if (mw.config.get('skin') == 'vector') {`
` var head = document.getElementById('mw-head');`
` if(head) removeKeys(head.getElementsByTagName('a'));`
` var panel = document.getElementById('mw-panel');`
` if(panel) removeKeys(panel.getElementsByTagName('a'));`
`} else {`
` var columnOne = document.getElementById('column-one');`
` if (!columnOne) columnOne = document.getElementById('mw_portlets');`
` if (!columnOne) return;`
` removeKeys(columnOne.getElementsByTagName('a'));`
` var cactions = document.getElementById('p-cactions');`
` if(cactions) removeKeys(cactions.getElementsByTagName('a'));`
` var personal = document.getElementById('p-personal');`
` if(personal) removeKeys(personal.getElementsByTagName('a'));`
`}`
`removeKeys(document.getElementsByTagName('input'));`
`removeKeys(document.getElementsByTagName('label'));`

} );

function removeKeys(nodeList){

` var el;`
`   for (var i = 0; i < nodeList.length; i++) {`
`       el = nodeList[i];`
`   if (!el.accessKey) continue;`
`   if (!window.removeAccessKeys || removeAccessKeys.indexOf(el.accessKey) >= 0) {`
`     el.accessKey = ''; // el.setAttribute('accessKey', ''); `
`     $(el).updateTooltipAccessKeys();`
`   }`
` }`

}