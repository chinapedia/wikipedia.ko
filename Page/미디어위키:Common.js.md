> This article is converted from Wikipedia: [:Common.js](https://ko.wikipedia.org/wiki/:Common.js).


/\*\*

`* 이 스크립트는 위키백과 전체에 적용됩니다. 고칠 때는 주의해주세요.`
`* `[`위키백과:위키프로젝트``   ``시스템`](https://ko.wikipedia.org/wiki/위키백과:위키프로젝트_시스템 "wikilink")` 참고`
`*`
`* 스크립트를 넣을 때는 충분한 설명, 출처를 넣어주세요! 이후 관리가 어려워집니다.`
`**/`

/\* global mw, $ \*/ /\* jshint strict:false, browser:true \*/

mw.loader.using( \['mediawiki.user', 'mediawiki.util', 'mediawiki.notify'\] ).done( function () { /\* Begin of mw.loader.using callback \*/

/\*\*

`* Main Page layout fixes`
`*`
`* Description: Adds an additional link to the complete list of languages available.`
`* Maintainers: `[`User:AzaToth`](https://ko.wikipedia.org/wiki/User:AzaToth "wikilink")`, `[`User:R.``   ``Koot`](https://ko.wikipedia.org/wiki/User:R._Koot "wikilink")`, `[`User:Alex``   ``Smotrov`](https://ko.wikipedia.org/wiki/User:Alex_Smotrov "wikilink")
`*/`

if ( mw.config.get( 'wgPageName' ) === '위키백과:대문' || mw.config.get( 'wgPageName' ) === '위키백과토론:대문' ) {

`   $( function () {`
`       mw.util.addPortletLink( 'p-lang', '//meta.wikimedia.org/wiki/List_of_Wikipedias/ko',`
`           '전체 목록', 'interwiki-completelist', '위키백과 전체 목록' );`
`   } );`

}

/\*\*

`* Redirect User:Name/skin.js and skin.css to the current skin's pages`
`* (unless the 'skin' page really exists)`
`* @source: `<http://www.mediawiki.org/wiki/Snippets/Redirect_skin.js>
`* @rev: 2`
`*/`

if ( mw.config.get( 'wgArticleId' ) === 0 && mw.config.get( 'wgNamespaceNumber' ) === 2 ) {

`   var titleParts = mw.config.get( 'wgPageName' ).split( '/' );`
`   /* Make sure there was a part before and after the slash`
`      and that the latter is 'skin.js' or 'skin.css' */`
`   if ( titleParts.length == 2 ) {`
`       var userSkinPage = titleParts.shift() + '/' + mw.config.get( 'skin' );`
`       if ( titleParts.slice( -1 ) == 'skin.js' ) {`
`           window.location.href = mw.util.getUrl( userSkinPage + '.js' );`
`       } else if ( titleParts.slice( -1 ) == 'skin.css' ) {`
`           window.location.href = mw.util.getUrl( userSkinPage + '.css' );`
`       }`
`   }`

}

/\*\*

`* Map addPortletLink to mw.util`
`* @deprecated: Use mw.util.addPortletLink instead.`
`*/`

mw.log.deprecate( window, 'addPortletLink', mw.util.addPortletLink, 'Use mw.util.addPortletLink instead' );

/\*\*

`* Extract a URL parameter from the current URL`
`* @deprecated: Use mw.util.getParamValue with proper escaping`
`*/`

mw.log.deprecate( window, 'getURLParamValue', mw.util.getParamValue, 'Use mw.util.getParamValue instead' );

/\*\*

`* Test if an element has a certain class`
`* @deprecated:  Use $(element).hasClass() instead.`
`*/`

mw.log.deprecate( window, 'hasClass', function ( element, className ) {

`   return $( element ).hasClass( className );`

}, 'jQuery.hasClass()를 대신 사용하십시오' );

/\*\*

`* @source www.mediawiki.org/wiki/Snippets/Load_JS_and_CSS_by_URL`
`* @rev 6`
`*/`

var extraCSS = mw.util.getParamValue( 'withCSS' ),

`   extraJS = mw.util.getParamValue( 'withJS' );`

if ( extraCSS ) {

`   if ( extraCSS.match( /^(MediaWiki|미디어위키):[^&<>=%#]*\.css$/ ) ) {`
`       mw.loader.load( '/w/index.php?title=' + extraCSS + '&action=raw&ctype=text/css', 'text/css' );`
`   } else {`
`       mw.notify( '미디어위키 이름공간의 문서만 허용됩니다.', { title: '유효하지 않은 withCSS 값' } );`
`   }`

}

if ( extraJS ) {

`   if ( extraJS.match( /^(MediaWiki|미디어위키):[^&<>=%#]*\.js$/ ) ) {`
`       mw.loader.load( '/w/index.php?title=' + extraJS + '&action=raw&ctype=text/javascript' );`
`   } else {`
`       mw.notify( '미디어위키 이름공간의 문서만 허용됩니다.', { title: '유효하지 않은 withJS 값' } );`
`   }`

}

/\* 인터랙티브 지도. 영어 위키백과에서 가져옴. -- [사용자:ChongDae](https://ko.wikipedia.org/wiki/사용자:ChongDae "wikilink") 2010년 3월 28일 (일) 02:08 (KST) \*/ /\*\*

`* WikiMiniAtlas`
`*`
`* Description: WikiMiniAtlas is a popup click and drag world map.`
`*              This script causes all of our coordinate links to display the WikiMiniAtlas popup button.`
`*              The script itself is located on meta because it is used by many projects.`
`*              See `[`Meta:WikiMiniAtlas`](https://ko.wikipedia.org/wiki/Meta:WikiMiniAtlas "wikilink")` for more information.`
`* Note - use of this service is recommended to be replaced with mw:Help:Extension:Kartographer`
`*/`

$( function () {

`   var require_wikiminiatlas = $( 'a.external.text[href*="geohack"]' ).length || $( 'div.kmldata' ).length;`
`   if ( require_wikiminiatlas ) {`
`       mw.loader.load( '//meta.wikimedia.org/w/index.php?title=MediaWiki:Wikiminiatlas.js&action=raw&ctype=text/javascript' );`
`   }`

} );

/\*\*

`* Collapsible tables; reimplemented with mw-collapsible`
`* Styling is also in place to avoid FOUC`
`* `
`* Allows tables to be collapsed, showing only the header. See `[`Help:Collapsing`](https://ko.wikipedia.org/wiki/Help:Collapsing "wikilink")`.`
`* @version 3.0.0 (2018-05-20)`
`* @source `<https://www.mediawiki.org/wiki/MediaWiki:Gadget-collapsibleTables.js>
`* @author `[`User:R.``   ``Koot`](https://ko.wikipedia.org/wiki/User:R._Koot "wikilink")
`* @author `[`User:Krinkle`](https://ko.wikipedia.org/wiki/User:Krinkle "wikilink")
`* @author `[`User:TheDJ`](https://ko.wikipedia.org/wiki/User:TheDJ "wikilink")
`* @deprecated Since MediaWiki 1.20: Use class="mw-collapsible" instead which`
`* is supported in MediaWiki core. Shimmable since MediaWiki 1.32`
`*/`

function makeCollapsibleMwCollapsible( $content ) {

`   var $tables = $content`
`       .find( 'table.collapsible:not(.mw-collapsible)' )`
`       .addClass( 'mw-collapsible' );`

`   $.each( $tables, function( index, table ) {`
`       // mw.log.warn( '이 문서는 구식 클래스 collapsible을 사용하고 있습니다. mw-collapsible로 변경해 주십시오.');`
`       if( $( table ).hasClass( 'collapsed') ) {`
`           $( table ).addClass( 'mw-collapsed' );`
`           // mw.log.warn( '이 문서는 구식 클래스 collapsed를 사용하고 있습니다. mw-collapsed로 변경해 주십시오.');`
`       }`
`   } );`
`   if( $tables.length > 0 ) {`
`       mw.loader.using( 'jquery.makeCollapsible' ).then( function() {`
`           $tables.makeCollapsible();`
`       } );`
`   }`

} mw.hook( 'wikipage.content' ).add( makeCollapsibleMwCollapsible );

/\*\*

`* Add support to mw-collapsible for autocollapse, innercollapse and outercollapse`
`*`
`* Maintainers: TheDJ`
`*/`

function mwCollapsibleSetup( $collapsibleContent ) {

`   var $element,`
`       $toggle,`
`       autoCollapseThreshold = 2;`
`   $.each( $collapsibleContent, function (index, element) {`
`       $element = $( element );`
`       if ( $element.hasClass( 'collapsible' ) ) {`
`           $element.find('tr:first > th:first').prepend( $element.find('tr:first > * > .mw-collapsible-toggle'));`
`       }`
`       if ( $collapsibleContent.length >= autoCollapseThreshold && $element.hasClass( 'autocollapse' ) ) {`
`           $element.data( 'mw-collapsible' ).collapse();`
`       } else if ( $element.hasClass( 'innercollapse' ) ) {`
`           if ( $element.parents( '.outercollapse' ).length > 0 ) {`
`               $element.data( 'mw-collapsible' ).collapse();`
`           }`
`       }`
`       // because of colored backgrounds, style the link in the text color`
`       // to ensure accessible contrast`
`       $toggle = $element.find( '.mw-collapsible-toggle' );`
`       if ( $toggle.length ) {`
`           // Make the toggle inherit text color`
`           if( $toggle.parent()[0].style.color ) {`
`               $toggle.find( 'a' ).css( 'color', 'inherit' );`
`           }`
`       }`
`   } );`

}

mw.hook( 'wikipage.collapsibleContent' ).add( mwCollapsibleSetup );

/\*\*

`* Dynamic Navigation Bars (experimental)`
`*`
`* Description: See `[`Wikipedia:NavFrame`](https://ko.wikipedia.org/wiki/Wikipedia:NavFrame "wikilink")`.`
`* Maintainers: UNMAINTAINED`
`*/`

var collapseCaption = '숨기기'; var expandCaption = '보이기';

// Set up the words in your language var navigationBarHide = '\[' + collapseCaption + '\]'; var navigationBarShow = '\[' + expandCaption + '\]';

/\*\*

`* Shows and hides content and picture (if available) of navigation bars.`
`*`
`* @param {number} indexNavigationBar The index of navigation bar to be toggled`
`* @param {jQuery.Event} event Event object`
`*/`

function toggleNavigationBar( indexNavigationBar, event ) {

`   var navToggle = document.getElementById( 'NavToggle' + indexNavigationBar );`
`   var navFrame = document.getElementById( 'NavFrame' + indexNavigationBar );`
`   var navChild;`

`   if ( !navFrame || !navToggle ) {`
`       return false;`
`   }`

`   // If shown now`
`   if ( navToggle.firstChild.data === navigationBarHide ) {`
`       for ( navChild = navFrame.firstChild; navChild !== null; navChild = navChild.nextSibling ) {`
`           if ( $( navChild ).hasClass( 'NavContent' ) ) {`
`               navChild.style.display = 'none';`
`           }`
`       }`
`       navToggle.firstChild.data = navigationBarShow;`
`   `
`   // If hidden now`
`   } else if ( navToggle.firstChild.data === navigationBarShow ) {`
`       for ( navChild = navFrame.firstChild; navChild !== null; navChild = navChild.nextSibling ) {`
`           if ( $( navChild ).hasClass( 'NavContent' ) ) {`
`               navChild.style.display = 'block';`
`           }`
`       }`
`       navToggle.firstChild.data = navigationBarHide;`
`   }`

`   event.preventDefault();`

}

/\*\*

`* Adds show/hide-button to navigation bars.`
`*`
`* @param {jQuery} $content`
`*/`

function createNavigationBarToggleButton( $content ) {

`   var i, j, navChild, navToggle, navToggleText, isCollapsed,`
`       indexNavigationBar = 0;`
`   // Iterate over all < div >-elements`
`   var $divs = $content.find( 'div.NavFrame:not(.mw-collapsible)' );`
`   $divs.each( function ( i, navFrame ) {`
`       indexNavigationBar++;`
`       navToggle = document.createElement( 'a' );`
`       navToggle.className = 'NavToggle';`
`       navToggle.setAttribute( 'id', 'NavToggle' + indexNavigationBar );`
`       navToggle.setAttribute( 'href', '#' );`
`       $( navToggle ).on( 'click', $.proxy( toggleNavigationBar, null, indexNavigationBar ) );`

`       isCollapsed = $( navFrame ).hasClass( 'collapsed' );`
`       /**`
`        * Check if any children are already hidden.  This loop is here for backwards compatibility:`
`        * the old way of making NavFrames start out collapsed was to manually add style="display:none"`
`        * to all the NavPic/NavContent elements.  Since this was bad for accessibility (no way to make`
`        * the content visible without JavaScript support), the new recommended way is to add the class`
`        * "collapsed" to the NavFrame itself, just like with collapsible tables.`
`        */`
`       for ( navChild = navFrame.firstChild; navChild !== null && !isCollapsed; navChild = navChild.nextSibling ) {`
`           if ( $( navChild ).hasClass( 'NavPic' ) || $( navChild ).hasClass( 'NavContent' ) ) {`
`               if ( navChild.style.display === 'none' ) {`
`                   isCollapsed = true;`
`               }`
`           }`
`       }`
`       if ( isCollapsed ) {`
`           for ( navChild = navFrame.firstChild; navChild !== null; navChild = navChild.nextSibling ) {`
`               if ( $( navChild ).hasClass( 'NavPic' ) || $( navChild ).hasClass( 'NavContent' ) ) {`
`                   navChild.style.display = 'none';`
`               }`
`           }`
`       }`
`       navToggleText = document.createTextNode( isCollapsed ? navigationBarShow : navigationBarHide );`
`       navToggle.appendChild( navToggleText );`

`       // Find the NavHead and attach the toggle link (Must be this complicated because Moz's firstChild handling is borked)`
`       for ( j = 0; j < navFrame.childNodes.length; j++ ) {`
`           if ( $( navFrame.childNodes[j] ).hasClass( 'NavHead' ) ) {`
`               navToggle.style.color = navFrame.childNodes[j].style.color;`
`               navFrame.childNodes[j].appendChild( navToggle );`
`           }`
`       }`
`       navFrame.setAttribute( 'id', 'NavFrame' + indexNavigationBar );`
`   } );`

}

mw.hook( 'wikipage.content' ).add( createNavigationBarToggleButton );

/\*\*

`* 편집 안내 ****************************************************`
`*`
`* 생존 인물에 대한 편집 안내. 영어 위키백과에서 가져옴 - ChongDae`
`* Description: Adds editintros on disambiguation pages and BLP pages.`
`* Maintainers: `[`User:RockMFR`](https://ko.wikipedia.org/wiki/User:RockMFR "wikilink")
`*/`

function addEditIntro( name ) {

`   $( '.mw-editsection, #ca-edit' ).find( 'a' ).each( function ( i, el ) {`
`       el.href = $( this ).attr( 'href' ) + '&editintro=' + name;`
`   } );`

}

if ( mw.config.get( 'wgNamespaceNumber' ) === 0 ) {

`   $( function () {`
`       var cats = mw.config.get('wgCategories');`
`       if ( !cats ) {`
`           return;`
`       }`
`       if ( $.inArray( '살아있는 사람', cats ) !== -1 || $.inArray( '생사 불명', cats ) !== -1 ) {`
`           addEditIntro( '틀:BLP_편집_안내' );`
`       }`
`   } );`

}

/\* Actions specific to the edit page \*/ if ( mw.config.get( 'wgAction' ) === 'edit' || mw.config.get( 'wgAction' ) === 'submit' ) {

`   /**`
`    * Fix edit summary prompt for undo`
`    *`
`    *  Fixes the fact that the undo function combined with the "no edit summary prompter"`
`    *  complains about missing editsummary, if leaving the edit summary unchanged.`
`    *  Added by `[`User:Deskana`](https://ko.wikipedia.org/wiki/User:Deskana "wikilink")`, code by `[`User:Tra`](https://ko.wikipedia.org/wiki/User:Tra "wikilink")`.`
`    *  See also `[`phab:T10912`](https://ko.wikipedia.org/wiki/phab:T10912 "wikilink")`.`
`    */`
`   $(function () {`
`       if (document.location.search.indexOf('undo=') !== -1 && document.getElementsByName('wpAutoSummary')[0]) {`
`           document.getElementsByName('wpAutoSummary')[0].value = '1';`
`       }`
`   });`

}

/\*\*\*\*\* 그림 정보 틀을 자동으로 불러옴 \*\*\*\*\*\*\*\*

`* Adds a link to subpages of current page`
`* from commons.wikimedia.org`
`*  Maintainers: `[`User:Yonidebest`](https://ko.wikipedia.org/wiki/User:Yonidebest "wikilink")`, `[`User:Dschwen`](https://ko.wikipedia.org/wiki/User:Dschwen "wikilink")
`*  `[`사용자:Kwj2772`](https://ko.wikipedia.org/wiki/사용자:Kwj2772 "wikilink")가` 수정`
`*  JSconfig items: bool 'loadAutoInformationTemplate'`
`*                       (true=enabled (default), false=disabled)`
`* JSConfig를 사용하지 않도록 수정함. --`[`klutzy`](https://ko.wikipedia.org/wiki/사용자:Klutzy "wikilink")` (`[`토론`](https://ko.wikipedia.org/wiki/사용자토론:Klutzy "wikilink")`) 2009년 9월 27일 (일) 20:33 (KST)`
`****/`

if (mw.config.get('wgCanonicalSpecialPageName') == 'Upload') {

` importScript('MediaWiki:Upload.js');`

}

/\* End of mw.loader.using callback \*/ } ); /\* DO NOT ADD CODE BELOW THIS LINE \*/