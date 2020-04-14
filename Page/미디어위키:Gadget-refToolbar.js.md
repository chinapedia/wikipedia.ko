> This article is converted from Wikipedia: [미디어위키:Gadget-refToolbar.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-refToolbar.js).


/\*\*

`* RefToolbar`
`*`
`* Adds tools for citing references to the edit toolbar.`
`* See `[`Wikipedia:RefToolbar`](https://ko.wikipedia.org/wiki/Wikipedia:RefToolbar "wikilink")` for further documentation. One of two`
`* possible versions will load (Reftoolbar 1.0 or Reftoolbar 1.0)`
`* depending on the user preferences (the usebetatoolbar preference).`
`*`
`* @see: `[`Wikipedia:RefToolbar`](https://ko.wikipedia.org/wiki/Wikipedia:RefToolbar "wikilink")
`* @see: `[`MediaWiki:RefToolbar.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbar.js "wikilink")
`* @see: `[`MediaWiki:RefToolbarConfig.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbarConfig.js "wikilink")
`* @see: `[`MediaWiki:RefToolbarLegacy.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbarLegacy.js "wikilink")
`* @see: `[`MediaWiki:RefToolbarMessages-en.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbarMessages-en.js "wikilink")
`* @see: `[`MediaWiki:RefToolbarMessages-de.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbarMessages-de.js "wikilink")
`* @see: `[`MediaWiki:Gadget-refToolbarBase.js`](https://ko.wikipedia.org/wiki/MediaWiki:Gadget-refToolbarBase.js "wikilink")
`* @author: `[`User:Mr.Z-man`](https://ko.wikipedia.org/wiki/User:Mr.Z-man "wikilink")
`* @author: `[`User:Kaldari`](https://ko.wikipedia.org/wiki/User:Kaldari "wikilink")
`*/`

/\*jshint browser: true, camelcase: true, curly: true, eqeqeq: true \*/ /\*global jQuery, mediaWiki, importScript \*/ ( function ( mw, $ ) { 'use strict'; function initializeRefTools() {

`   if ( window.refToolbarInstalled || $( '#wpTextbox1[readonly]' ).length ){`
`       return;`
`   }`
`       // using weak comparison because ("0") is true, but ("0" == true) is false `
`   if ( mw.user.options.get( 'usebetatoolbar' ) == true ) {`
`       // Enhanced editing toolbar is on. Going to load RefToolbar 2.0.`
`       // TODO:`
`       // * Explicitly declare global variables from `[`MediaWiki:RefToolbar.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbar.js "wikilink")` using window.*`
`       // * Move `[`MediaWiki:RefToolbar.js`](https://ko.wikipedia.org/wiki/MediaWiki:RefToolbar.js "wikilink")` to `[`MediaWiki:Gadget-refToolbarDialogs.js`](https://ko.wikipedia.org/wiki/MediaWiki:Gadget-refToolbarDialogs.js "wikilink")
`       // * Create the module 'ext.gadget.refToolbarDialogs' depending on 'ext.gadget.refToolbarBase' and 'ext.wikiEditor'`
`       // * Replace the code below by mw.loader.load( 'ext.gadget.refToolbarDialogs' );`
`       mw.loader.using( [ 'ext.gadget.refToolbarBase', 'ext.wikiEditor' ], function () {`
`           importScript( '미디어위키:RefToolbar.js' );`
`       } );`
`   } else if ( mw.user.options.get( 'showtoolbar' ) ) {`
`       // Enhanced editing toolbar is off. Loading RefToolbar 1.0. (legacy)`
`       importScript( '//en.wikipedia.org/w/index.php?title=MediaWiki:RefToolbarLegacy.js&action=raw&ctype=text/javascript' );`
`   } else {`
`       return;`
`   }`
`   window.refToolbarInstalled = true;`

}

if ( $.inArray( mw.config.get( 'wgAction' ), \[ 'edit', 'submit' \] ) \!== -1 ) {

`   // Double check if user.options is loaded, to prevent errors when copy pasted accross installations`
`   $.when( mw.loader.using( ['user.options'] ), $.ready ).done( initializeRefTools );`

}

}( mediaWiki, jQuery ) );