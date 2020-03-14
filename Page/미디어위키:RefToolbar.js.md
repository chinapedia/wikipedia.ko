> This article is converted from Wikipedia: [:RefToolbar.js](https://ko.wikipedia.org/wiki/:RefToolbar.js).


/\*jshint smarttabs:true, loopfunc:true,forin:false\*/ /\*global mw, $, importScript \*/ // TODO: make autodate an option in the CiteTemplate object, not a preference

// Global object // TODO: // \* Remove this once the page is moved to a module 'ext.gadget.refToolbarDialogs' depending on 'ext.gadget.refToolbarBase' if (typeof CiteTB === 'undefined') {

` var CiteTB = {`
`   "Templates" : {}, // All templates`
`   "Options" : {}, // Global options`
`   "UserOptions" : {}, // User options`
`   "DefaultOptions" : {}, // Script defaults`
`   "ErrorChecks" : {} // Error check functions`
` };`

}

// Only execute on edit, unless it is a user JS/CSS page // TODO: Remove tests already done by [MediaWiki:Gadget-refToolbar.js](https://ko.wikipedia.org/wiki/MediaWiki:Gadget-refToolbar.js "wikilink") if (

`   ( mw.config.get('wgAction') === 'edit' || mw.config.get('wgAction') === 'submit' ) &&`
`   ( ( mw.config.get('wgNamespaceNumber') !== 2 && mw.config.get('wgNamespaceNumber') !== 4 ) ||`
`   ( mw.config.get('wgPageName').indexOf('.js') === -1 && mw.config.get('wgPageName').indexOf('.css') === -1 ) )`

) {

// TODO: Move this to [MediaWiki:Gadget-refToolbarDialogs.css](https://ko.wikipedia.org/wiki/MediaWiki:Gadget-refToolbarDialogs.css "wikilink") and add it to the definition of module 'ext.gadget.refToolbarDialogs' mw.util.addCSS(".cite-form-td {"+ "height: 0 \!important;"+ "padding: 0.1em \!important;"+ "}");

// Default options, these mainly exist so the script won't break if a new option is added CiteTB.DefaultOptions = {

` "date format" : "`<year>`-`<zmonth>`-`<zdate>`",`
` "autodate fields" : [],`
` "months" : ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],`
` "modal" : true,`
` "autoparse" : false,`
` "expandtemplates": false`

};

// Get an option - user settings override global which override defaults CiteTB.getOption = function(opt) {

` if (CiteTB.UserOptions[opt] !== undefined) {`
`   return CiteTB.UserOptions[opt];`
` } else if (CiteTB.Options[opt] !== undefined) {`
`   return CiteTB.Options[opt];`
` }`
` return CiteTB.DefaultOptions[opt];`

};

