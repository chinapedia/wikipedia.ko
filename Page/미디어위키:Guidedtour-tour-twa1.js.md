> This article is converted from Wikipedia: [:Guidedtour-tour-twa1.js](https://ko.wikipedia.org/wiki/:Guidedtour-tour-twa1.js).


// The Wikipedia Adventure Mission 1

// Todo list // 한국어 위키백과에 맞도록 페이지 제목을 교정해야 함 // url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1\&step=1' 이런 부분 일괄 치환 필요

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

`       name: 'twa1',`
`       shouldLog: true,`
`       steps: [ {`
`               //1`
`               title: '위키백과에 어서 오세요!',`
`               description: '`

<div align="left">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_left_top.png "wikilink")

</div>

위키백과는 <b>누구나 편집할 수 있는</b> 자유로운 백과사전입니다. 저희 위키를 어떻게 편집하는지 모험 형식으로 친절히 알려 드리겠습니다.
저희는 미션 일곱 개를 준비했으며, 각각의 미션을 수행하실 때마다 위키백과 편집 능력이 눈에 띨 정도로 향상되실 것입니다.

',

`               onShow: gt.parseDescription,`
`               overlay: true,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '준비 완료',`
`                       action: 'next',`
`               } ],`
`               allowAutomaticOkay: false   `

`       },  {`
`               //2`
`               title: '미리 알려드립니다',`
`               description: '`
<b>`나가지 말아주세요 (x)`</b>
` 귀하가 미션을 완료하기 전에 창을 닫아버린다면 미션을 처음부터 다시 실행해야 합니다.`

<b>`자동 메시지`</b>
` 이 게임을 하실 때 파란 버튼에 `<span style="font-size:larger"><b>`*`</b></span>` 표시가 있으면 귀하의 사용자 문서를 편집하는 것입니다`

`',`
`               onShow: gt.parseDescription,`
`               overlay: true,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=1'          `
`               } , {`
`                       name: '따라오세요...',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false       `

`       },  {`
`               //3`
`               title: '왜 위키백과인가요?',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

저희는 정말 멋진 목표가 있습니다.

<b>이 세상에 있는 모든 사람들이 사람들의 지식에 자유롭게 접근할 수 있는 세상을 상상해보세요.</b>

가장 놀라운 것은...

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=2'          `
`               } , {`
`                        name: '지금 일어나고 있는 것',`
`                        action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false               `

`       },  {`
`               //4`
`               title: '지금 일어나고 있는 것',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

위키백과는 매월 5억 명의 사람들이 초당 8000번을 보고 있습니다. 저희는 전 세계에서 다섯 번째로 큰 웹 사이트입니다. 단지 2001년에 시작했을 뿐인데 말이죠\!

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=3'          `
`               } , {`
`                       name: '누가 위키백과를 만드나요?',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false`
`       },  {`
`               //5`
`               title: '누가 위키백과를 만드나요?',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

당신이요. 거의 38만 명에 달하는 등록 사용자가 있습니다.(영어 위키백과는 1900만). 가장 중요한 것은, 전문가만 기여를 할 수 있는 것은 아닙니다. 저희 편집자 대다수는 자원봉사자입니다.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=4'          `
`               } , {`
`                       name: '왜 사람들은 편집할까요?',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false`
`       },  {`

`               //6`
`               title: '특별한 역할을 찾아보세요',`
`               description: '`

<div align="left">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_left_top.png "wikilink")

</div>

위키백과에서 놀라운 부분은 자신만의 길과 목적을 찾아가야 한다는 것입니다. 하지만 개개인이 모이면 큰 변화를 이끌어냅니다. 한 사람의 변화가 세계를 바꿀 수 있습니다.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=5'          `
`               } , {`
`                       name: '준비되셨나요?',`
`                       action: 'next',`
`                        } ],`
`               allowAutomaticOkay: false,`

}, {

`               //7`
`               title: '로그인 또는 계정 만들기',`
`               description: '`

<div align="left">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_left_top.png "wikilink")

</div>

