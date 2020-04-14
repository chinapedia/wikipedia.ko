> This article is converted from Wikipedia: [미디어위키:Gadget-editsummary.js](https://ko.wikipedia.org/wiki/미디어위키:Gadget-editsummary.js).


/\*\*\*

`* 편집요약 상용구`
`* `
`* 설명:`
`*  편집 요약 입력란 아래에, 클릭하면 요약에 정해진 문구를 입력하는 버튼을 추가`
`* `
`* 환경설정용 변수:`
`*  window.esSummaries: object, 추가될 버튼 혹은 텍스트`
`***/`

// 주 함수: 페이지 로드 완료 시 버튼 생성 function esEditSummary() {

`   // 편집 화면(미리보기 포함)이면서 새 주제 덧붙이기가 아닌 경우`
`   // (#wpSummary가 제목으로 사용되는 경우)에만 동작`
`   // 요약창이 없는 경우에는 미동작`
`   if (($.inArray( mw.config.get('wgAction'), ['edit', 'submit']) !== -1) &&`
`       editform.wpSection.value !== 'new' && $('#wpSummary').length !== 0) {`
`       // esCanBeMinor: esInsSummary 함수에서 사용`
`       window.esCanBeMinor = 1;`
`       `
`       // 레거시`
`       if (typeof window.esSummaries === 'undefined' && typeof esEditSummaries === 'object') {`
`           window.esSummaries = esEditSummaries;`
`       }`
`       `
`       // 컨테이너`
`       $('#wpSummaryLabel').after($('`

<div>

</div>

').attr('id', 'esBtns'));

`       // 레이블 추가`
`       var label = $('`<span></span>`');`
`       label.addClass('esLabel');`
`       label.text('편집요약 상용구: ');`
`       $("#esBtns").prepend(label);`
`       $("#esBtns").append($('`
`'));`
`       `
`       // 요약 비우기 버튼 추가`
`       var clrBtn = $("`<span></span>`").attr('title', '편집 요약 비우기');`
`       clrBtn.addClass('esClrBtn');`
`       clrBtn.text('❌');`
`       clrBtn.click(function () {`
`           $('#wpMinoredit').prop('checked', mw.user.options.get('minordefault'));`
`           $('#wpSummary')[0].value = '';`
`           window.esCanBeMinor = 1;`
`       });`
`       $("#esBtns").append(clrBtn);`
`       `
`       // 설정 배열의 각 요소에 대해 버튼 추가 함수 실행`
`       for (var id in window.esSummaries) {`
`           esAppendBtn(id);`
`       }`
`   }`

}

// 버튼 추가 함수 function esAppendBtn(id) {

`   if (typeof window.esSummaries[id] === 'object') {`
`       var btn = $("`<span></span>`").attr({`
`           'class': 'esBtn',`
`           'title': window.esSummaries[id][2]});`
`       btn.text(window.esSummaries[id][0]);`
`       btn.click(function () {esInsSummary(window.esSummaries[id][1],`
`            window.esSummaries[id][3], window.esSummaries[id][4])});`
`       $("#esBtns").append(btn);`
`   }`
`   // 줄바꿈 및 소제목`
`   else if (typeof window.esSummaries[id] === 'string') {`
`       if (window.esSummaries[id] === 'br') {`
`           $('#esBtns').append($('`
`'));`
`       }`
`       else {`
`       var sTitle = $("`<span></span>`").attr({`
`           'class': 'esSTitle'});`
`       sTitle.text(window.esSummaries[id]);`
`       $('#esBtns').append(sTitle);`
`       }`
`   }`

}

// 편집 요약 수정 함수: 버튼이 눌리면 동작 function esInsSummary(text, isMinor, clear) {

`   var wpSummary = $('#wpSummary')[0];`
`   // 사소한 편집 여부 체크박스 조작`
`   if (typeof isMinor !== 'undefined') {`
`       // 사소한 편집이 명시적으로 아닌 요약이 한 번이라도 추가되면`
`       // 다른 요약 버튼에 의해 사소한 편집이 체크되지 않음`
`       if (isMinor === 0 ) window.esCanBeMinor = 0;`
`       $('#wpMinoredit').prop('checked', (window.esCanBeMinor && isMinor));`
`   }`
`   `
`   if (typeof clear === 'undefined') clear = 0;`
`   `
`   // 요약 비우기`
`   if (clear) wpSummary.value = text;`
`   // 요약 덧붙이기`
`   else if (wpSummary.value.indexOf(text) === -1) {`
`       if (wpSummary.value.match(/[^,; \/]$/)) wpSummary.value += ', ';`
`       wpSummary.value = wpSummary.value.replace(/\s+$/, " ") + text;`
`   }`

}

jQuery( document ).ready(esEditSummary);