CiteTB.init = function() {

` /* Main stuff, build the actual toolbar structure`
`  * 1. get the template list, make the dropdown list and set up the template dialog boxes`
`  * 2. actually build the toolbar:`
`  *    * A section for cites`
`  *    ** dropdown for the templates (previously defined)`
`  *    ** button for named refs with a dialog box`
`  *    ** button for errorcheck`
`  * 3. add the whole thing to the main toolbar`
` */`

` if (typeof $('div[rel=cites]')[0] !== 'undefined') { // Mystery IE bug workaround`
`   return;`
` }`
` $('head').trigger('reftoolbarbase');`
` var $target = $('#wpTextbox1');`
` var temlist = {};`
` for (var t in CiteTB.Templates) {`
`   var tem = CiteTB.Templates[t];`
`   var sform = CiteTB.escStr(tem.shortform);`
`   var actionobj = { `
`     type: 'dialog',`
`     module: 'cite-dialog-'+sform`
`   };`
`   var dialogobj = {};`
`   dialogobj['cite-dialog-'+sform] = {`
`     resizeme: false,`
`     titleMsg: 'cite-dialog-'+sform, `
`     id: 'citetoolbar-'+sform,`
`     init: function() {}, `
`     html: tem.getInitial(), `
`     dialog: {`
`       width:675,`
`       open: function() { `
`         $(this).html(CiteTB.getOpenTemplate().getForm());`
`         /** @param {jQuery.Event} e */`
`         $('.cite-prev-parse').on( 'click', function ( e ) {`
`           e.preventDefault();`
`           CiteTB.prevParseClick();`
`         });`
`       },`
`       buttons: {`
`         'cite-form-submit': function() {`
`           var ref = CiteTB.getRef(false, true);`
`           $(this).dialog( 'close' );`
`           $.wikiEditor.modules.toolbar.fn.doAction( $(this).data( 'context' ), {`
`             type: 'encapsulate',`
`             options: {`
`               post: ref`
`             }`
`           }, $(this) );`
`         },`
`         'cite-form-showhide': CiteTB.showHideExtra,`
`         'cite-refpreview': function() {   `
`           var ref = CiteTB.getRef(false, false);`
`           var template = CiteTB.getOpenTemplate();`
`           var div = $("#citetoolbar-"+CiteTB.escStr(template.shortform));`
`           div.find('.cite-preview-label').show();`
`           div.find('.cite-ref-preview').text(ref).show();`
`           if (CiteTB.getOption('autoparse')) {`
`             CiteTB.prevParseClick();`
`           } else {`
`             div.find('.cite-prev-parse').show();`
`             div.find('.cite-prev-parsed-label').hide();`
`             div.find('.cite-preview-parsed').html('');`
`           }         `
`         },`
`         'wikieditor-toolbar-tool-link-cancel': function() {`
`           $(this).dialog( 'close' );`
`         },`
`         'cite-form-reset': function() {`
`           CiteTB.resetForm();`
`         }`
`       }`
`     } `
`   };`
`   $target.wikiEditor('addDialog', dialogobj);`
`   //if (!CiteTB.getOption('modal')) {`
`     //$('#citetoolbar-'+sform).dialog('option', 'modal', false);`
`   //}`
`   temlist[sform] = {label: tem.templatename, action: actionobj };  `
` }`

` var refsection =  {`
`   'sections': {`
`     'cites': { `
`       type: 'toolbar', `
`       labelMsg: 'cite-section-label',`
`       groups: { `
`         'template': {`
`           tools: {`
`             'template': {`
`               type: 'select',`
`               labelMsg: 'cite-template-list',`
`               list: temlist`
`             } `
`           }`
`         },`
`         'namedrefs': {`
`           labelMsg: 'cite-named-refs-label',`
`           tools: {`
`             'nrefs': {`
`               type: 'button',`
`               action: {`
`                 type: 'dialog',`
`                 module: 'cite-toolbar-namedrefs'`
`               },`
`               icon: '//upload.wikimedia.org/wikipedia/commons/thumb/b/be/Nuvola_clipboard_lined.svg/22px-Nuvola_clipboard_lined.svg.png',`
`               section: 'cites',`
`               group: 'namedrefs',`
`               labelMsg: 'cite-named-refs-button'`
`             }`
`           }`
`         },`
`         'errorcheck': {`
`           labelMsg: 'cite-errorcheck-label',`
`           tools: {`
`             'echeck': {`
`               type: 'button',`
`               action: {`
`                 type: 'dialog',`
`                 module: 'cite-toolbar-errorcheck'           `
`               },`
`               icon: '//upload.wikimedia.org/wikipedia/commons/thumb/a/a3/Nuvola_apps_korganizer-NO.png/22px-Nuvola_apps_korganizer-NO.png',`
`               section: 'cites',`
`               group: 'errorcheck',`
`               labelMsg: 'cite-errorcheck-button'`
`             }`
`           }`
`         }`
`       } `
`     } `
`   } `
` };`
` `
` var defaultdialogs = { `
`   'cite-toolbar-errorcheck': {`
`     titleMsg: 'cite-errorcheck-label',`
`     id: 'citetoolbar-errorcheck',`
`     resizeme: false,`
`     init: function() {},`
`     html: '`

<div id="cite-namedref-loading">

'+

`       '`<img src="//upload.wikimedia.org/wikipedia/commons/4/42/Loading.gif" />`'+`
`       ' '+mw.usability.getMsg('cite-loading')+'`

</div>

',

`     dialog: {`
`       width:550,`
`       open: function() { `
`         CiteTB.loadRefs();`
`       },`
`       buttons: {`
`         'cite-errorcheck-submit': function() {`
`           var errorchecks = $("input[name='cite-err-test']:checked");`
`           var errors = [];`
`           for (var i=0; i<errorchecks.length; i++) {`
`             errors = errors.concat(CiteTB.ErrorChecks[$(errorchecks[i]).val()].run());`
`           }`
`           CiteTB.displayErrors(errors);`
`           $(this).dialog( 'close' );                      `
`         },`
`         'wikieditor-toolbar-tool-link-cancel': function() {`
`           $(this).dialog( 'close' );`
`         }`
`       }`
`     }`
`   },`
`   'cite-toolbar-namedrefs': {`
`     titleMsg: 'cite-named-refs-title',`
`     resizeme: false,`
`     id: 'citetoolbar-namedrefs',`
`     html: '`

<div id="cite-namedref-loading">

'+

`       '`<img src="//upload.wikimedia.org/wikipedia/commons/4/42/Loading.gif" />`'+`
`       ' '+mw.usability.getMsg('cite-loading')+'`

</div>

',

`     init: function() {},`
`     dialog: {`
`       width: 550,`
`       open: function() { `
`         CiteTB.loadRefs();`
`       },`
`       buttons: {`
`         'cite-form-submit': function() {`
`           var refname = $("#cite-namedref-select").val();`
`           if (refname === '') {`
`             return;`
`           }`
`           $(this).dialog( 'close' );`
`           $.wikiEditor.modules.toolbar.fn.doAction( $(this).data( 'context' ), {`
`             type: 'encapsulate',`
`             options: {`
`               post: CiteTB.getNamedRef(refname, true)`
`             }`
`           }, $(this) );`
`         },`
`         'wikieditor-toolbar-tool-link-cancel': function() {`
`           $(this).dialog( 'close' );`
`         }                   `
`       }`
`     }      `
`   }`
` };`
` `
` $target.wikiEditor('addDialog', defaultdialogs);`
` $('#citetoolbar-namedrefs').off('dialogopen');`
` if (!CiteTB.getOption('modal')) {`
`   //$('#citetoolbar-namedrefs').dialog('option', 'modal', false);`
`   //$('#citetoolbar-errorcheck').dialog('option', 'modal', false);`
`   mw.util.addCSS(".ui-widget-overlay {"+`
`   "display:none !important;"+`
`   "}");  `
` }`
` $target.wikiEditor('addToToolbar', refsection);`

};

