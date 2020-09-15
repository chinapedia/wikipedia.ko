> This article is converted from Wikipedia: [미디어위키:Gadget-scrollUpButton.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-scrollUpButton.js).


/\* scrollUpButton

  - Add a button to scroll up to the top of the current page.
  - @rev 3 (2019-28-07)
  - @author Kwj2772
  - @contributor Perhelion
  - No internationalisation required
  - \[kowiki\] Fixed an issue with help-panel-button ([ko:User:ykhwong](https://ko.wikipedia.org/wiki/ko:User:ykhwong "wikilink"))
  - <nowiki>
  - /

/\* global $:false \*/ $(function () { 'use strict';

var $icon = '//upload.wikimedia.org/wikipedia/commons/5/59/Font_Awesome_5_regular_arrow-circle-up_blue.svg'; var helpPanelButtonFound = false;

if (\!document.implementation.hasFeature('<http://www.w3.org/TR/SVG11/feature#Image>', '1.1'))

`   $icon = '//upload.wikimedia.org/wikipedia/commons/thumb/5/59/Font_Awesome_5_regular_arrow-circle-up_blue.svg/32px-Font_Awesome_5_regular_arrow-circle-up_blue.svg.png';`

$icon = $('<img>', {

`   src: $icon,`
`   id: 'scrollUpButton'`

}).css({

`       position: 'fixed',`
`       bottom: '24px',`
`       right: '18px',`
`       opacity: 0.7,`
`       cursor: 'pointer',`
`       display: 'none'`
`   }).on('click', function () {`
`       // Move to the top of the page`
`       $('html, body').animate({ scrollTop: 0 }, 660);`
`   }).on('mouseenter mouseleave', function (e) {`
`       this.style.opacity = e.type === 'mouseenter' ? 1 : 0.7;`
`   }).appendTo('body');`

$(window).on('scroll', function () {

`   if (!helpPanelButtonFound && $("#mw-ge-help-panel-cta-button").length > 0) {`
`       $("img#scrollUpButton").css({`
`           bottom: '75px'`
`       });`
`       helpPanelButtonFound = true;`
`   }`

`   // Fade out if you reach the top of the page`
`   if ($(this).scrollTop() > 60) $icon.fadeIn('slow');`
`   else $icon.fadeOut('slow');`

});

}());