계정을 만들면 좋은 점이 많습니다. 어서 만드세요.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=6'  `
`               } , {`
`                   name: '로그인된 상태',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=8'`
`                       `
`               } , {`
`                   name: '로그인을 해야 함',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:UserLogin' ) + '?tour=twa1&step=7'`
`                    `
`               } , {`
`                   name: '계정 만들기!',`
`                   action: 'externalLink',`
`                   url: mw.config.get('wgServer') + mw.config.get('wgScriptPath') + '/index.php?title=Special:UserLogin&returnto=위키백과:위키백과_대모험&returntoquery=tour%3Dtwa1%26step%3D8%26showGettingStarted%3Dfalse&type=signup'`
`                       `
`               } ],`
`               allowAutomaticOkay: false,`
`               shouldSkip: function () {`
`               return mw.config.get( 'wgUserId' )  !== null;`
`               }`
`               `

} , {

`               //8`
`               title: '위키백과에게 안부 묻기',`
`               description: '`
`  저희 공동체에게 자신을 소개해 봅시다.`

`(나머지 모험을 위해서는 로그인을 해야 합니다)`

`',`
`               overlay: true,`
`               onShow: gt.parseDescription,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=6'          `
`               } , {`
`                        name: '안부 전하기*',`
`                        action: 'externalLink',`
`                        url:  mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=9'`
`                        // onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "로그인을 해 주세요." );   return;   } sendMessage( '사용자토론:' + mw.config.get( 'wgUserName' ), '위키백과:위키백과 대모험' , mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=9'); } `
`               } ],    `
`               allowAutomaticOkay: false`
`               `

} , {

`               //9`
`               title: '사용자 문서',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

사용자 문서는 다른 편집자들에게 자신을 소개하는 공간입니다. 좋아하는 것이나 흥미, 위키백과에 기여하고 싶은 것 등을 공유하는 것입니다.

<i>사용자 문서는 모든 사람들에게 공개되므로 개인 정보를 올리지 마세요.</i>

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '위키백과:위키백과 대모험' ) + '?tour=twa1&step=8'          `
`               } , {`
`                       name: '좋은 사용자 문서는 어떤 것인가요?',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Wikipedia:TWA/1/Bio' ) + '?tour=twa1&step=10'`
`               } ],`
`       allowAutomaticOkay: false`
`       `

} , {

`               //10`
`               //원래는 사용자가 고르도록 되어 있으나 임시적으로 코드 수정`
`               title: '스스로 해야 할 때...',`
`               description: '좋은 사용자 문서는 사생활을 드러내지 않고, 자기 자랑을 하지 않는 것이 좋습니다. 편집과 관련 있는 링크를 모아두거나, 자주 가는 링크를 보관하는 용도로 쓰지요. 무례한 말도 써서는 안 되고요.',`
`               attachTo:'#contentSub',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false, `
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( '특수:내사용자문서' ) + '?tour=twa1&step=9'          `
`                   }, {`
`                       name: '이해했어요',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=11'} ],`
`              `

} , {

`               //11`
`               title: '해 보세요!',`
`               description: '`
`위키백과에 사용자 문서를 만드는 것은 편집하는 것 만큼 쉽습니다. 페이지 위에 있는 `

<b>`원본 만들기`</b>`나 `<b>`원본 편집`</b>`을 클릭하세요. `

`(시각편집기를 사용할 수도 있지만 이 모험은 소스 편집기를 사용합니다.).`

`',`
`               attachTo: '#ca-edit',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=9'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.hasQuery( { action: 'edit' } );`
`               }`

}, {

`               //12`
`               title: '편집 인터페이스',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

여기는 마법이 현실이 되는 곳입니다.

큰 텍스트 상자의 왼쪽 상단에 글을 입력해 보세요. 사용자 이름이나 흥미, 기여하고 싶은 분야 등등을 입력할 수 있습니다. 무엇을 하면 재미가 있을까요? 원하는 만큼 글을 쓸 수 있지만 적어도 편집 하나는 해야 합니다.

사용자 문서가 있으시다면 적어도 <b>한 번</b>은 수정을 해야 합니다.

',

`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=11'          `
`               } , {`
`                       name: '입력했어요',`
`                       action: 'next'`
`              } ],`
`              `

} , {

`               //13`
`               title: '편집 요약과 저장',`
`               description: '`
`잘 하셨어요! 저장 버튼을 누르기 전에, 어떤 편집을 했는지  편집 요약을 남길 필요가 있습니다. 다른 사용자들이 귀하가 어떤 편집을 했는지 알기 쉽게 해 줘요.`

`"자기소개" 같이 어떤 편집을 했는지 써 줍시다.`

`남은 것은 저장하기 뿐. 다 하신 뒤에 저장 버튼을 눌러주세요.`

`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               attachTo:  '#wpSave', `
`               position: 'bottomRight',`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               shouldSkip: function() {`
`                       return gt.isPostEdit();`
`               },`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=12&action=edit'          `
`               } ],`
`               buttons: postEditButtons`

} , {

`               //14`
`               title: 'Congrats!',`
`               description: '새로운 도구 얻음:  `<b>`편집자 뱃지`</b>

<center>

[250px](https://ko.wikipedia.org/wiki/파일:TWA_badge_1.png "wikilink")

</center>


당신은 위키백과 편집자입니다\! 기분이 어떠세요? 자기 소개를 한 것은 훌륭합니다.
',

`               overlay: false,`
`               onShow: gt.parseDescription,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=13&action=edit'          `
`               } , {`
`                       name: '더 좋게 만들어보기*',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=15&action=edit'  `
`                       //onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User:' + mw.config.get( 'wgUserName' ), 'Wikipedia:TWA/Badge/1template2' , mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=15'); } `
`               } ],`

} , {

`               //15`
`               title: '더 잘하기',`
`               description: '`
`되돌아가서 내용을 조금 바꿔보아요. `<b>`원본 편집`</b>`을 눌러주세요.`

`',`
`               overlay: false,`
`               attachTo: '#ca-edit',`
`               position: 'bottom',`
`               onShow: gt.parseDescription,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=14'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.hasQuery( { action: 'edit' } );`
`               }`

} , {

`               //16`
`               title: '글자 굵게 하기',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

텍스트 박스에서, 사용자 이름(또는 다른 문구)를 마우스를 이용해서 블록을 잡아주세요.

그런 다음에 텍스트 상자 위의 편집 툴바에 있는 [파일:Toolbaricon_bold_B-1.png](https://ko.wikipedia.org/wiki/파일:Toolbaricon_bold_B-1.png "wikilink") 버튼을 눌러주세요.

편집 툴바는 글에 효과를 쉽게 넣어 주기 때문에 유용한 도구입니다.',

`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=15'          `
`               } , {`
`                       name: '굵게 만들었습니다',`
`                       action: 'next'`
`               } ],`

} , {

`               //17`
`               title: '기울임체 추가',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

흥미를 마우스로 블록을 잡아 봅시다.

그런 다음에 편집 툴바의 [파일:Toolbaricon_italics_I.png](https://ko.wikipedia.org/wiki/파일:Toolbaricon_italics_I.png "wikilink") 버튼을 눌러 기울임체를 적용해 보아요.

',

`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false   ,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=16&action=edit'          `
`               } , {`
`                       name: '기울임체를 적용했습니다',`
`                       action: 'next'`
`               } ],`

} , {

`               //18`
`               title: '위키링크 추가',`
`               description: '`

<div align="right">

[link=](https://ko.wikipedia.org/wiki/파일:TWA_guide_right_top.png "wikilink")

</div>

위키백과의 다른 페이지로 링크를 걸 수 있습니다. 이것은 웹을 만드는 것에 도움을 주고, 링크를 계속 따라가면서 다른 문서를 볼 수 있게 도와줍니다. ^^

링크를 걸고 싶은 문구를 블록잡아 주세요.

그런 다음에 편집 툴바에 잇는 [파일:Toolbar_Insert_link.png](https://ko.wikipedia.org/wiki/파일:Toolbar_Insert_link.png "wikilink") 버튼을 눌러 주세요.

마지막으로, 링크를 넣어주세요

',

`               attachTo: '#wpTextbox1', `
`               position: 'bottomRight',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=17&action=edit'          `
`               } , {`
`                       name: '위키링크를 걸었습니다',`
`                       action: 'next'`
`               } ],`

} , {

`               //19`
`               title: '편집 요약',`
`               description: '`
`"굵은 글씨, 기울인 글씨, 위키 링크 추가"를 입력하세요.  저장 버튼을 누르면 문서 내용이 바뀝니다.`

`',`
`               attachTo: '#wpSave',`
`               position: 'bottomRight',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               allowAutomaticOkay: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=18&action=edit'          `
`               } ],`
`               shouldSkip: function() {`
`                       return gt.isPostEdit();`
`               },`
`               buttons: postEditButtons`

} , {

`               //20`
`               title: 'You did it :)',`
`               description: '새로운 도구 증정:  `<b>`형식 뱃지`</b>

<center>

[250px](https://ko.wikipedia.org/wiki/파일:TWA_badge_2.png "wikilink")

</center>


빨리 배우시네요. 수고하셨습니다. 막 모험을 시작했을 뿐이지만 앞으로 필요한 기본적인 도구는 이미 익힌 것입니다. 편집 페이지 위아래에 있는 각종 도구를 잘 익혀 두세요. 문서 편집에 도움이 됩니다.
',

`               overlay: true,`
`               onShow: gt.parseDescription,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '`<span style="font-size:larger">`←`</span>`',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=19&action=edit'          `
`               } , {`
`                       name: '다음 단계는 무엇인가요??*',`
`                       action: 'externalLink',`
`                       url: mw.util.getUrl( 'Special:MyPage' ) + '?tour=twa1&step=21&action=edit'  `
`                       // onclick: function()  {  if(!mw.config.get('wgUserName')){  alert( "Please login." );   return;   } sendMessage( 'User:' + mw.config.get( 'wgUserName' ), 'Wikipedia:TWA/Badge/2template2' , mw.util.getUrl( 'Wikipedia:TWA/1/End' ) + '?tour=twa1&step=21'); } `
`               } ],`
`               allowAutomaticOkay: false`

} , {

`               //21`
`               title: '미션 1 성공!',`
`               description: '`
[`파일:Carl``   ``Czerny``   ``-``   ``Duo``   ``Concertante``   ``-``   ``1.``   ``Allegro``   ``(short).ogg`](https://ko.wikipedia.org/wiki/파일:Carl_Czerny_-_Duo_Concertante_-_1._Allegro_\(short\).ogg "wikilink")
<b>`미션 2 수행하기... (준비 중)`</b>`',`
`               onShow: gt.parseDescription,`
`               overlay: false,`
`               closeOnClickOutside: false,`
`               buttons: [ {`
`                       name: '축하합니다!',`
`                       action: 'end'      `
`               } ],`

}\]

} );

} (window, document, jQuery, mediaWiki, mediaWiki.guidedTour ) ) ;