// Load local data - messages, cite templates, etc. $(document).ready( function() {

` switch( mw.config.get('wgUserLanguage') ) {`
`   case 'ko': // Korean`
`     importScript('미디어위키:RefToolbarMessages-ko.js');`
`     break;`
`   default: // English`
`     importScript('미디어위키:RefToolbarMessages-en.js');`
` }`

});

// Setup the main object CiteTB.mainRefList = \[\]; CiteTB.refsLoaded = false;

// REF FUNCTIONS // Actually assemble a ref from user input CiteTB.getRef = function(inneronly, forinsert) {

` var i;`
` var template = CiteTB.getOpenTemplate();`
` var templatename = template.templatename;`
` var res = '';`
` var refobj = {'shorttag':false};`
` if (!inneronly) {`
`   var group = $('#cite-'+CiteTB.escStr(template.shortform)+'-group').val();`
`   var refname = $('#cite-'+CiteTB.escStr(template.shortform)+'-name').val();`
`   res += '<ref';`
`   if (refname) {`
`     refname = $.trim(refname);`
`     res+=' name='+CiteTB.getQuotedString(refname);`
`     refobj.refname = refname;`
`   }`
`   if (group) {`
`     group = $.trim(group);`
`     res+=' group='+CiteTB.getQuotedString(group);`
`     refobj.refgroup = group;`
`   }`
`   res+='>';`
` }`
` var content ='{{'+templatename;`
` for( g in template.incrementables ) {`
`   group = template.incrementables[g];`
`   for (i=1; i<=group.val; i++) {`
`       for (j=0; j<group.fields.length; j++) {`
`           var fieldname = group.fields[j].field;`
`           var fieldid = fieldname.replace('`<N>`', i.toString());`
`           var field = $('#cite-'+CiteTB.escStr(template.shortform)+'-'+fieldid).val();`
`           if (field) {`
`               content+='|'+fieldid+'=';`
`               content+= $.trim(field);`
`           }`
`       }`
`   }`
` }`
` for( i=0; i<template.basic.length; i++ ) {`
`   if (template.basic[i].increment_group) {`
`       continue;`
`   }`
`   var fieldname = template.basic[i].field;`
`   var field = $('#cite-'+CiteTB.escStr(template.shortform)+'-'+fieldname).val();`
`   if (field) {`
`     content+=' |'+fieldname+'=';`
`     content+= $.trim(field);`
`   }`
` }`
` if ($('#cite-form-status').val() !== 'closed') {`
`   for( i=0; i<template.extra.length; i++ ) {`
`     if (template.extra[i].increment_group) {`
`       continue;`
`     }`
`     var fieldname = template.extra[i].field;`
`     var field = $('#cite-'+CiteTB.escStr(template.shortform)+'-'+fieldname).val();`
`     if (field) {`
`       content+=' |'+fieldname+'=';`
`       content+= $.trim(field);`
`     }`
`   }`
` }`
` content+= '}}';`
` res+=content;`
` refobj.content = content;`
` if (!inneronly) {`
`   res+= '`</ref>`';`
` }`
` if (forinsert) {`
`   CiteTB.mainRefList.push(refobj);`
` }`
` return res;`

};

// Make a reference to a named ref CiteTB.getNamedRef = function(refname, forinsert) {

` if (forinsert) {`
`   CiteTB.mainRefList.push( {'shorttag':true, 'refname':refname} );`
` }`
` return '`\[1\]`';  `

};

// Function to load the ref list CiteTB.loadRefs = function() {

` if (CiteTB.refsLoaded) {`
`   return;`
` }`
` CiteTB.getPageText(CiteTB.loadRefsInternal);`

};

// Function that actually loads the list from the page text CiteTB.loadRefsInternal = function(text) {

