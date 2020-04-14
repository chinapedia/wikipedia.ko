> This article is converted from Wikipedia: [미디어위키:Group-sysop.js](https://ko.wikipedia.org/wiki/미디어위키:Group-sysop.js).


/\* 관리자일 경우만 실행되는 스크립트입니다. [위키백과:위키프로젝트 시스템](https://ko.wikipedia.org/wiki/위키백과:위키프로젝트_시스템 "wikilink") 참고

  - /

// '위키백과:\#\#\# 요청' 문서 목차에  혹은 된 요청들 취소선 긋기 // by klutzy: //ko.wikipedia.org/w/index.php?title=%EC%82%AC%EC%9A%A9%EC%9E%90:Klutzy/common.js\&oldid=6414855 // 파이어폭스 3.5 이상에서 동작합니다. 다른 브라우저의 경우도 최신 브라우저에서만 동작할 가능성이 높습니다.

// by Ykhwong: 크롬, 파이어폭스 등에서 동작 문제가 발생하여 소스 전면 수정합니다. (2017-12-18)

mw.hook('wikipage.content').add(function() {

`   var arr_ids = [];`
`   var toc;`

`   if (mw.config.get('wgNamespaceNumber') !== 4 || mw.config.get('wgAction') !== "view") return;`
`   if (mw.config.get('wgTitle').indexOf('요청') < 0 && mw.config.get('wgTitle').indexOf('신청') < 0) return;`
`   toc = document.getElementById("toc");`
`   if(!toc) return;`
`   toc = toc.getElementsByTagName("ul")[0];`
`   if(!toc) return;`

`   $( '#toc li.toclevel-1' ).each( function ( i, li ) {`
`       var cnt=0;`
`       var checked = false;`
`       var hrefNode, sibl;`
`       var txt = '#' + $.escapeSelector($( li ).find( 'span.toctext' ).text().replace(/ +/g, "_"));`
`       arr_ids.forEach(function (item) {`
`           if (item == txt) {`
`               cnt++;`
`           }`
`       });`
`       arr_ids.push(txt);`
`       if (cnt !== 0) {`
`           cnt++;`
`           txt = txt + "_" + cnt;`
`       }`
`       sibl = $(txt).parent().next();`
`       if (sibl.html() === undefined) { return; }`
`       while (true) {`
`           var filename = sibl.find('img').attr("alt");`
`           if (filename == "Yes check.svg" || filename == "X mark.svg" || filename == "Yellow check.svg" || filename == "U2713.svg") {`
`               checked = true;`
`               break;`
`           }`
`           sibl = sibl.next();`
`           if (sibl.html() === undefined) { break; }`
`           if (sibl[0].nodeName.toLowerCase() == "h2") { break; }`
`       }`
`       if (!checked) { return; }`

`       hrefNode = toc.getElementsByClassName("toclevel-1")[i].getElementsByTagName("a")[0];`
`       hrefNode.innerHTML = "`~~`"+hrefNode.innerHTML+"`~~`";`
`   });`

});