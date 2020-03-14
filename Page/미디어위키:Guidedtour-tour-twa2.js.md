> This article is converted from Wikipedia: [:Guidedtour-tour-twa2.js](https://ko.wikipedia.org/wiki/:Guidedtour-tour-twa2.js).


// The Wikipedia Adventure Mission 2

( function ( window, document, $, mw, gt ) {

//automatic api:edit function to send yourself messages function sendMessage( targetPage, msgPage, linkTo ) {

`   var api = new mw.Api();`
`   api.get( {`
`       'action' : 'query',`
`       'titles' : msgPage,`
`       'prop'   : 'revisions|info',`
`       'intoken' : 'edit',`
`       'rvprop' : 'content',`
`       'indexpageids' : 1`
`   } ).done( function (result) {`
`       result = result.query;`
`       var page = result.pages[result.pageids[0]];`
`       var text = page.revisions[0]['*'];`
`       api.post( {`
`           'action' : 'edit',`
`           'title' : targetPage,`
`           'appendtext' : "\n" + text,`
`           'summary' : 'New Message (simulated automatically as part of `[`The``   ``Wikipedia``   ``Adventure`](https://ko.wikipedia.org/wiki/WP:The_Wikipedia_Adventure "wikilink")`)',`
`           'token' : page.edittoken`
`       } ).done( function () {`
`           window.location.href = linkTo;`
`       } );`
`   } );`

}

// Fail gracefully post-save but not postedit var postEditButtons = \[\]; if ( mw.config.get( 'wgAction' ) === 'view' && \!gt.isPostEdit() ) {

`       postEditButtons.push( {`
`               name: 'Click here to go back and make an edit',`
`               onclick: function() {`
`                       window.location.href = new mw.Uri().extend( { action: 'edit' } ).toString();`
`               }`
`       } );`

}

// Fail gracefully post-save but not postedit for visual editor var postEditButtonsVisual = \[\]; if ( mw.config.get( 'wgAction' ) === 'view' && \!gt.isPostEdit() ) {

`       postEditButtonsVisual.push( {`
`               name: 'Go Back',`
`               onclick: function() {`
`                       window.location.href = window.location.href +`

"\&veaction=edit";

`               }`
`       } );`

}

gt.defineTour( {

`       name: 'twa2',`
`       shouldLog: true,`
`       steps: [ {`
`               //1`
`               title: 'Mission 2 begins!',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

Great to see you again. This mission we\\'re going on a quest to communicate with other editors.

',

`               onShow: gt.parseDescription,`
`               overlay: true,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: 'Let\'s dive in',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false`

`       },  {`
`               //2`
`               title: 'The Talk page',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

Like the userpage, every editor has their own TALK page. People can leave you messages.

Hey, look at that...Someone sent you a message.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Wikipedia:TWA/2/Start' ) + '?tour=twa2&step=1'          `
`               } , {`
`                       name: 'Check your new message*',`
`                       onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User talk:' + mw.config.get( 'wgUserName' ) + '/TWA', 'Wikipedia:TWA/MyTalk/1' , mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=3'); }`
`               } ],`
`               allowAutomaticOkay: false`

`       },  {`
`               //3`
`               title: 'Real people',`
`               description: '`

<div align="left">

[TWA_guide_left_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_left_top.png "fig:TWA_guide_left_top.png")

</div>

Wow, that was nice. There are real people here like me.

Let\\'s Reply to the talk page message.

',

`               onShow: gt.parseDescription,`
`               attachTo: '#content.mw-body',`
`               position: 'bottom',`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Wikipedia:TWA/2/Start' ) + '?tour=twa2&step=2'          `
`               } , {`
`                        name: 'Reply to Will',`
`                        action: 'externalLink',`
`                        url: mw.util.getUrl( 'Wikipedia:TWA/2/Will' ) + '?tour=twa2&step=4'`
`               } ],`
`               allowAutomaticOkay: false               `

`       },  {`
`               //4`
`               title: 'Challenge yourself BELOW...',`
`               description: 'Hint: you can learn as much from getting it wrong as getting it right.  And you can always try again!',`
`               attachTo:'#contentSub',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false, `
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=3'          `
`               } ],`

`       },  {`
`               //5`
`               title: 'Write your reply',`
`               description: '`
`Click EDIT SOURCE so you can leave your message to Will`

`',`
`               attachTo: '#ca-edit',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Wikipedia:TWA/2/Will' ) + '?tour=twa2&step=4'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.hasQuery( { action: 'edit' } );`
`               }`

`       },  {`
`               //6`
`               title: 'Copy your message',`
`               description: '`

<div align="left">

[TWA_guide_left_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_left_top.png "fig:TWA_guide_left_top.png")

</div>

Copy and paste the best reply into the editing text box, at the bottom below Will\\'s message to you

:Thanks so much for your friendly welcome \[\[User:WillKomen|User:WillKomen\]\]. I can\\'t wait to start editing\! \~\~\~\~
',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=5'          `
`               } , {`
`                       name: 'Copied',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false`

}, {

`               //7`
`               title: 'Three quick things',`
`               description: '`
<b>`Indent`</b>` replies with a colon :   to move the text one notch to the right and show you\'re responding to a message.`

`  `<b>`Sign`</b>` messages with ~~~~ to leave your username on your reply--or use the `[<File:Insert-signature.png>](https://ko.wikipedia.org/wiki/File:Insert-signature.png "fig:File:Insert-signature.png")` signature button.  We only sign Talk pages, not Article pages.`

<b>`Notify`</b>` Will that you replied by typing his name somewhere in your reply like [[User:WillKomen|User:WillKomen]].  If you\'re on Will\'s user talk page, it will notify him automatically.',`
`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=6&action=edit'          `
`               } , {`
`                       name: 'Got it',`
`                       action: 'next'`
`               } ],`
`               allowAutomaticOkay: false,`
`               `

} , {

`               //8`
`               title: 'Edit summary and Save',`
`               description: '`
`Add an edit summary, something like: "Thanks for the warm welcome".`

`Then SAVE when you\'re ready.`

`',`
`               attachTo: '#wpSave',`
`               position: 'bottomRight',`
`               autoFocus: 'yes',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=7&action=edit'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.isPostEdit();`
`               },`
`               buttons: postEditButtons`

} , {

`               //9`
`               title: 'Indented, signed, and notified!',`
`               description: 'NEW TOOL EARNED:  `<b>`Communicator Badge`</b>

<center>

[TWA_badge_3.png](https://ko.wikipedia.org/wiki/File:TWA_badge_3.png "fig:TWA_badge_3.png")

</center>


',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=8&action=edit'          `
`               } , {`
`                       name: 'Keep on talking*',`
`                       onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User:' + mw.config.get( 'wgUserName' ), 'Wikipedia:TWA/Badge/3template2' , mw.util.getUrl( 'Wikipedia:TWA/2/Start' ) + '?tour=twa2&step=10'); } `
`               } ],`
`              allowAutomaticOkay: false`
`       `

} , {

`               //10`
`               title: 'Communication power!',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

Hey, what if you\\'re having lots of conversations at once? How can you keep track of them all?

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=9'          `
`               } , {`
`                       name: 'A good problem to have...',`
`                       action: 'next'`
`              } ],`

}, {

`               //11`
`               title: 'A solution',`
`               description: '`
`The Watchlist. Your very own feed of changes to the articles and pages you choose to follow.`

`To follow a page just click the `[<File:Vector_skin_-_page_not_in_the_watchlist.png>](https://ko.wikipedia.org/wiki/File:Vector_skin_-_page_not_in_the_watchlist.png "fig:File:Vector_skin_-_page_not_in_the_watchlist.png")` star at the top center of it.  When it turns`[<File:Vector_skin_-_page_in_the_watchlist.png>](https://ko.wikipedia.org/wiki/File:Vector_skin_-_page_in_the_watchlist.png "fig:File:Vector_skin_-_page_in_the_watchlist.png")` blue, you\'re following! (You can also set your Preferences to automatically follow any page you edit).`

`Click WATCHLIST.',`
`               attachTo: '#pt-watchlist',`
`               position: 'bottom', `
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=10'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.isPage( 'Special:Watchlist' );`
`               }`
`               `

} , {

`               //12`
`               title: 'Check out your watchlist',`
`               description: '`

<div align="left">

[TWA_guide_left_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_left_top.png "fig:TWA_guide_left_top.png")

</div>

A <i>very</i> neat part about Wikipedia is that every single edit is recorded. This lets people check out each other\\'s work, because we\\'re at our best when we have help.

',

`               onShow: gt.parseDescription,`
`               attachTo: '#content.mw-body',`
`               position: 'bottom',`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=11'          `
`               } , {`
`                       name: 'Our Motto',`
`                       action: 'next'`
`              } ],`

} , {

`               //13`
`               title: 'Be Bold',`
`               description: 'It\'s also really difficult to mess anything up here, because you can always just switch back to an older version of a page.`

`Kind of a relief, right?`

` That\'s why our motto on Wikipedia is to `<b>`Be Bold!`</b>

`',`
`               onShow: gt.parseDescription,`
`               overlay: true,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:Watchlist' ) + '?tour=twa2&step=12'          `
`               } , {`
`                       name: 'Beyond the watchlist',`
`                       action: 'next'`
`              } ],`

} , {

`               //14`
`               title: 'Track your contributions',`
`               description: '`
`In addition to tracking changes on all the pages you follow on your watchlist, you can also keep track of just your edits.`

`Click CONTRIBUTIONS.',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#pt-mycontris',`
`               position: 'bottomLeft',`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:Watchlist' ) + '?tour=twa2&step=13'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.isPage( 'Special:Contributions/' + mw.config.get( 'wgUserName' ).replace(/ /g, '_') );`
`               }`

} , {

`               //15`
`               title: 'All your work',`
`               description: '`
`Here are your contributions so far.  They\'re all to your userpage and Talk page...`

`Let\'s see if we can do something about that.`

`Oh, wait a second, it looks like you have a new message.`

`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:Watchlist' ) + '?tour=twa2&step=14'          `
`               } , {`
`                       name: 'Check your new message*',`
`                       onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User talk:' + mw.config.get( 'wgUserName' ) + '/TWA', 'Wikipedia:TWA/MyTalk/2' , mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=16'); }`
`               } ],       `
`               allowAutomaticOkay: false`

} , {

`               //16`
`               title: 'An invitation',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

Neat, something to work on...

',

`               onShow: gt.parseDescription,`
`               attachTo: '#content.mw-body',`
`               position: 'bottom',`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ('Special:Contributions/' ) + mw.config.get( 'wgUserName' ) + '?tour=twa2&step=15'          `
`               } , {`
`                        name: 'Reply to GaiaGirl',`
`                        action: 'externalLink',`
`                        url: mw.util.getUrl( 'Wikipedia:TWA/2/Gaia' ) + '?tour=twa2&step=17'`
`               } ],`
`               allowAutomaticOkay: false               `

`       },  {`
`               //17`
`               title: 'Challenge yourself BELOW...',`
`               description: 'Hint: you can learn as much from getting it wrong as getting it right.  And you can always try again!',`
`               attachTo:'#contentSub',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false, `
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=16'          `
`               } ],`
`               `
`       },  {`
`               //18`
`               title: 'Reply',`
`               description: '`
`Click EDIT SOURCE so you can leave your reply to GaiaGirl`

`',`
`               attachTo: '#ca-edit',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Wikipedia:TWA/2/Gaia' ) + '?tour=twa2&step=17'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.hasQuery( { action: 'edit' } );`
`               }`
`               `
`       },  {`
`               //19`
`               title: 'Write your message',`
`               description: '`
`Copy your reply into the text box at the bottom underneath GaiaGirl\'s message.`

`:Awesome [[User:GaiaGirl86|User:GaiaGirl86]], it\'s my favorite planet! How do I get there? ~~~~`
`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=18'          `
`               } , {`
`                       name: 'Copied',`
`                       action: 'next'`
`               } ],`
`               allowAutomaticOkay: false`

}, {

`               //20`
`               title: 'Edit summary and Save',`
`               description: '`
`Just add an edit summary.  How about, "I\'d love to help".`

`Then SAVE when you\'re ready.`

`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#wpSave',`
`               position:  'bottomRight',`
`               autoFocus: 'yes',`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=19&action=edit'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.isPostEdit();`
`               },`
`               buttons: postEditButtons`

} , {

`               //21`
`               title: 'Tic, toc, tic, toc',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

Hey, let\\'s reload the page to see if GaiaGirl responded\!',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=20&action=edit'          `
`               } , {`
`                        name: 'Spin Earth around*',`
`                        onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User talk:' + mw.config.get( 'wgUserName' ) + '/TWA', 'Wikipedia:TWA/MyTalk/3' , mw.util.getUrl( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=22'); }`
`               } ],`

} , {

`               //22`
`               title: 'Directions?',`
`               description: '`

<div align="right">

[TWA_guide_right_top.png](https://ko.wikipedia.org/wiki/File:TWA_guide_right_top.png "fig:TWA_guide_right_top.png")

</div>

I\\'ll take you there. Follow me to EARTH.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#content.mw-body',`
`               position: 'bottom',`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<big>`←`</big>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl ( 'Special:MyTalk/TWA' ) + '?tour=twa2&step=21'          `
`               } , {`
`                        name: 'Head to Earth',`
`                        action: 'externalLink',`
`                        url: mw.util.getUrl( 'Wikipedia:TWA/2/End' ) + '?tour=twa2&step=23'`
`               } ],`

} , {

`               //23`
`               title: 'You\'ve reached the end of mission 2!',`
`               description: '`
[<File:Ringtone>`   ``(3).ogg`](https://ko.wikipedia.org/wiki/File:Ringtone_\(3\).ogg "fig:File:Ringtone (3).ogg")
<b>`Journey on to mission 3...`</b>`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: 'Congrats me!',`
`                       action: 'end'`
`               } ],`

}\]

} );

} (window, document, jQuery, mediaWiki, mediaWiki.guidedTour ) ) ;