` // What this does:             extract first name/group                                     extract second name/group                                          shorttag   inner content`
` var refsregex = /< *ref(?: +(name|group) *= *(?:"([^"]*?)"|'([^']*?)'|([^ '"\/\>]*?)) *)? *(?: +(name|group) *= *(?:"([^"]*?)"|'([^']*?)'|([^ '"\/\>]*?)) *)? *(?:\/ *>|>((?:.|\n)*?)< *\/ *ref *>)/gim;`
` // This should work regardless of the quoting used for names/groups and for linebreaks in the inner content  `
` while (true) {`
`   var ref = refsregex.exec(text);`
`   if (ref === null) {`
`     break;`
`   }`
`   var refobj = {};`
`   if (ref[9]) { // Content + short tag check`
`     //alert('"'+ref[9]+'"');`
`     refobj.content = ref[9]; `
`     refobj.shorttag = false;`
`   } else {`
`     refobj.shorttag = true;`
`   }`
`   if (ref[1] !== '') { // First name/group`
`     if (ref[2]) {`
`       refobj['ref'+ref[1]] = ref[2];`
`     } else if (ref[3]) {`
`       refobj['ref'+ref[1]] = ref[3];`
`     } else {`
`       refobj['ref'+ref[1]] = ref[4];`
`     }`
`   }`
`   if (ref[5] !== '') { // Second name/group`
`     if (ref[6]) {`
`       refobj['ref'+ref[5]] = ref[6];`
`     } else if (ref[7]) {`
`       refobj['ref'+ref[5]] = ref[7];`
`     } else {`
`       refobj['ref'+ref[5]] = ref[8];`
`     }`
`   }`
`   CiteTB.mainRefList.push(refobj);`
` }`
` CiteTB.refsLoaded = true;`
` CiteTB.setupErrorCheck();`
` CiteTB.setupNamedRefs();`

};

// AJAX FUNCTIONS // Parse some wikitext and hand it off to a callback function CiteTB.parse = function(text, callback) {

` $.post( mw.util.wikiScript( 'api' ),`
`   {action:'parse', title:mw.config.get('wgPageName'), text:text, prop:'text', format:'json'},`
`   function(data) {`
`     var html = data.parse.text['*'];`
`     callback(html);`
`   },`
`   'json'`
` );  `

};

// Use the API to expand templates on some text CiteTB.expandtemplates = function(text, callback) {

` $.post( mw.util.wikiScript( 'api' ),`
`   {action:'expandtemplates', title:mw.config.get('wgPageName'), text:text, format:'json'},`
`   function(data) {`
`     var restext = data.expandtemplates['*'];`
`     callback(restext);`
`   },`
`   'json'`
` );`

};

// Function to get the page text CiteTB.getPageText = function(callback) {

` var section = $("input[name='wpSection']").val();`
` if ( section !== '' ) {`
`   var postdata = {action:'query', prop:'revisions', rvprop:'content', pageids:mw.config.get('wgArticleId'), format:'json'};`
`   if (CiteTB.getOption('expandtemplates')) {`
`     postdata.rvexpandtemplates = '1';`
`   }`
`   $.get( mw.util.wikiScript( 'api' ),`
`     postdata,`
`     function(data) {`
`       var pagetext = data.query.pages[mw.config.get('wgArticleId').toString()].revisions[0]['*'];`
`       callback(pagetext);`
`     },`
`     'json'`
`   );`
` } else {`
`   if (CiteTB.getOption('expandtemplates')) {`
`     CiteTB.expandtemplates($('#wpTextbox1').wikiEditor('getContents').text(), callback);`
`   } else {`
`     callback($('#wpTextbox1').wikiEditor('getContents').text());`
`   }`
` }`

};

// Autofill a template from an ID (ISBN, DOI, PMID, URL) CiteTB.initAutofill = function() {

` var elemid = $(this).attr('id');`
` var res = /^cite\-auto\-(.*?)\-(.*)\-(.*)$/.exec(elemid);`
` var tem = res[1];`
` var field = res[2];`
` var autotype = res[3];`
` var id = $('#cite-'+tem+'-'+field).val();`
` if (!id) {`
`   return false;`
` }`
` var url = '//tools.wmflabs.org/reftoolbar/lookup.php?';`
` url+=autotype+'='+encodeURIComponent(id);`
` url+='&template='+encodeURIComponent(tem);`
` var s = document.createElement('script');`
` s.setAttribute('src', url);`
` s.setAttribute('type', 'text/javascript');`
` document.getElementsByTagName('head')[0].appendChild(s);`
` return false;`

};

// Callback for autofill //TODO: Autofill the URL, at least for DOI CiteTB.autoFill = function(data, template, type) {

