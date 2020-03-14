> This article is converted from Wikipedia: [:Gadget-quickeditcounter.js](https://ko.wikipedia.org/wiki/:Gadget-quickeditcounter.js).


// Warning\! This gadget also use other projects. // Original version: // - QuickEditCounter script by [:pl:User:ChP94](https://ko.wikipedia.org/wiki/:pl:User:ChP94 "wikilink") // - Released under the [GNU Public License (GPL)](http://www.gnu.org/licenses/gpl.txt) // Modified by: [:pl:User:Beau](https://ko.wikipedia.org/wiki/:pl:User:Beau "wikilink"), [:pl:User:Rzuwig](https://ko.wikipedia.org/wiki/:pl:User:Rzuwig "wikilink")

window.qecGadget = {

`   version: 9,`

`   init: function() {`
`       if ( mw.config.get( 'wgNamespaceNumber' ) != 2 && mw.config.get( 'wgNamespaceNumber' ) != 3 ) {`
`           return;`
`       }`

`       if ( mw.util.getParamValue('printable') == 'yes' ) {`
`           return;`
`       }`

`       this.username = mw.config.get( 'wgTitle' ).replace(/\/.*$/, '');`

`       var that = this;`

`       var request = {`
`           action: 'query',`
`           list:   'users',`
`           usprop: 'editcount|gender',`
`           format: 'json',`
`           ususers:    this.username,`
`           requestid:  new Date().getTime()`
`       };`

`       jQuery.getJSON( mw.util.wikiScript( 'api' ), request, function(result) {`
`           jQuery(document).ready(function() {`
`               if (result) {`
`                   that.showResults(result);`
`               }`
`           });`
`       });`
`   },`
`   showResults: function(data) {`
`       data = data.query.users[0];`
`       if (!data || data.name != this.username || data.invalid != null || data.editcount === undefined)`
`           return;`

`       var firstHeading;`
`       var headers = document.getElementsByTagName( 'h1' );`

`       for ( var i = 0; i < headers.length; i++ ) {`
`           var header = headers[i];`
`           if(header.className == "firstHeading" || header.id == "firstHeading" || header.className == "pagetitle") {`
`               firstHeading = header; break;`
`           }`
`       }`

`       if( !firstHeading ) {`
`           firstHeading = document.getElementById("section-0");`
`       }`

`       if( !firstHeading ) {`
`           return;`
`       }`

`       var html = '이 사용자는';`
`       var lang = 'ko';`
`       var wiki = 'wikipedia';`

`       var m;`
`       if (m = mw.config.get( 'wgServer' ).match(/^(?:http:)?\/\/(.+?).([^.]+).org$/)) {`
`           lang = m[1];`
`           wiki = m[2];`
`       }`
`       else if (m = mw.config.get( 'wgScriptPath' ).match(/\/(.+?)\/(.+?)\//)) {`
`           lang = m[2];`
`           wiki = m[1];`
`       }`
`       html += ' 총 `<a href="//tools.wmflabs.org/xtools-ec/index.php?name=' + encodeURIComponent(this.username) + '&wiki=' + encodeURIComponent(wiki) + '&lang=' + encodeURIComponent(lang) + '">`' + data.editcount + '`</a>`회 편집했습니다.';`

`       var div = document.createElement("div");`
`       div.style.cssText = "font-size:0.5em; line-height:1em; margin-bottom:5px;";`
`       div.className = 'plainlinks';`
`       div.innerHTML = html;`

`       if ( mw.config.get( 'skin' ) == 'modern' ) {`
`           div.style.marginLeft = "10px";`
`           div.style.display = "inline-block";`
`       }`

`       firstHeading.appendChild(div);`
`   }`

};

qecGadget.init();