> This article is converted from Wikipedia: [미디어위키:RefToolbarConfig.js](https://ko.wikipedia.org/wiki/미디어위키:RefToolbarConfig.js).


/\* Sitewide options for the the Cite toolbar button:

  - All options should be specified
  -
  - "date format" sets the date format used for the function to insert the current date
  - Current available options:
  - date - the day of the month
  - zdate - day of the month, zero padded to 2 digits
  - monthname - The month name
  - month - The numberic month (1-12)
  - zmonth - numeric month, zero padded to 2 digits
  - year - The full year (4 digits)
  -
  - "autodate fields" is a list of template fields that should have a button to insert the current date
  -
  - "months" is a list of localized month names
  -
  - "modal" - if true, the dialogs will be modal windows, blocking access to the rest of the window.
  - See <http://en.wikipedia.org/wiki/Modal_window>
  - All dialogs in the toolbar are modal by default
  -
  - "autoparse" - if true, previewing a ref will automatically trigger a preview of the parsed wikitext.
  - It is not recommended to set this to true as a global setting as it may slow the script down for
  - people with slow connections.
  -
  - "expandtemplates" - if true, templates and parser functions will be expanded when getting page text
  - (templates inside of ref tags will not be expanded). This will allow references inside of templates or
  - references using {{\#tag:ref}} to be listed in the named refs dialog and searched by error checks.
  - This may slow loading the named refs and error check dialogs.
  - /

CiteTB.Options = { "date format" : "<year>-<zmonth>-<zdate>", "autodate fields" : \['확인날짜'\], // "months" : \['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December'\], "modal" : true, "autoparse" : false, "expandtemplates" : false };

// Cite template definitions new citeTemplate('웹 인용', 'web', \[ // Basic fields {"field": "성<N>", "autofillprop":"last-incr", 'increment_group':'author'}, {"field": "이름<N>", "autofillprop":"first-incr", 'increment_group':'author', 'increment_button':true}, {"field": "제목", "autofillprop":"title"}, {"field": "url"}, {"field": "웹사이트", "autofillprop":"journal"}, {"field": "출판사"}, {"field": "날짜", "autofillprop":"date"}, {"field": "확인날짜"}, {"field": "ref", "tooltip":"cite-ref-tooltip"}, {"field": "인용문"} \], \[ // Expanded fields {"field": "저자<N>", 'increment_group':'author_alt', 'increment_button':true}, {"field": "저자링크<N>", "tooltip":"cite-authorlink-tooltip", 'increment_group':'authorlink', 'increment_button':true}, {"field": "보존url"}, {"field": "보존날짜"}, {"field": "위치"}, {"field": "쪽", "tooltip":"cite-page-tooltip"}, {"field": "언어"}, {"field": "형식"}, {"field": "doi", "autofillid":"doi"} \]);

new citeTemplate('뉴스 인용', 'news', \[ // Basic fields {"field": "성<N>", "autofillprop":"last-incr", 'increment_group':'author'}, {"field": "이름<N>", "autofillprop":"first-incr", 'increment_group':'author', 'increment_button':true}, {"field": "제목", "autofillprop":"title"}, {"field": "url"}, {"field": "날짜", "autofillprop":"date"}, {"field": "확인날짜"}, {"field": "뉴스", "tooltip":"cite-work-tooltip", "autofillprop":"journal"}, {"field": "호"}, {"field": "출판사"}, {"field": "ref", "tooltip":"cite-ref-tooltip"} \], \[ // Expanded fields {"field": "저자<N>", 'increment_group':'author_alt', 'increment_button':true}, {"field": "저자링크<N>", "tooltip":"cite-authorlink-tooltip", 'increment_group':'authorlink', 'increment_button':true}, {"field": "보존url"}, {"field": "보존날짜"}, {"field": "위치"}, {"field": "쪽", "tooltip":"cite-page-tooltip"}, {"field": "통신사"}, {"field": "언어"}, {"field": "형식"}, {"field": "doi", "autofillid":"doi"}, {"field": "인용문"} \]);

new citeTemplate('서적 인용', 'book', \[ // Basic fields {"field": "성<N>", "autofillprop":"last-incr", 'increment_group':'author'}, {"field": "이름<N>", "autofillprop":"first-incr", 'increment_group':'author', 'increment_button':true}, {"field": "제목", "autofillprop":"title"}, {"field": "날짜", "autofillprop":"year"}, {"field": "출판사", "autofillprop":"publisher"}, {"field": "위치", "autofillprop":"location"}, {"field": "isbn", "autofillid":"isbn"}, {"field": "쪽", "tooltip":"cite-page-tooltip"}, {"field": "판", "autofillprop":"edition"}, {"field": "url"}, {"field": "확인날짜"}, {"field": "ref", "tooltip":"cite-ref-tooltip"}

\], \[ // Expanded fields {"field": "저자<N>", 'increment_group':'author_alt', 'increment_button':true}, {"field": "저자링크<N>", "tooltip":"cite-authorlink-tooltip", 'increment_group':'authorlink', 'increment_button':true}, {"field": "편집자<N>-성", "increment_group":"editor"}, {"field": "편집자<N>-이름", "increment_group":"editor", "increment_button":true}, {"field": "편집자<N>-링크", 'increment_group':'editorlink', 'increment_button':true}, {"field": "보존url"}, {"field": "보존날짜"}, {"field": "언어"}, {"field": "형식"}, {"field": "장"}, {"field": "인용문"} \]);

new citeTemplate('저널 인용', 'journal', \[ // Basic fields {"field": "성<N>", "autofillprop":"last-incr", 'increment_group':'author'}, {"field": "이름<N>", "autofillprop":"first-incr", 'increment_group':'author', 'increment_button':true}, {"field": "제목", "autofillprop":"title"}, {"field": "저널", "autofillprop":"journal"}, {"field": "날짜", "autofillprop":"date"}, {"field": "권", "autofillprop":"volume"}, {"field": "호", "autofillprop":"issue"}, {"field": "쪽", "tooltip":"cite-page-tooltip"}, {"field": "doi", "autofillid":"doi"}, {"field": "pmid", "autofillid":"pmid"}, {"field": "url"}, {"field": "확인날짜"}, {"field": "ref", "tooltip":"cite-ref-tooltip"}, \], \[ // Expanded fields {"field": "저자<N>", 'increment_group':'author_alt', 'increment_button':true}, {"field": "저자링크<N>", "tooltip":"cite-authorlink-tooltip", 'increment_group':'authorlink', 'increment_button':true}, {"field": "편집자<N>-성", "increment_group":"editor"}, {"field": "편집자<N>-이름", "increment_group":"editor", "increment_button":true}, {"field": "편집자<N>-링크", 'increment_group':'editorlink', 'increment_button':true}, {"field": "총서"}, {"field": "쪽기타", "tooltip":"cite-at-tooltip"}, {"field": "번역제목"}, {"field": "출판사"}, {"field": "위치"}, {"field": "언어"}, {"field": "형식"}, {"field": "issn"}, {"field": "pmc"}, {"field": "oclc"}, {"field": "bibcode"}, {"field": "id"}, {"field": "인용문"}, \]);

new citeErrorCheck({'type':'reflist', 'testname':'samecontent', 'desc': 'cite-samecontent-desc', 'func': function(reflist) {

` var errors = [];`
` var refs2 = [];`
` for(var i=0; i<reflist.length; i++) {`
`   if (!reflist[i].shorttag) {`
`     if ($.inArray(reflist[i].content, refs2) != -1) {`
`       if ($.inArray(reflist[i].content, errors) == -1) {`
`         errors.push(reflist[i].content);`
`       }`
`     } else {`
`       refs2.push(reflist[i].content);`
`     }`
`   }`
` }`
` ret = [];`
` for(var j=0; j<errors.length; j++) {`
`   ret.push({'msg':'cite-samecontent-error', 'err':errors[j]});`
` }`
` return ret;`

}} );

new citeErrorCheck({'type':'reflist', 'testname':'repeated', 'desc':'cite-repeated-desc', 'func': function(reflist) {

` var errors = [];`
` var refs2 = [];`
` for(var i=0; i<reflist.length; i++) {`
`   if (!reflist[i].shorttag && reflist[i].refname) {`
`     if ($.inArray(reflist[i].refname, refs2) != -1) {`
`       if ($.inArray(reflist[i].refname, errors) == -1) {`
`         errors.push(reflist[i].refname);`
`       }`
`     } else {`
`       refs2.push(reflist[i].refname);`
`     }`
`   }`
` }`
` ret = [];`
` for(var j=0; j<errors.length; j++) {`
`   ret.push({'msg':'cite-repeated-error', 'err':errors[j]});`
` }`
` return ret;`

}} );

new citeErrorCheck({'type':'reflist', 'testname':'undefined', 'desc':'cite-undefined-desc', 'func': function(reflist) {

` var errors = [];`
` var longrefs = [];`
` for(var i=0; i<reflist.length; i++) {`
`   if (!reflist[i].shorttag && reflist[i].refname) {`
`     longrefs.push(reflist[i].refname);`
`   }`
` }`
` for(var j=0; i<reflist.length; j++) {`
`   if (reflist[i].shorttag && $.inArray(reflist[i].refname, errors) == -1 && $.inArray(reflist[i].refname, longrefs) == -1) {`
`     errors.push(reflist[i].refname);`
`   }`
` }`
` ret = [];`
` for(var j=0; j<errors.length; j++) {`
`   ret.push({'msg':'cite-undefined-error', 'err':errors[j]});`
` }`
` return ret;`

}} );

CiteTB.init();