` var cl = 'cite-'+template+'-';`
` var i,j, coauthors;`
` $('.'+cl+'title').val(data.title);`
` // Fill in authors`
` if (data.authors && data.authors.length > 0) {`
`     if ($('.'+cl+'last-incr-1').length != 0) {`
`       var classes = $('.'+cl+'last-incr-1').eq(0).attr('class').split(/\s+/);`
`       var group = false;`
`       var patt = /cite-[^-]*?-incr-(.*)/`
`       for (var c=0; c<classes.length; c++) {`
`           if (patt.exec(classes[c])) {`
`               group = patt.exec(classes[c])[1];`
`               break;`
`           }`
`       }`
`       $('.'+cl+'last-incr-1').val(data.authors[0][0])`
`       $('.'+cl+'first-incr-1').val(data.authors[0][1])`
`       elemid = '#cite-incr-'+template+'-'+group;`
`       for (var i=2; i<data.authors.length+1; i++) {`
`           $(elemid).click();`
`           $('.'+cl+'last-incr-'+i.toString()).val(data.authors[i-1][0])`
`           $('.'+cl+'first-incr-'+i.toString()).val(data.authors[i-1][1])`
`       }`
`     } else if ($('.'+cl+'author-incr-1').length != 0) {`
`       var classes = $('.'+cl+'author-incr-1').eq(0).attr('class').split(/\s+/);`
`       var group = false;`
`       var patt = /cite-[^-]*?-incr-(.*)/`
`       for (var c=0; c<classes.length; c++) {`
`           if (patt.exec(classes[c])) {`
`               group = patt.exec(classes[c])[1];`
`               break;`
`           }`
`       }`
`       $('.'+cl+'author-incr-1').val(data.authors[0].join(', '))`
`       elemid = '#cite-incr-'+template+'-'+group;`
`       for (var i=2; i<data.authors.length+1; i++) {`
`           $(elemid).click();`
`           $('.'+cl+'author-incr-'+i.toString()).val(data.authors[i-1].join(', '))`
`       }`
`     } else if ($('.'+cl+'last1').length != 0) {`
`       for(i=0; data.authors && i<data.authors.length; i++) {`
`         if ($('.'+cl+'last'+(i+1)).length) {`
`            $('.'+cl+'last'+(i+1)).val(data.authors[i][0]);`
`            $('.'+cl+'first'+(i+1)).val(data.authors[i][1]);`
`         } else {`
`           coauthors = [];`
`           for(j=i; j<data.authors.length; j++) {`
`             coauthors.push(data.authors[j].join(', '));`
`           }`
`           $('.'+cl+'coauthors').val(coauthors.join('; '));`
`           break;`
`         }`
`       }`
`     } else if($('.'+cl+'author1').length !== 0) {`
`       for(i=0; data.authors && i<data.authors.length; i++) {`
`         if ($('.'+cl+'author'+(i+1)).length) {`
`            $('.'+cl+'author'+(i+1)).val(data.authors[i].join(', '));`
`         } else {`
`           coauthors = [];`
`           for(j=i; j<data.authors.length; j++) {`
`             coauthors.push(data.authors[j].join(', '));`
`           }`
`           $('.'+cl+'coauthors').val(coauthors.join('; '));`
`           break;`
`         }`
`       }`
`     } else {`
`       var authors = [];`
`       for(i=0; data.authors && i<data.authors.length; i++) {`
`         authors.push(data.authors[i].join(', '));`
`       }`
`       $('.'+cl+'authors').val(authors.join('; '));`
`     }`
` }`

` if (type === 'pmid' || type === 'doi') {`
`   if (data.date && (data.fulldate || !$('.'+cl+'month').length)) {`
`     var DT = new Date(data.date);`
`     var useday = /\d{4}-\d{2}-\d{2}/.test(data.date);`
`     var usemonth = /\d{4}-\d{2}/.test(data.date);`
`     $('.'+cl+'date').val(CiteTB.formatDate(DT, useday, usemonth));`
`   } else if (!data.fulldate && $('.'+cl+'month').length && $('.'+cl+'year').length) {`
`     if (data.month) { // lookup.php sets month to false if it isn't provided`
`       $('.'+cl+'month').val( CiteTB.getOption('months')[parseInt(data.month)-1] );`
`     }`
`     $('.'+cl+'year').val(data.year);`
`   } else {`
`     $('.'+cl+'date').val(data.date);`
`   }`
`   $('.'+cl+'journal').val(data.journal);`
`   $('.'+cl+'volume').val(data.volume);`
`   $('.'+cl+'issue').val(data.issue);`
`   $('.'+cl+'pages').val(data.pages);`
`   if (type === 'pmid' && data.doi) {`
`     $('.'+cl+'doi').val(data.doi);`
`   }`
` } else if (type === 'isbn') {`
`   $('.'+cl+'publisher').val(data.publisher);`
`   $('.'+cl+'location').val(data.location);`
`   $('.'+cl+'year').val(data.year);`
`   $('.'+cl+'edition').val(data.edition);`
` } else if (type === 'url') {`
`   if (data.date) {`
`     var DT = new Date(data.date);`
`     var useday = /\d{4}-\d{2}-\d{2}/.test(data.date) && template !== 'book';`
`     var usemonth = /\d{4}-\d{2}/.test(data.date) && template !== 'book';`
`     var yearOrDate = (template === 'book') ? 'year' : 'date';`
`     $('.'+cl+yearOrDate).val(CiteTB.formatDate(DT, useday, usemonth));`
`   }`
`   $('.'+cl+'journal').val(data.journal);`
`   $('.'+cl+'volume').val(data.volume);`
`   $('.'+cl+'issue').val(data.issue);`
`   $('.'+cl+'pages').val(data.pages);`
`   $('.'+cl+'publisher').val(data.publisher);`
`   $('.'+cl+'edition').val(data.edition);`
`   $('.'+cl+'isbn').val(data.isbn);`
`   $('.'+cl+'issn').val(data.issn);`
`   $('.'+cl+'doi').val(data.doi);`
`   // "en-US" isn't a valid value for the language parameter`
`   if (data.language && data.language !== 'en-US' && data.language !== 'en-GB') {`
`       $('.'+cl+'language').val(data.language);`
`   }`
`   $('.'+cl+'chapter').val(data.chapter);`
` }`

};

