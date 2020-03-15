> This article is converted from Wikipedia: [:Mobile.css](https://ko.wikipedia.org/wiki/:Mobile.css).


/\* 이 CSS 설정은 모바일 사이트를 사용하는 사용자에게 적용됩니다 \*/

/\* Mobile template hacks (see phab T56176) \*/ .mobile-float-reset {

`   float: none !important;`
`   width: 100% !important;`

}

/\* Hide the images \*/ .geo-nondefault, .geo-multi-punct, /\* Hide stuff meant for accounts with special permissions. Made visible again in

`  `[`MediaWiki:Group-sysop.css`](https://ko.wikipedia.org/wiki/MediaWiki:Group-sysop.css "wikilink")`, `[`MediaWiki:Group-accountcreator.css`](https://ko.wikipedia.org/wiki/MediaWiki:Group-accountcreator.css "wikilink")` and`
`  `[`MediaWiki:Group-autoconfirmed.css`](https://ko.wikipedia.org/wiki/MediaWiki:Group-autoconfirmed.css "wikilink")`. */`

.sysop-show, .accountcreator-show, .autoconfirmed-show, /\* Copied from Common.css - allow for hiding text in compact form e.g. clean up templates \*/ .hide-when-compact, /\* portal pages are badly formatted. Until this changes these should be hidden. (see <https://phabricator.wikimedia.org/T86495>) \*/ .noprint.portal {

`   display: none;`

}

/\* For linked citation numbers and document IDs, where

`  the number need not be shown on a screen or a handheld,`
`  but should be included in the printed version`

TODO: Move to Citation template when templates have stylesheets See <https://www.mediawiki.org/wiki/Requests_for_comment/Allow_styling_in_templates>

  - /

@media screen, handheld {

`   .citation *.printonly {`
`       display: none;`
`   }`

} /\* Styling for citations (CSS3). Breaks long urls, etc., rather than overflowing box \*/ .citation {

`   word-wrap: break-word;`

}

/\* override default center aligning of th cells in some browsers,

`* most th cells in infoboxes are row headers and left aligned */`

.infobox \> th {

`   /* @noflip */`
`   text-align: left;`

}

/\* Default styling for Navbar template TODO: Move to Navbar template when templates have stylesheets See <https://www.mediawiki.org/wiki/Requests_for_comment/Allow_styling_in_templates>

  - /

.navbar {

`   display: inline;`
`   font-size: 88%;`
`   font-weight: normal;`

} .navbar ul {

`   display: inline;`
`   white-space: nowrap;`

} .navbar li {

`   word-spacing: -0.125em;`

} .navbar.mini li span {

`   font-variant: small-caps;`

} /\* Navbar styling when nested in infobox and navbox \*/ .navbox .navbar, .infobox .navbar {

`   font-size: 100%;`

} .navbox .navbar {

`   display: block;`

} .navbox-title .navbar {

`   /* @noflip */`
`   float: left;`
`   /* @noflip */`
`   text-align: left;`
`   /* @noflip */`
`   margin-right: 0.5em;`
`   width: 6em;`

} /\* Unbulleted lists e.g. Barack Obama page \*/ .plainlist ul {

`   list-style: none;`

}

.visualhide {

`   position: absolute;`
`   left: -10000px;`
`   top: auto;`
`   width: 1px;`
`   height: 1px;`
`   overflow: hidden;`

}

/\* Hatnotes and disambiguation notices Please review the default hatnote styles provided by MobileFrontend before adding here.

  - /

.hatnote i {

`   font-style: normal;`

} div.hatnote {

`   /* @noflip */`
`   /*padding-left: 1.6em;`
`   margin-bottom: 0.5em;`
`   commented out until `<https://phabricator.wikimedia.org/T130846>` is resolved*/`

}

/\* Geographical coordinates defaults. See [Template:Coord/link](https://ko.wikipedia.org/wiki/Template:Coord/link "wikilink")

`  for how these are used. The classes "geo", "longitude", and`
`  "latitude" are used by the `[`Geo``   ``microformat`](https://ko.wikipedia.org/wiki/Geo_microformat "wikilink")`. */`

.geo-default, .geo-dms, .geo-dec { display: inline; }

.longitude, .latitude { white-space: nowrap; }

/\* Prevent line breaks in silly places:

`  1) Where desired`
`  2) Links when we don't want them to`
`  3) Bold "links" to the page itself`
`  4) Ref tags with group names `<ref group="Note">` --> "[Note 1]"`

Please document here what pages use this Enabled

  - /

.mw-parser-output .nowrap, .nowraplinks a, .nowraplinks .selflink, sup.reference a {

`   white-space: nowrap;`

} .mw-parser-output .infobox .nowrap {

`   white-space: normal !important;`

} /\* But allow wrapping where desired: \*/ .wrap, .wraplinks a {

`   white-space: normal;`

}

/\* hidden sortkey for tablesorter \*/ td .sortkey, th .sortkey {

`   display: none;`
`   speak: none;`

}

/\* Pie chart: Transparent borders \*/ .transborder {

`   border: solid transparent;`

}

/\* Generic class for Times-based serif, texhtml class for inline math \*/ /\* .times-serif, span.texhtml {

`   font-family: serif;`

}

  - /

span.texhtml {

`   white-space: nowrap;`

}

/\* Enable custom list style types for lists of references \*/ .reflist ol.references {

`   list-style-type: inherit;`

}

/\* Hanging indentation for Template:Refbegin \*/ .refbegin-hanging-indents \> ul, .refbegin-hanging-indents \> dl {

`   list-style-type: none;`
`   margin-left: 0;`

} .refbegin-hanging-indents \> ul \> li, .refbegin-hanging-indents \> dl \> dd {

`   margin-left: 0;`
`   padding-left: 1.0em;`
`   text-indent: -1.0em;`
`   list-style: none;`

}

/\* Prevent flags in tables from collapsing \*/ .flagicon img {

`   min-width: 25px;`

}

/\* Prevent unnecessary margin at the bottom of centralnotices \*/ .cnotice {

`   margin-bottom: 0 !important;`

}

/\*\*

  -   - DEPRECATED STYLES \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

These styles will be removed shortly. Please see inline comments.

  -   - /

/\* Generate interpuncts Should be removed and moved to templates once TemplateStyles is live

  - /

<!-- end list -->

1.  content .hlist dt:after {

`   content: ": ";`

} /\* Can be removed when T169315 is resolved \*/

1.  content .hlist-separated li:after {

`   font-size: 0.8em;`
`   color: #333;`

} /\* Note the mobile skin provides a \`hlist-separated\` class for this purpose. Use this class name alongside the hlist class instead as this will result in a FOUC. Should be removed and moved to templates once TemplateStyles is live

  - /

<!-- end list -->

1.  content .hlist dd:after {

`   content: " · ";`
`   font-weight: bold;`

} /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist dd:last-child:after,
2.  content .hlist dt:last-child:after,
3.  content .hlist li:last-child:after {

`   content: none;`

} /\* Add parentheses around nested lists \*/ /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist dd dd:first-child:before, \#content .hlist dd dt:first-child:before, \#content .hlist dd li:first-child:before,
2.  content .hlist dt dd:first-child:before, \#content .hlist dt dt:first-child:before, \#content .hlist dt li:first-child:before,
3.  content .hlist li dd:first-child:before, \#content .hlist li dt:first-child:before, \#content .hlist li li:first-child:before {

`   content: " (";`
`   font-weight: normal;`

} /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist dd dd:last-child:after, \#content .hlist dd dt:last-child:after, \#content .hlist dd li:last-child:after,
2.  content .hlist dt dd:last-child:after, \#content .hlist dt dt:last-child:after, \#content .hlist dt li:last-child:after,
3.  content .hlist li dd:last-child:after, \#content .hlist li dt:last-child:after, \#content .hlist li li:last-child:after {

`   content: ") ";`
`   font-weight: normal;`

} /\* Put ordinals in front of ordered list items \*/ /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist ol {

`   counter-reset: listitem;`

} /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist ol \> li {

`   counter-increment: listitem;`

} /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist ol \> li:before {

`   content: " " counter(listitem) " ";`
`   white-space: nowrap;`

} /\* Should be removed and moved to templates once TemplateStyles is live \*/

1.  content .hlist dd ol \> li:first-child:before,
2.  content .hlist dt ol \> li:first-child:before,
3.  content .hlist li ol \> li:first-child:before {

`   content: " (" counter(listitem) " ";`

}