> This article is converted from Wikipedia: [:Gadget-siteNotice.js](https://ko.wikipedia.org/wiki/:Gadget-siteNotice.js).


/\*

  - siteNotice
  - The contents of Mediawiki:Sitenotice are always exposed to search engines.
  - This gadget fixes the problem.
  - @author ykhwong
  - Reference: <https://gerrit.wikimedia.org/r/plugins/gitiles/mediawiki/extensions/DismissableSiteNotice/+/master/modules/ext.dismissableSiteNotice.js>
  - /

$(function () {

var cookieName = 'dismissNewSiteNotice'; var dismissStrLang = {

`   en: "Dismiss",`
`   ko: "숨기기"`

}; var dismissStr = dismissStrLang.ko; var noticeGrpPage = '%EC%9C%84%ED%82%A4%EB%B0%B1%EA%B3%BC:%EC%86%8C%EB%8F%84%EA%B5%AC/noticeGrp'; // [ko:Wikipedia:소도구/noticeGrp](https://ko.wikipedia.org/wiki/ko:Wikipedia:소도구/noticeGrp "wikilink")

function html2text(html) {

`   var tag = document.createElement('div');`
`   tag.innerHTML = html;`

`   return tag.innerText;`

}

function getDivHtml(html, target) {

`   var tag = document.createElement('div');`
`   tag.innerHTML = html;`

`   return $(tag).find(target).html();`

}

function getDivText(html, target) {

`   var tag = document.createElement('div');`
`   tag.innerHTML = html;`

`   return $(tag).find(target).text().trim();`

}

function procDismiss(sitenoticeId) {

`   $("#siteNoticeLocal").prepend('`

<div class="mw-dismissable-notice-close2">

' +

`       '`<a tabindex="0" role="button"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/X-schliessen.svg/16px-X-schliessen.svg.png" title="' + dismissStr + '">`' +`
`       '`</a>

</div>

');

`   if (/^ko\.m\.wikipedia\.org/.test(window.location.host)) {`
`       $("#siteNoticeLocal").css(`
`           { 'position': 'relative',`
`             'padding': '12px',`
`             'padding-right': '12px',`
`             'padding-bottom': '15px',`
`             'background-color': '#e8eeff',`
`             'border': '1px solid #ccd9ff'`
`           }`
`       );`
`       $(".mw-dismissable-notice-close2").css(`
`           {`
`               'position': 'relative',`
`               'top': '0px',`
`               'right': '0px',`
`               'text-align': 'right',`
`               'float': 'right'`
`           }`
`       );`
`   } else {`
`       $("#siteNoticeLocal").css(`
`           { 'padding-top': '5px',`
`             'padding-bottom': '5px',`
`             'background-color': '#e8eeff',`
`             'border': '1px solid #ccd9ff',`
`             'margin-bottom': '5px'`
`           }`
`       );`
`       $(".mw-dismissable-notice-close2").css(`
`           {`
`               'position': 'relative',`
`               'top': '0px',`
`               'right': '7px',`
`               'text-align': 'right',`
`               'float': 'right'`
`           }`
`       );`
`   }`

`   $( '.mw-dismissable-notice-close2' )`
`       .css( 'visibility', 'visible' )`
`       .find( 'a' )`
`       .on( 'click keypress', function ( e ) {`
`           if (`
`               e.type === 'click' ||`
`               e.type === 'keypress' && e.which === 13`
`           ) {`
`               $("#siteNoticeLocal").hide();`
`               $.cookie( cookieName, sitenoticeId, {`
`                   expires: 30,`
`                   path: '/'`
`               } );`
`           }`
`       });`

}

if (/bot|googlebot|crawler|spider|robot|crawling/i.test(navigator.userAgent)) {

`   $("#siteNotice").html("");`
`   $(".noprint").html("");`
`   $(".mw-jump-link").html("");`

} else {

`   $.get("/w/api.php?action=parse&format=json&page=" + noticeGrpPage, function(data) {`
`       var html = data.parse.text["*"].replace("mw-parser-output", "mw-dismissable-notice");`
`       var gadgetSiteNotice = getDivHtml(html, "#gadgetSiteNotice");`
`       var gadgetAnonnotice = html2text(getDivHtml(html, "#gadgetAnonnotice")).trim();`
`       var sitenoticeId = getDivText(html, "#sitenoticeId");`

`       if (mw.config.get('wgUserName') !== null) {`
`           if(/\S/.test(html2text(gadgetSiteNotice).trim())) {`
`               // If the user has the notice dismissal cookie set, exit.`
`               if ( $.cookie( cookieName ) !== sitenoticeId ) {`
`                   $("#siteNotice").append('`

<div id="siteNoticeLocal">

' + gadgetSiteNotice + '

</div>

');

`                   procDismiss(sitenoticeId);`
`               }`
`           }`
`           return;`
`       }`
`       if (gadgetAnonnotice.length === 0) {`
`           return;`
`       } else if (/^\s*-\s*$/.test(gadgetAnonnotice)) {`
`           if(/\S/.test(html2text(gadgetSiteNotice).trim())) {`
`               // If the user has the notice dismissal cookie set, exit.`
`               if ( $.cookie( cookieName ) !== sitenoticeId ) {`
`                   $("#siteNotice").append('`

<div id="siteNoticeLocal">

' + gadgetSiteNotice + '

</div>

');

`                   procDismiss();`
`               }`
`           }`
`       } else {`
`           $("#siteNotice").append('`

<div id="siteNoticeLocal">

' + gadgetAnonnotice + '

</div>

');

`       }`
`   });`

}

}());