// FORM DIALOG FUNCTIONS // Add new incrementable fields CiteTB.incrementFields = function() {

`   template = CiteTB.getOpenTemplate();`
`   var currentrow = $(this).parents('tr')[0];`
`   $(this).prev().css('width', '100%')`
`   $(this).detach();`
`   var elemid = $(this).attr('id');`
`   var res = /^cite\-incr\-(.*?)\-(.*)$/.exec(elemid);`
`   group = res[2];`
`   increments = template.incrementables[group];`
`   fields = increments.fields;`
`   incrval = increments.val+1;`
`   template.incrementables[group].val += 1;`
`   trs = template.makeFormInner(fields, false);`
`   trs.reverse();`
`   for (var i=0; i<trs.length; i++) {`
`       $(currentrow).after(trs[i]);`
`   }`

};

// fill the accessdate param with the current date CiteTB.fillAccessdate = function() {

` var elemid = $(this).attr('id');`
` var res = /^cite\-date\-(.*?)\-(.*)$/.exec(elemid);`
` var id = res[1];`
` var field = res[2];`
` var DT = new Date();`
` var datestr = CiteTB.formatDate(DT);`
` $('#cite-'+id+'-'+field).val(datestr);`
` return false;`

};

CiteTB.formatDate = function(DT, useday, usemonth) {

` if (typeof useday == "undefined") {`
`   useday = true;  `
` }`
` if (typeof usemonth == "undefined") {`
`   usemonth = true;    `
` }`
` var datestr = CiteTB.getOption('date format');`
` var zmonth = '';`
` var month = DT.getMonth()+1;`
` if (month < 10) {`
`   zmonth = "0"+month.toString();`
` } else {`
`   zmonth = month.toString();`
` }`
` month = month.toString();`
` var zdate = '';`
` var date = DT.getDate();`
` if (date < 10) {`
`   zdate = "0"+date.toString();`
` } else {`
`   zdate = date.toString();`
` }`
` date = date.toString();`
` if (useday) {`
`   datestr = datestr.replace('`<date>`', date);`
`   datestr = datestr.replace('`<zdate>`', zdate);`
` } else {`
`   datestr = datestr.replace('`<date>`', '');`
`   datestr = datestr.replace('`<zdate>`', '');`
` }`
` if (usemonth) {`
`   datestr = datestr.replace('`<month>`', month);`
`   datestr = datestr.replace('`<zmonth>`', zmonth);`
`   datestr = datestr.replace('`<monthname>`', CiteTB.getOption('months')[DT.getMonth()]);`
` } else {`
`   datestr = datestr.replace('`<month>`', '');`
`   datestr = datestr.replace('`<zmonth>`', '');`
`   datestr = datestr.replace('`<monthname>`', '');`
` }  `
` datestr = datestr.replace('`<year>`', DT.getFullYear().toString());`
` return datestr.replace(/^[ \/\-\,\.]*(.*?)[ \/\-\,\.]*$/g, "$1"); // Cleanup any dangling spaces or connectors that might result from omitting date/month`

};

// Function called after the ref list is loaded, to actually set the contents of the named ref dialog // Until the list is loaded, its just a "Loading" placeholder CiteTB.setupNamedRefs = function() {

` var names = [], i;`
` for( i=0; i<CiteTB.mainRefList.length; i++) {`
`   if (!CiteTB.mainRefList[i].shorttag && CiteTB.mainRefList[i].refname) {`
`     names.push(CiteTB.mainRefList[i]);`
`   }`
` }`
` var stuff = $('`

