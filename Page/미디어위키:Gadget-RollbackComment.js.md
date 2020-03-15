> This article is converted from Wikipedia: [:Gadget-RollbackComment.js](https://ko.wikipedia.org/wiki/:Gadget-RollbackComment.js).


/\*

  - 롤배커들을 위한 Gadget Script
      - by [사용자:\*devunt](https://ko.wikipedia.org/wiki/사용자:*devunt "wikilink"), from [사용자:\*devunt/rollback.js](https://ko.wikipedia.org/wiki/사용자:*devunt/rollback.js "wikilink")

<!-- end list -->

  - /

function addExtRbLink($container) {

`   var $rbnode = $([]), index = {};`
`   var wgCanonicalSpecialPageName = mw.config.get('wgCanonicalSpecialPageName');`
`   var wgAction = mw.config.get('wgAction');`
`   if (typeof rollbackLinksDisable == 'object' && rollbackLinksDisable instanceof Array)`
`       for (var i = 0; i < rollbackLinksDisable.length; i++)`
`           index[rollbackLinksDisable[i]] = true;`
`   if (`
`       !('user' in index) && wgCanonicalSpecialPageName == "Contributions" ||`
`       !('recent' in index) && wgCanonicalSpecialPageName == "Recentchanges" ||`
`       !('watchlist' in index) && wgCanonicalSpecialPageName == "Watchlist" ||`
`       !('history' in index) && wgAction == "history" ||`
`       !('diff' in index) && (diffnode = document.getElementById("mw-diff-ntitle2"))`
`   ) {`
`       $rbnode = $container.find( 'span.mw-rollback-link' );`
`   }`
`   $rbnode.each( function () { addExtendedRollbackLink( this ); } );`

}

function confirmRollback() {

`   var url = this.href;`
`   var user = url.match(/[?&]from=([^&]*)/);`
`   if (!user) return;`
`   user = decodeURIComponent(user[1].replace(/\+/g, " "));`
`   var summary = prompt("추가할 편집 요약을 입력하세요.\n\n$user 는 편집이 되돌려질 사용자 이름으로 치환됩니다.",`
`                        rollbackSummaryDefault);`
`   if (summary === null)`
`       return false;`
`   else if (summary === "")`
`       return true;`
`   this.href += "&summary=" + '`[`$2`](https://ko.wikipedia.org/wiki/특수:기여/$2 "wikilink")`(`[`토론`](https://ko.wikipedia.org/wiki/User_talk:$2 "wikilink")`)의 편집을 전부 되돌림: '.replace(/\$2/g, user) + encodeURIComponent(summary.replace(/\$user/g, user));`
`   return true;`

}

function rollbackAsBot() {

`   this.href += "&bot=1";`
`   return true;`

}

function addExtendedRollbackLink(rbnode) {

`   var rblink = rbnode.getElementsByTagName("a")[0];`
`   var alink = rblink.cloneNode(true);`
`   alink.className = "";`
`   alink.firstChild.nodeValue = "(+편집 요약)";`
`   alink.onclick = confirmRollback;`
`   rbnode.insertBefore(alink, rblink.nextSibling);`
`   rbnode.insertBefore(document.createTextNode(" | "), alink);`
`   if (userIsInGroup('sysop'))`
`   {`
`       var blink = rblink.cloneNode(true);`
`       blink.className = "";`
`       blink.firstChild.nodeValue = "(+봇)";`
`       blink.onclick = rollbackAsBot;`
`       rbnode.insertBefore(blink, alink.nextSibling);`
`       rbnode.insertBefore(document.createTextNode(" | "), blink);`
`   }`

} if (typeof rollbackLinksDisable == 'undefined')

`   rollbackLinksDisable = [];`

if (typeof rollbackSummaryDefault == 'undefined')

`   rollbackSummaryDefault = "";`

mw.hook( 'wikipage.content' ).add(addExtRbLink);

function userIsInGroup (group) {

` var wgUserGroups = mw.config.get('wgUserGroups');`
` if (wgUserGroups) {`
`   if (!group || group.length === 0) group = '*';`
`   return wgUserGroups.join (' ').indexOf (group) >= 0;`
` }`
` return false;`

}