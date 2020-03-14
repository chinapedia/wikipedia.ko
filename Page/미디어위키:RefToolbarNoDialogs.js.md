> This article is converted from Wikipedia: [:RefToolbarNoDialogs.js](https://ko.wikipedia.org/wiki/:RefToolbarNoDialogs.js).


var numforms = 0; var wikEdAutoUpdateUrl; function refbuttons() {

` if (mw.toolbar && (document.getElementById('toolbar') || document.getElementById('wikiEditor-section-main'))/* && wikEdAutoUpdateUrl == null*/) {`
`   if (document.getElementById('toolbar')) {`
`     button = document.createElement('a');`
`     button.href = "`<javascript:easyCiteMain>`()";`
`     button.title = "인용";`
`     buttonimage = document.createElement('img');`
`     buttonimage.src = "//upload.wikimedia.org/wikipedia/commons/0/00/Button_easy_cite_%281%29.png";`
`     buttonimage.alt = "Insert footnote";`
`     button.appendChild(buttonimage);`
`     document.getElementById('toolbar').appendChild(button);`
`   } else {`
`     button = document.createElement('a');`
`     button.href = "#";`
`     button.title = "인용";`
`     button.id = 'reftoolbar-button';`
`     buttonimage = document.createElement('img');`
`     buttonimage.src = "//upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Curly_Brackets.svg/22px-Curly_Brackets.svg.png";`
`     buttonimage.alt = "인용";`
`     button.classname = "tool tool-button";`
`     buttonimage.style.width = "22px";`
`     buttonimage.style.height = "17px";`
`     buttonimage.style.paddingTop = "5px";`
`     buttonimage.style.paddingLeft = "3px";`
`     button.appendChild(buttonimage);`
`     document.getElementById('wikiEditor-ui-toolbar').childNodes[0].childNodes[1].appendChild(button);`
`     $('#wikiEditor-section-main .group-insert').append( button );`
`     $(button).click( function() { easyCiteMain(); });`
`   }`
`   if (navigator.userAgent.indexOf('MSIE') == -1) {`
`     citemain = document.createElement('div');`
`     citemain.style.display = 'none';`
`     citemain.setAttribute('Id', 'citeselect');`
`     citemain.appendChild( addOption("citeWeb()", "웹 인용") );`
`     citemain.appendChild( addOption("citeBook()", "서적 인용") );`
`     citemain.appendChild( addOption("citeJournal()", "저널 인용") );`
`     citemain.appendChild( addOption("citeNews()", "뉴스 인용") );`
`     citemain.appendChild( addOption("citeNamedRef()", "이름이 지정된 각주") );`
`     citemain.appendChild( addOption("dispErrors()", "오류 검사") );`
`     citemain.appendChild( addOption("hideInitial()", "취소") );`
`     document.getElementById('wpTextbox1').parentNode.insertBefore(citemain, document.getElementById('wpTextbox1'));`
`   }`
`   else {`
`   selection = '`

<div id="citeselect" style="display:none">

<input type="button" value="웹 인용" onclick="citeWeb()" />'+

`     '`<input type="button" value="서적 인용" onclick="citeBook()" />`'+`
`     '`<input type="button" value="저널 인용" onclick="citeJournal()" />`'+`
`     '`<input type="button" value="뉴스 인용" onclick="citeNews()" />`'+`
`     '`<input type="button" value="이름이 지정된 각주" onclick="citeNamedRef()" />`'+`
`     '`<input type="button" value="오류 검사" onclick="dispErrors()" />`'+`
`     '`<input type="button" value="취소" onclick="hideInitial()" />

</div>

';

`   document.getElementById('editform').innerHTML = selection + document.getElementById('editform').innerHTML;`
`   }`
` }`

}

function addOption(script, text) {

` option = document.createElement('input');`
` option.setAttribute('type', 'button');`
` option.setAttribute('onclick', script);`
` option.setAttribute("value", text);`
` return option;`

}

function hideInitial() {

` document.getElementById('citeselect').style.display = 'none';`
` oldFormHide();`

}

function oldFormHide() {

` if (numforms != 0) {`
`   document.getElementById('citediv'+numforms).style.display = 'none';`
` }`
` if (document.getElementById('errorform') != null) {`
`   document.getElementById('citeselect').removeChild(document.getElementById('errorform'));`
` }`

}

function easyCiteMain() {

` document.getElementById('citeselect').style.display = '';`

}

var months = \['January', 'February', 'March', 'April', 'May', 'June',

` 'July', 'August', 'September', 'October', 'November', 'December'];`

var citeGlobalDateFormat = "<year>-<zmonth>-<zdate>"; function getTime() {

` var datestr = '';`
` if (typeof citeUserDateFormat != 'undefined') {`
`   datestr = citeUserDateFormat;`
` } else {`
`   datestr = citeGlobalDateFormat;`
` }`
` var DT = new Date();`
` var zmonth = '';`
` var month = DT.getMonth()+1;`
` if (month < 10) {`
`   zmonth = "0"+month.toString();`
` } else {`
`   zmonth = month.toString();`
` }`
` month = month.toString();`
` var zdate = '';`
` var date = DT.getDate()`
` if (date < 10) {`
`   zdate = "0"+date.toString();`
` } else {`
`   zdate = date.toString();`
` }`
` date = date.toString()`
` datestr = datestr.replace('`<date>`', date);`
` datestr = datestr.replace('`<month>`', month);`
` datestr = datestr.replace('`<zdate>`', zdate);`
` datestr = datestr.replace('`<zmonth>`', zmonth);`
` datestr = datestr.replace('`<monthname>`', months[DT.getMonth()]);`
` datestr = datestr.replace('`<year>`', DT.getFullYear().toString());`
` return (datestr);`

}

function citeWeb() {

` citeNewsWeb("웹 인용");`

} function citeNews() {

` citeNewsWeb("뉴스 인용");`

}

function citeNewsWeb(templatename) {

` oldFormHide();`
` template = templatename;`
` var legend;`
` if (template == "웹 인용") {`
`   legend = "웹 인용 자료";`
` } else {`
`   legend = "뉴스 인용 자료";`
` }`
` newtime = getTime();`
` numforms++;`
` form = '`

<div id="citediv'+numforms+'">

'+

`   '`

<fieldset>

<legend>'+legend+'</legend>'+

`   '`

<table cellspacing="5">

'+

`   '`<input type="hidden" value="'+template+'" id="template">`'+`
`   '`

<tr>

<td width="120">

<label for="url"> URL: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="url">

</td>

'+

`   '`

<td width="120">

<label for="title"> 제목: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="제목">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="last"> 성: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="성">

</td>

'+

`   '`

<td width="120">

<label for="first"> 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="이름">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="author"> 저자: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="저자">

</td>

'+

`   '`

<td width="120">

<label for="date"> 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="날짜">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="work"> 작품: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="작품">

</td>

'+

`   '`

<td width="120">

<label for="publisher"> 출판사: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="출판사">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="pages"> 쪽: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="쪽">

</td>

'+

`   '`

<td width="120">

<label for="language"> 언어: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="언어">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="accessdate"> 확인 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="확인날짜" value="'+ newtime +'">

</td>

'+

`   '`

<td width="120">

<label for="location"> 위치: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="위치">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="refname"> 각주 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="refname">

</td>

</tr>

'+

`   '`

</table>

'+

`   '`<input type="button" value="인용 넣기" onClick="addcites()">`'+`
`'`

</fieldset>

</div>

';

`  document.getElementById('citeselect').innerHTML += form;`

}

function citeBook() {

` oldFormHide();`
` template = "서적 인용";`
` numforms++;`
` form = '`

<div id="citediv'+numforms+'">

'+

`   '`

<fieldset>

<legend>서적 인용 자료</legend>'+

`   '`

<table cellspacing="5">

'+

`   '`<input type="hidden" value="'+template+'" id="template">`'+`
`   '`

<tr>

<td width="120">

<label for="last"> 성: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="성">

</td>

'+

`   '`

<td width="120">

<label for="first"> 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="이름">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="author"> 저자: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="저자">

</td>

'+

`   '`

<td width="120">

<label for="others"> 기타: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="기타">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="title"> 제목: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="제목">

</td>

'+

`   '`

<td width="120">

<label for="editor"> 편집자: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="편집자">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="publisher"> 출판사: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="출판사">

</td>

'+

`   '`

<td width="120">

<label for="location"> 위치: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="위치">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="date"> 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="날짜">

</td>

'+

`   '`

<td width="120">

<label for="edition"> 판: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="판">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="series"> 총서: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="총서">

</td>

'+

`   '`

<td width="120">

<label for="volume"> 권: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="권">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="pages"> 쪽: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="쪽">

</td>

'+

`   '`

<td width="120">

<label for="chapter"> 장: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="장">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="isbn"> ISBN: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="isbn">

</td>

'+

`   '`

<td width="120">

<label for="oclc"> OCLC: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="oclc">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="url"> URL: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="url">

</td>

'+

`   '`

<td width="120">

<label for="accessdate"> 확인 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="확인날짜">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="language"> 언어: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="언어">

</td>

'+

`   '`

<td width="120">

<label for="refname"> 각주 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="refname">

</td>

</tr>

'+

`   '`

</table>

'+

`   '`<input type="button" value="인용 추가" onClick="addcites()">`'+`
`'`

</fieldset>

</div>

';

`  document.getElementById('citeselect').innerHTML += form;`

}

function citeJournal() {

` oldFormHide();`
` template = "저널 인용";`
` numforms++;`
` form = '`

<div id="citediv'+numforms+'">

'+

`   '`

<fieldset>

<legend>저널 인용 자료</legend>'+

`   '`

<table cellspacing="5">

'+

`   '`<input type="hidden" value="'+template+'" id="template">`'+`
`   '`

<tr>

<td width="120">

<label for="last"> 성: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="성">

</td>

'+

`   '`

<td width="120">

<label for="first"> 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="이름">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="author"> 저자: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="저자">

</td>

'+

`   '`

<td width="120">

<label for="date"> 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="날짜">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="title"> 제목: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="제목">

</td>

'+

`   '`

<td width="120">

<label for="journal"> 저널: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="저널">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="publisher"> 출판사: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="출판사">

</td>

'+

`   '`

<td width="120">

<label for="location"> 위치: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="위치">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="volume"> 권: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="권">

</td>

'+

`   '`

<td width="120">

<label for="issue"> 호: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="호">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="pages"> 쪽: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="쪽">

</td>

'+

`   '`

<td width="120">

<label for="issn"> ISSN: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="issn">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="oclc"> OCLC: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="oclc">

</td>

'+

`   '`

<td width="120">

<label for="language"> 언어: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="언어">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="url"> URL: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="url">

</td>

'+

`   '`

<td width="120">

<label for="accessdate"> 확인 날짜: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="확인날짜">

</td>

</tr>

'+

`   '`

<tr>

<td width="120">

<label for="refname"> 각주 이름: </label>

</td>

'+

`     '`

<td width="400">

<input type="text" tabindex=1 style="width:100%" id="refname">

</td>

</tr>

'+

`   '`

</table>

'+

`   '`<input type="button" value="인용 추가" onClick="addcites()">`'+`
`'`

</fieldset>

</div>

';

`  document.getElementById('citeselect').innerHTML += form;`

}

function addcites(template) {

` cites = document.getElementById('citediv'+numforms).getElementsByTagName('input');`
` var citebegin = '<ref';`
` var citename = '';`
` var citeinner = '';`
` for (var i=0; i<cites.length-1; i++) {`
`   if (cites[i].value != '' && cites[i].id != "refname" && cites[i].id != "template") {`
`     citeinner += "|" + cites[i].id + "=" + cites[i].value;`
`   }`
`   else if (cites[i].value != '' && cites[i].id == "refname" && cites[i].id != "template") {`
`     citebegin += ' name="' + cites[i].value + '"';`
`   }`
`   else if (cites[i].value != '' && cites[i].id != "refname" && cites[i].id == "template") {`
`     citename = '>{{' + cites[i].value;`
`   }`
` }`
` cite = citebegin + citename + citeinner + "}}`</ref>`";`
` $("#wpTextbox1").focus();`
` insertTags(cite, '', '');`
` document.getElementById('citediv'+numforms).style.display = 'none';`

}

function getNamedRefs(calls) {

` if (typeof(wikEdUseWikEd) != 'undefined') {`
`   if (wikEdUseWikEd == true) {`
`     WikEdUpdateTextarea();`
`   }`
` }`
` text = document.getElementById('wpTextbox1').value;`
` var regex;`
` if (calls) {`
`   regex = /< *?ref +?name *?= *?(('([^']*?)')|("([^"]*?)")|([^'"\s]*?[^\/]\b)) *?\/ *?>/gi //'`
` } else {`
`   regex = /< *?ref +?name *?= *?(('([^']*?)')|("([^"]*?)")|([^'"\s]*?[^\/]\b)) *?>/gi //'`
` }`
` var namedrefs = [];`
` var i=0;`
` var nr=true;`
` do {`
`   ref = regex.exec(text);`
`   if(ref != null){`
`     if (ref[5]) {`
`       namedrefs[i] = ref[5];`
`     } else if (ref[3]) {`
`       namedrefs[i] = ref[3];`
`     } else {`
`       namedrefs[i] = ref[6];`
`     }`
`     i++;`
`   } else {`
`     nr=false;`
`   }`
` } while (nr==true);`
` return namedrefs;`

}

function citeNamedRef() {

` namedrefs = getNamedRefs(false);`
` if (namedrefs == '') {`
`   oldFormHide();`
`   numforms++;`
`   out = '`

<div id="citediv'+numforms+'">

<fieldset>

'+

`     '`<legend>`본문 내 각주`</legend>`문서 내에 이름이 지정된 각주(`<ref name="이름">`)가 없습니다.`

</fieldset>

</div>

';

`   document.getElementById('citeselect').innerHTML += out;`
` }`
` else {`
`   oldFormHide();`
`   numforms++;`
`   form = '`

<div id="citediv'+numforms+'">

'+

`     '`

<fieldset>

<legend>문서 내 각주</legend>'+

`     '`

<table cellspacing="5">

'+

`     '`

<tr>

<td>

<label for="namedrefs"> 이름이 지정된 각주 목록</label>

</td>

'+

`           '`

<td>

<select name="namedrefs" id="namedrefs">';

`   for (var i=0;i<namedrefs.length;i++) {`
`     form+= '`<option value="'+namedrefs[i]+'">`'+namedrefs[i]+'`</option>`';`
`   }`
`   form+= '`</select>`'+`
`     '`

</td>

</tr>

</table>

'+

`     '`<input type="button" value="인용 추가" onClick="addnamedcite()">`'+`
`     '`

</fieldset>

</div>

';

`    document.getElementById('citeselect').innerHTML += form;`
` }`

}

function addnamedcite() {

` name = document.getElementById('citediv'+numforms).getElementsByTagName('select')[0].value;`
` ref = '`\[1\]`';`
` $("#wpTextbox1").focus();`
` insertTags(ref, '', '');`
` document.getElementById('citediv'+numforms).style.display = 'none';`

}

function getAllRefs() {

` if (typeof(wikEdUseWikEd) != 'undefined') {`
`   if (wikEdUseWikEd == true) {`
`     WikEdUpdateTextarea();`
`   }`
` }`
` text = document.getElementById('wpTextbox1').value;`
` regex = /< *?ref( +?name *?= *?(('([^']*?)')|("([^"]*?)")|([^'"\s]*?[^\/]\b)))? *?>((.|\n)*?)< *?\/? *?ref *?>/gim //"`
` var allrefs = [];`
` var i=0;`
` var nr=true;`
` do {`
`   ref = regex.exec(text);`
`   if(ref != null){`
`     if (ref[0].search(/[^\s]{150}/) != -1) {`
`       ref[0] = ref[0].replace(/\|([^\s])/g, "| $1");`
`     }`
`     ref[0] = ref[0].replace(/</g, "<");`
`     ref[0] = ref[0].replace(/>/g, ">");`
`     allrefs[i] = ref[0];`
`     i++;`
`   } else {`
`     nr=false;`
`   }`
` } while (nr==true);`
` return allrefs;`

}

function NRcallError(namedrefs, refname) {

` for (var i=0; i<namedrefs.length; i++) {`
`   if (namedrefs[i] == refname) {`
`     return true;`
`   }`
` }`
` return false;`

}

function errorCheck() {

` var allrefs = getAllRefs();`
` var allrefscontent = [];`
` var samecontentexclude = [];`
` var sx=0;`
` var templateexclude = [];`
` var tx=0;`
` var skipcheck = false;`
` var namedrefcalls = getNamedRefs(true);`
` for (var i=0; i<allrefs.length; i++) {`
`   allrefscontent[i] = allrefs[i].replace(/< *?ref( +?name *?= *?(('([^']*?)')|("([^"]*?)")|([^'"\s]*?[^\/]\b)))? *?>((.|\n)*?)< *?\/? *?ref *?>/gim, "$8");  //"`
` }`
` var namedrefs = getNamedRefs(false);`
` var errorlist = [];`
` var q=0;`
` unclosed = document.getElementById('unclosed').checked;`
` samecontent = document.getElementById('samecontent').checked;`
` templates = document.getElementById('templates').checked;`
` repeated = document.getElementById('repeated').checked;`
` undef = document.getElementById('undef').checked;`
` for (var i=0; i<allrefs.length; i++) {`
`   if (allrefs[i].search(/< *?\/ *?ref *?>/) == -1 && unclosed) {`
`     errorlist[q] = '`

<tr>

<td width="75%">

`'+allrefs[i]+'`

</td>

';

`     errorlist[q] += '`

<td width="25%">

닫히지 않은 <ref> 태그

</td>

</tr>

';

`     q++;`
`   }`
`   if (samecontent) {`
`     for (var d=0; d<samecontentexclude.length; d++) {`
`       if (allrefscontent[i] == samecontentexclude[d]) {`
`         skipcheck = true;`
`       }`
`     }`
`     var p=0;`
`     while (p<allrefs.length && !skipcheck) {`
`       if (allrefscontent[i] == allrefscontent[p] && i != p) {`
`         errorlist[q] = '`

<tr>

<td width="75%">

`'+allrefscontent[i]+'`

</td>

';

`         errorlist[q] += '`

<td width="25%">

내용이 똑같은 각주가 있습니다.

</td>

</tr>

';

`         q++;`
`         samecontentexclude[sx] = allrefscontent[i]`
`         sx++;`
`         break;`
`       }`
`       p++;`
`     }`
`    skipcheck=false;`
`   }`
`   if (templates) {`
`     if (allrefscontent[i].search(/\{\{cite/i) == -1 && allrefscontent[i].search(/\{\{citation/i) == -1 && allrefscontent[i].search(/\{\{Comic (book|strip) reference/i) == -1 && allrefscontent[i].search(/\{\{Editorial cartoon reference/i) == -1 && allrefscontent[i].search(/\{\{harv/i) == -1) {`
`       for (var x=0; x<templateexclude.length; x++) {`
`         if (allrefscontent[i] == templateexclude[x]) {`
`           skipcheck = true;`
`         }`
`       }`
`       if (!skipcheck) {`
`         errorlist[q] = '`

<tr>

<td width="75%">

`'+allrefs[i]+'`

</td>

';

`         errorlist[q] += '`

<td width="25%">

인용 틀을 쓰지 않았습니다.

</td>

</tr>

';

`         q++;`
`         templateexclude[tx] = allrefscontent[i];`
`         tx++;`
`       }`
`       skipcheck = false;`
`     }`
`   }`
` }`
` if (repeated) {`
`   var repeatnameexclude = [];`
`   var rx=0;`
`   for (var k=0; k<namedrefs.length; k++) {`
`     for (var d=0; d<repeatnameexclude.length; d++) {`
`       if (namedrefs[k] == repeatnameexclude[d]) {`
`         skipcheck = true;`
`       }`
`     }`
`     var z=0;`
`     while (z<namedrefs.length && !skipcheck) {`
`       if (namedrefs[k] == namedrefs[z] && k != z) {`
`         errorlist[q] = '`

<tr>

<td width="75%">

`'+namedrefs[k]+'`

</td>

';

`         errorlist[q] += '`

<td width="25%">

같은 이름을 사용한 각주가 있습니다.

</td>

</tr>

';

`         q++;`
`         repeatnameexclude[rx] = namedrefs[z];`
`         rx++;`
`         break;`
`       }`
`       z++;`
`     }`
`    skipcheck = false;`
`   }`
` }`
` if (undef) {`
`   var undefexclude = [];`
`   var ux=0;`
`   for (var p=0; p<namedrefcalls.length; p++) {`
`     for (var d=0; d<undefexclude.length; d++) {`
`       if (allrefscontent[i] == undefexclude[d]) {`
`         skipcheck = true;`
`       }`
`     }`
`     if (!skipcheck) {`
`       if (!NRcallError(namedrefs, namedrefcalls[p])) {`
`         errorlist[q] = '`

<tr>

<td width="75%">

`'+namedrefcalls[p]+'`

</td>

';

`         errorlist[q] += '`

<td width="25%">

이름이 지정된 각주가 있지만 내용이 정의되지 않았습니다.

</td>

</tr>

';

`         q++;`
`         undefexclude[ux] = namedrefs[p];`
`         ux++;`
`       }`
`     }`
`     skipcheck = false;`
`   }`
`}`
` if (q > 0) {`
`   return errorlist;`
` } else {`
`   return 0;`
` }`

}

function dispErrors() {

` oldFormHide();`
` form = '`

<div id="errorform">

<fieldset>

'+

`   '`<legend>`오류 검사하기`</legend>`'+`
`   '`<b>`검사할 항목을 선택하세요.`</b>
`'+`
`   '`<input type="checkbox" id="unclosed" />` 닫히지 않은 `<ref>` 태그`
`'+`
`   '`<input type="checkbox" id="samecontent" />` 내용이 같은 각주`
`'+`
`   '`<input type="checkbox" id="templates" />` 인용 틀을 쓰지 않은 각주`
`'+`
`   '`<input type="checkbox" id="repeated" />` 같은 이름을 가진 각주`
`'+`
`   '`<input type="checkbox" id="undef" />` 이름이 있지만 내용이 정의되지 않은 각주`
`'+`
`   '`<input type="button" id="errorchecksubmit" value="선택한 항목에 대해 검사하기" onclick="doErrorCheck()"/>`'+`
`   '`

</fieldset>

</div>

';

` document.getElementById('citeselect').innerHTML += form;`

}

function doErrorCheck() {

` var errors = errorCheck();`
` document.getElementById('citeselect').removeChild(document.getElementById('errorform'));`
` if (errors == 0) {`
`   if (numforms != 0) {`
`     document.getElementById('citediv'+numforms).style.display = 'none';`
`   }`
`   numforms++;`
`   out = '`

<div id="citediv'+numforms+'">

<fieldset>

'+

`     '`<legend>`오류 검사하기`</legend>`발견된 오류가 없습니다.`

</fieldset>

</div>

';

`   document.getElementById('citeselect').innerHTML += out;`
` }`
` else {`
`   if (numforms != 0) {`
`     document.getElementById('citediv'+numforms).style.display = 'none';`
`   }`
`   numforms++;`
`   form = '`

<div id="citediv'+numforms+'">

'+

`     '`

<fieldset>

<legend>오류 검사하기</legend>'+

`     '`

<table border="1px">

';

`   for (var i=0; i<errors.length; i++) {`
`     form+=errors[i];`
`   }`
`   form+= '`

</table>

'+

`     '`

</fieldset>

</div>

';

`    document.getElementById('citeselect').innerHTML += form;`
` }`

}

$( refbuttons );

1.