<div>

');

` $('#citetoolbar-namedrefs').html( stuff );`
` if (names.length === 0) {`
`   stuff.html(mw.usability.getMsg('cite-no-namedrefs'));`
` } else {`
`   stuff.html(mw.usability.getMsg('cite-namedrefs-intro'));`
`   var select = $('`<select id="cite-namedref-select">`');`
`   select.append($('`<option value="" />`').text(mw.usability.getMsg('cite-named-refs-dropdown')));`
`   for(i=0; i<names.length; i++) {`
`     select.append($('`<option />`').text(names[i].refname));`
`   }`
`   stuff.after(select);`
`   select.before('`
`');      `
`   var prevlabel = $('`

<div id="cite-nref-preview-label" style="display:none;" />

').html(mw.usability.getMsg('cite-raw-preview'));

`   select.after(prevlabel);`
`   prevlabel.before("`

`");`
`   prevlabel.after('`

<div id="cite-namedref-preview" style="padding:0.5em; font-size:110%" />

');

`   var parselabel = $('`<span id="cite-parsed-label" style="display:none;" />`').html(mw.usability.getMsg('cite-parsed-label'));`
`   $('#cite-namedref-preview').after(parselabel);`
`   parselabel.after('`

<div id="cite-namedref-parsed" style="padding-bottom:0.5em; font-size:110%" />

');

`   var link = $('`<a href="#" id="cite-nref-parse" style="margin:0 1em 0 1em; display:none; color:darkblue" />`');`
`   link.html(mw.usability.getMsg('cite-form-parse'));`
`   $('#cite-namedref-parsed').after(link);`
`   `
`   $("#cite-namedref-select").on( 'change', CiteTB.namedRefSelectClick);`
`   $('#cite-nref-parse').on( 'click', CiteTB.nrefParseClick);`
` }      `

};

// Function to get the errorcheck form HTML CiteTB.setupErrorCheck = function() {

` var form = $('`

<div id="cite-errorcheck-heading" />

').html(mw.usability.getMsg('cite-errorcheck-heading'));

` var ul = $("`

");

` var test;`
` for (var t in CiteTB.ErrorChecks) {`
`   test = CiteTB.ErrorChecks[t];`
`   ul.append(test.getRow());`
` }`
` form.append(ul);`
` $('#citetoolbar-errorcheck').html(form);`

};

// Callback function for parsed preview CiteTB.fillNrefPreview = function(parsed) {

` $('#cite-parsed-label').show();`
` $('#cite-namedref-parsed').html(parsed);`

};

// Click handler for the named-ref parsed preview CiteTB.nrefParseClick = function() {

` var choice = $("#cite-namedref-select").val();`
` if (choice === '') {`
`   $('#cite-parsed-label').hide();`
`   $('#cite-namedref-parsed').text('');`
`   return false;`
` }`
` $('#cite-nref-parse').hide();`
` for( var i=0; i<CiteTB.mainRefList.length; i++) {`
`   if (!CiteTB.mainRefList[i].shorttag && CiteTB.mainRefList[i].refname == choice) {`
`     CiteTB.parse(CiteTB.mainRefList[i].content, CiteTB.fillNrefPreview);`
`     return false;`
`   }`
` }  `

};

// Click handler for the named-ref dropdown CiteTB.lastnamedrefchoice = ''; CiteTB.namedRefSelectClick = function() {

` var choice = $("#cite-namedref-select").val();`
` if (CiteTB.lastnamedrefchoice == choice) {`
`   return;`
` }`
` CiteTB.lastnamedrefchoice = choice;`
` $('#cite-parsed-label').hide();`
` $('#cite-namedref-parsed').text('');`
` if (choice === '') {`
`   $('#cite-nref-preview-label').hide();`
`   $('#cite-namedref-preview').text('');`
`   $('#cite-nref-parse').hide();`
`   return;`
` }`
` for( var i=0; i<CiteTB.mainRefList.length; i++) {`
`   if (!CiteTB.mainRefList[i].shorttag && CiteTB.mainRefList[i].refname == choice) {`
`     $('#cite-nref-preview-label').show();`
`     $('#cite-namedref-preview').text(CiteTB.mainRefList[i].content);`
`     if (CiteTB.getOption('autoparse')) {`
`       CiteTB.nrefParseClick();`
`     } else {`
`       $('#cite-nref-parse').show();`
`     }`
`   }`
` }`

};

// callback function for parsed preview CiteTB.fillTemplatePreview = function(text) {

` var template = CiteTB.getOpenTemplate();`
` var div = $("#citetoolbar-"+CiteTB.escStr(template.shortform));`
` div.find('.cite-prev-parsed-label').show();`
` div.find('.cite-preview-parsed').html(text);`

};

// Click handler for template parsed preview CiteTB.prevParseClick = function() {

