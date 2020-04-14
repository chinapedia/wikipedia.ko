> This article is converted from Wikipedia: [미디어위키:Gadget-noSignAlert.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-noSignAlert.js).


/\*\*\*

`* 서명 누락 경고 스크립트`
`* `
`* 설명:`
`*  정해진 문서에서 편집창에 서명(물결표 넷)이 입력되지 않았을 경우,`
`*  변경사항 게시 버튼을 눌렀을 때 서명 누락을 사용자에게 경고`
`* `
`* 사용자 설정:`
`*  window.nsaIgnoreNoTime: boolean, 물결표 셋만 입력한 경우(=시간을 자동`
`*  입력하지 않는 경우)에 경고하지 않음`
`*  window.nsaNoAlertMinor: boolean, “사소한 편집”이 체크되면 경고하지 않음`

  -   - /

function noSignAlert() {

//동작할 문서 지정 //wgNamespaceNumber: RegExp //RegExp가 ''이면 해당 이름공간에서는 항상 동작 var nsaTitleList = {

`   4: '^(사랑방 \`\((일반|기술|정책)\\)`/|삭제 토론/|' + `
`       '문서 관리 요청/|문서 이동 요청/|사용자 관리 요청/|' + `
`       '사용자 권한 신청/|계정 이름 변경 요청|봇/|봇 편집 요청/|' +`
`       '관리자 알림판|질문방/|방명록|함께 검토하기|' +`
`       '위키프로젝트/제안|중재 요청/|의견 요청/|편집 필터/오동작|' +`
`       '관리자 선거/|사무장 선거/|검사관 선거/|중재위원회 선거/|' +`
`       '관리자 권한 회수/|파일 업로드 요청|다중 계정 검사 요청|' +`
`       '알찬 글 후보/|좋은 글 후보/|알찬 목록 후보/)',`
`   102: '^(위키백과 토막글/제안)'`

};

var wgNamespaceNumber = mw.config.get('wgNamespaceNumber'); var wgTitle = mw.config.get('wgTitle'); var wpSave = document.getElementById('wpSave');

if (\!wpSave) return;

//토론 문서에서는 무조건 동작 if (wgNamespaceNumber % 2 \!== 1) {

`   //토론이 아닌 경우`
`   //nsaTitleList[wgNamespaceNumber] === undefined 인 경우 항상`
`   // !wgTitle.match(nsaTitleList[wgNamespaceNumber]) === false`
`   if (typeof nsaTitleList[wgNamespaceNumber] == 'undefined' ||`
`       !wgTitle.match(nsaTitleList[wgNamespaceNumber])) return;`

}

`   //서명 안 했을 때 경고`

wpSave.onclick = function(){

`   var wpTextbox1val = document.editform.wpTextbox1.value;`
`   var minor = false;`
`   if ( typeof $('#wpMinoredit')[0] === 'object' ) {`
`       minor = $('#wpMinoredit')[0].checked;`
`   }`
`   if ( minor && window.nsaNoAlertMinor )`
`       return;`
`   else if (wpTextbox1val.indexOf('~~\~~') < 0 && wpTextbox1val.indexOf('~\~~') >= 0 && !window.nsaIgnoreNoTime )`
`       return confirm('서명에 시각이 입력되지 않았습니다. 이대로 저장하시겠습니까?');`
`   else if (wpTextbox1val.indexOf('~\~~') < 0 )`
`       return confirm('서명을 하지 않았습니다. 이대로 저장하시겠습니까?');`
`   else`
`       return;`
`   };`

}

jQuery( document ).ready( function( $ ) {

`   if ($.inArray( mw.config.get('wgAction'), ['edit', 'submit']) !== -1) {`
`       noSignAlert();`
`   }`

});