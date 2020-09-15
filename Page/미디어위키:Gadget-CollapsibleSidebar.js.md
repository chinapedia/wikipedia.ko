> This article is converted from Wikipedia: [미디어위키:Gadget-CollapsibleSidebar.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-CollapsibleSidebar.js).


/\*

  - CollapsibleSidebar
  - @author ykhwong
  - /

$(function () { const sidebarCookieName = 'sidebarHidden'; const commonImgUrl = "<https://upload.wikimedia.org/wikipedia/commons/thumb>"; const img = {

`   next: commonImgUrl + "/9/95/Icons8_flat_next.svg/15px-Icons8_flat_next.svg.png",`
`   prev: commonImgUrl + "/b/bd/Icons8_flat_previous.svg/15px-Icons8_flat_previous.svg.png",`
`   logo: commonImgUrl + "/3/3e/WP_mobile_launch_icon.svg/30px-WP_mobile_launch_icon.svg.png"`

}; const isMobile = /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent); const cookieExpires = 30; var sidebarHidden = false; var sidebarGadgetLoaded = false; var fadeSpeed=15; var lastTime = 0; var sDiv, timer;

function autoHide() {

`   if( isMobile ) {`
`       return;`
`   }`
`   sDiv = document.getElementById('sidebarCollapse').style;`
`   sDiv.opacity = 0;`
`   $(document).on('mousemove', function(e){`
`       var thisTime = Math.round(Date.now()/1000);`
`       if ((thisTime - lastTime) < 1) {`
`           return;`
`       }`
`       lastTime = thisTime;`
`       clearTimeout(timer);`
`       (function fadeIn(){(`
`           sDiv.opacity=parseFloat(sDiv.opacity)+0.1);`
`           if (sDiv.opacity<1) {`
`               setTimeout(fadeIn, fadeSpeed);`
`           } else {`
`               clearTimeout(timer);`
`           }`
`       })();`
`       timer = setTimeout(function() {`
`           (function fadeOut(){(`
`               sDiv.opacity=parseFloat(sDiv.opacity)-0.1);`
`               if (sDiv.opacity<0) {`
`                   clearTimeout(timer);`
`               } else {`
`                   setTimeout(fadeOut, fadeSpeed);`
`               }`
`           })();`
`           clearTimeout(timer);`
`       }, 1500);`
`   });`

}

function hideSidebar() {

`   sidebarHidden = true;`
`   $("#sidebarCollapse").attr("src", img.next);`
`   updatePos();`

`   $("#content").css({`
`       "position": "relative",`
`       "left": "-145px",`
`       "right": "0px",`
`       "margin-right": "-145px"`
`   });`
`   $("#mw-data-after-content").css({`
`       "position": "relative",`
`       "left": "-145px",`
`       "right": "0px",`
`       "margin-right": "-145px"`
`   });`
`   $("#footer").css({`
`       "margin-left": "20px"`
`   });`
`   $("#mw-panel").hide();`
`   $("#sliderCollapseLogo, #sliderCollapseText").show();`
`   $.cookie( sidebarCookieName, "true", {`
`       expires: cookieExpires, path: '/'`
`   });`

}

function showSidebar() {

`   sidebarHidden = false;`
`   $("#sidebarCollapse").attr("src", img.prev);`
`   updatePos();`

`   $("#content").css({`
`       "position": "static",`
`       "left": "0px",`
`       "right": "auto",`
`       "margin-right": "0px"`
`   });`
`   $("#mw-data-after-content").css({`
`       "position": "static",`
`       "left": "0px",`
`       "right": "auto",`
`       "margin-right": "0px"`
`   });`
`   $("#footer").css({`
`       "margin-left": "167px"`
`   });`
`   $("#mw-panel").show();`
`   $("#sliderCollapseLogo, #sliderCollapseText").hide();`
`   $.cookie( sidebarCookieName, "false", {`
`       expires: cookieExpires, path: '/'`
`   });`

}

function updatePosHelper(arr) {

`   const divList = [ "#sidebarCollapse", "#sliderCollapseLogo", "#sliderCollapseText" ];`
`   for (var i=0; i < arr.length; i++) {`
`       if (arr[i] === null) {`
`           continue;`
`       }`
`       const bDiv = divList[i];`
`       const bLeft = $(bDiv).css("left");`
`       const bSize = arr[i];`
`       if (bLeft !== bSize) {`
`           $(bDiv).css("left", bSize);`
`       }`
`   }`

}

function updatePos() {

`   if ($("#mw-panel").outerWidth() > 160) {`
`       updatePosHelper(sidebarHidden ? ["20px", "30px", "70px"] : ["165px", null, null]);`
`   } else {`
`       updatePosHelper(sidebarHidden ? ["4px", "15px", "55px"] : ["149px", null, null]);`
`   }`
`   if (mw.user.options.get("visualeditor-newwikitext") === "1") {`
`       var menuloc = $(".oo-ui-toolbar").offset().top + $(".oo-ui-toolbar-bar").outerHeight(true); `
`       $("#sidebarCollapse").css("top", ( menuloc + 15 ) + "px");`
`   }`

}

function sidebarHiddenProc() {

`   var myLang = "";`
`   var sidebarCollapse = "";`
`   var newLink = "";`
`   var sidebarTitle = mw.config.get("wgSiteName");`

`   sidebarGadgetLoaded = true;`
`   myLang = window.location.host.split('.')[0];`

`   sidebarCollapse = $('`<img />`').attr({`
`       'id': 'sidebarCollapse',`
`       'src': img.prev,`
`   }).css({`
`       'position': 'fixed',`
`       'float': 'right',`
`       'width': '13px',`
`       'height': '13px',`
`       'top': '140px',`
`       'cursor': 'pointer',`
`       'padding': '5px',`
`       '-webkit-border-radius': '50px',`
`       '-moz-border-radius': '50px',`
`       'border-radius': '50px',`
`       'text-align': 'center',`
`       'border': '1px solid rgb(199, 238, 255)',`
`       'background': 'white',`
`       'z-index': '2'`
`   });`

`   newLink = $('`<a />`').attr({`
`       'id': 'newLink',`
`       'href': '/',`
`       'title': $(".mw-wiki-logo").attr("title")`
`   });`

`   $('`<img />`').attr({`
`       'id': 'sliderCollapseLogo',`
`       'src': img.logo`
`   }).css({`
`       'display': 'none',`
`       'position': 'absolute',`
`       'top': '47px',`
`       'cursor': 'pointer',`
`       'float': 'none'`
`   }).appendTo(newLink);`

`   $('`

<div />

').attr({

`       'id': 'sliderCollapseText'`
`   }).css({`
`       'display': 'none',`
`       'position': 'absolute',`
`       'top': '50px',`
`       'color': 'black',`
`       'text-decoration': 'none'`
`   }).html(`
`       sidebarTitle`
`   ).appendTo(newLink);`

`   sidebarCollapse.appendTo('#mw-navigation');`
`   newLink.appendTo('#mw-navigation');`

`   if ( $.cookie( sidebarCookieName ) === "true" ) {`
`       hideSidebar();`
`   }`
`   updatePos();`
`   autoHide();`

`   $(window).resize(function() {`
`       updatePos();`
`   });`

`   $("#sidebarCollapse").mouseover(function() {`
`       $(this).css("background", "rgb(223, 245, 255)");`
`   }).mouseout(function() {`
`       $(this).css("background", "white");`
`   }).click(function() {`
`       sidebarHidden ? showSidebar() : hideSidebar();`
`   });`

}

function sidebarHiddenInit() {

`   // Should only work with vector skin`
`   // Exception handling: Blankpage and RTRC`
`   if (`
`       mw.config.get( 'skin' ) !== 'vector' ||`
`       $(".skin-vector-legacy").length === 0 || $(".mw-special-Blankpage").length !== 0`
`   ) {`
`       return;`
`   }`

`   if ( $('#mw-navigation').length === 0 ) {`
`       var obs = new MutationObserver(function(mutations, observer) {`
`           if (sidebarGadgetLoaded) {`
`               return;`
`           }`
`           for (var i=0; i<mutations.length; ++i) {`
`               for (var j=0; j<mutations[i].addedNodes.length; ++j) {`
`                   if (mutations[i].addedNodes[j].id == "mw-navigation") {`
`                       sidebarHiddenProc();`
`                       break;`
`                   }`
`               }`
`           }`
`       });`
`       obs.observe(document.body, { childList: true });`
`       return;`
`   }`

`   sidebarHiddenProc();`

}

sidebarHiddenInit(); }());