` var ref = CiteTB.getRef(true, false);`
` var template = CiteTB.getOpenTemplate();`
` var div = $("#citetoolbar-"+CiteTB.escStr(template.shortform));`
` div.find('.cite-prev-parse').hide();`
` CiteTB.parse(ref, CiteTB.fillTemplatePreview);`

};

// Show/hide the extra fields in the dialog box CiteTB.showHideExtra = function() {

` var template = CiteTB.getOpenTemplate();`
` var div = $("#citetoolbar-"+CiteTB.escStr(template.shortform));`
` var setting = div.find(".cite-form-status").val();`
` if ( setting === 'closed' ) {`
`   div.find(".cite-form-status").val('open');`
`   div.find('.cite-extra-fields').show(1, function() {`
`     // jQuery adds "display:block", which screws things up`
`     div.find('.cite-extra-fields').attr('style', 'width:100%; background-color:transparent;'); `
`   });`
` } else {`
`   div.find(".cite-form-status").val('closed');`
`   div.find('.cite-extra-fields').hide();`
` } `

};

// Resets form fields and previews // Resets form fields and previews CiteTB.resetForm = function() {

` var template = CiteTB.getOpenTemplate();`
` var div = $("#citetoolbar-"+CiteTB.escStr(template.shortform));`
` div.html(template.getForm());`

};

// STRING UTILITY FUNCTIONS // Returns a string quoted as necessary for name/group attributes CiteTB.getQuotedString = function(s) {

` var sq = /\'/.test(s); // single quotes`
` var dq = /\"/.test(s); // double quotes`
` if (!sq && !dq) { // Always quotes for non-latin alphabet`
`   return '"'+s+'"';`
` } else if (!dq) { // Can use double quotes`
`   return '"'+s+'"';`
` } else if (!sq) { // Can use single quotes`
`   return "'"+s+"'";`
` } else { // Has double and single quotes`
`   s = s.replace(/\"/g, '\'');`
`   return '"'+s+'"';`
` }`

};

// Fix up strings for output - capitalize first char, replace underscores with spaces CiteTB.fixStr = function(s) {

` s = s.slice(0,1).toUpperCase() + s.slice(1);`
` s = s.replace('_',' ');`
` return s;`

};

// Escape spaces and quotes for use in HTML classes/ids CiteTB.escStr = function(s) {

` return s.replace(' ', '-').replace("'", "\'").replace('"', '\"');`

};

// MISC FUNCTIONS // Determine which template form is open, and get the template object for it CiteTB.getOpenTemplate = function() {

` var dialogs = $(".ui-dialog-content.ui-widget-content:visible");`
` var templatename = $(dialogs[0]).find(".cite-template").val();`
` return CiteTB.Templates[templatename];`

};

// Display the report for the error checks CiteTB.displayErrors = function(errors) {

` $('#cite-err-report').remove();`
` var table = $('`

<table id="cite-err-report" style="width:100%; border:1px solid #A9A9A9; background-color:#FFEFD5; padding:0.25em; margin-top:0.5em" />

');

` $('#editpage-copywarn').before(table);`
` var tr;`
` var tr1 = $('`

<tr style="width:100%" />

');

` var th1 = $('`

<th style="width:60%; font-size:110%" />

').html(mw.usability.getMsg('cite-err-report-heading'));

` var th2 = $('`

<th style="text-align:right; width:40%" />

');

` var im = $('`<img />`').attr('src', '//upload.wikimedia.org/wikipedia/commons/thumb/5/55/Gtk-stop.svg/20px-Gtk-stop.svg.png');`
` im.attr('alt', mw.usability.getMsg('cite-err-report-close')).attr('title', mw.usability.getMsg('cite-err-report-close'));`
` var ad = $('`<a id="cite-err-check-close" />`').attr('href', '#');`
` ad.append(im);`
` th2.append(ad);`
` tr1.append(th1).append(th2);`
` table.append(tr1);`
` $('#cite-err-check-close').on('click', function() {  $('#cite-err-report').remove(); });`
` if (errors.length === 0) {`
`   tr = $('`

<tr style="width:100%;" />

');

`   var td = $('`

<td style="text-align:center; margin:1.5px;" />

').html(mw.usability.getMsg('cite-err-report-empty'));

`   tr.append(td);`
`   table.append(tr);`
`   `
`   return;`
` }`
` for(var e in errors) {`
`   var err = errors[e];`
`   tr = $('`

<tr style="width:100%;" />

');

`   var td1 = $('`

<td style="border: 1px solid black; margin:1.5px; width:60%" />

').html(err.err);

`   var td2 = $('`

<td style="border: 1px solid black; margin:1.5px; width:40%" />

').html(mw.usability.getMsg(err.msg));

`   tr.append(td1).append(td2);`
`   table.append(tr);`
` }`

};

} // End of code loaded only on edit

1.