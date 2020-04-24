> This article is converted from Wikipedia: [미디어위키:Gadget-direct-commons.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-direct-commons.js).


/\*\*

`* Direct imagelinks to Commons`
`*`
`* Required modules: mediawiki.util`
`*`
`* @source `<https://www.mediawiki.org/wiki/Snippets/Direct_imagelinks_to_Commons>
`* @author Krinkle`
`* @version 2017-08-30`
`*/`

if ( mw.config.get( 'wgNamespaceNumber', 0 ) \>= 0 ) {

`   mw.loader.using( [ 'mediawiki.util' ] ).then( function () {`
`       mw.hook( 'wikipage.content' ).add( function ( $content ) {`
`           var uploadBaseRe = /^(https:)?\/\/upload\.wikimedia\.org\/wikipedia\/commons/,`
`               localFileNSString = mw.config.get( 'wgFormattedNamespaces' )['6'] + ':',`
`               localBasePath = new RegExp( '^' + mw.util.escapeRegExp( mw.util.getUrl( localFileNSString ) ) ),`
`               localBaseScript = new RegExp( '^' + mw.util.escapeRegExp(`
`                   mw.util.wikiScript() + '?title=' + mw.util.wikiUrlencode( localFileNSString )`
`               ) ),`
`               commonsBasePath = '`<https://commons.wikimedia.org/wiki/File>`:',`
`               commonsBaseScript = '`<https://commons.wikimedia.org/w/index.php?title=File>`:';`

`           $content.find( 'a.image' ).attr( 'href', function ( i, currVal ) {`
`               if ( uploadBaseRe.test( $( this ).find( 'img' ).attr( 'src' ) ) ) {`
`                   return currVal`
`                       .replace( localBasePath, commonsBasePath )`
`                       .replace( localBaseScript, commonsBaseScript );`
`               }`
`           } );`
`       } );`
`   } );`

}