> This article is converted from Wikipedia: [VCard](https://ko.wikipedia.org/wiki/VCard).


**vCard**는 전자 [명함](https://ko.wikipedia.org/wiki/명함 "wikilink")의 세계 표준 [파일 형식이다](https://ko.wikipedia.org/wiki/파일_형식 "wikilink"). 주로 [이메일](https://ko.wikipedia.org/wiki/이메일 "wikilink")에 덧붙여 보내거나, [월드 와이드 웹이나](../Page/월드_와이드_웹.md "wikilink") [메시지](../Page/메시지.md "wikilink") 형태로 바꿀 수 있다. 보통 vCard에는 [이름](../Page/이름.md "wikilink"), [주소](../Page/주소.md "wikilink"), [전화번호](../Page/전화번호.md "wikilink"), [이메일](https://ko.wikipedia.org/wiki/이메일 "wikilink"), [웹사이트](../Page/웹사이트.md "wikilink"), [로고](../Page/로고.md "wikilink"), [사진](../Page/사진.md "wikilink"), [소리](../Page/소리.md "wikilink") 등 [문자](../Page/문자.md "wikilink"), [멀티미디어](../Page/멀티미디어.md "wikilink") 자료도 넣을 수 있다.

## vCard 파일의 예

1인에 대한 정보가 담긴 vCard 파일의 예는 다음과 같다.

### vCard 2.1

    BEGIN:VCARD
    VERSION:2.1
    N:Gump;Forrest;;Mr.
    FN:Forrest Gump
    ORG:Bubba Gump Shrimp Co.
    TITLE:Shrimp Man
    PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
    TEL;WORK;VOICE:(111) 555-1212
    TEL;HOME;VOICE:(404) 555-1212
    ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
    LABEL;WORK;PREF;ENCODING=QUOTED-PRINTABLE;CHARSET=UTF-8:100 Waters Edge=0D=
     =0ABaytown\, LA 30314=0D=0AUnited States of America
    ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
    LABEL;HOME;ENCODING=QUOTED-PRINTABLE;CHARSET=UTF-8:42 Plantation St.=0D=0A=
     Baytown, LA 30314=0D=0AUnited States of America
    EMAIL:forrestgump@example.com
    REV:20080424T195243Z
    END:VCARD

### vCard 3.0

    BEGIN:VCARD
    VERSION:3.0
    N:Gump;Forrest;;Mr.;
    FN:Forrest Gump
    ORG:Bubba Gump Shrimp Co.
    TITLE:Shrimp Man
    PHOTO;VALUE=URI;TYPE=GIF:;http://www.example.com/dir_photos/my_photo.gif
    TEL;TYPE=WORK,VOICE:(111) 555-1212
    TEL;TYPE=HOME,VOICE:(404) 555-1212
    ADR;TYPE=WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
    LABEL;TYPE=WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
    ADR;TYPE=HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
    LABEL;TYPE=HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
    EMAIL:forrestgump@example.com
    REV:2008-04-24T19:52:43Z
    END:VCARD

### vCard 4.0

최신 표준은 RFC 6350 표준에 기반을 둔다.

    BEGIN:VCARD
    VERSION:4.0
    N:Gump;Forrest;;Mr.;
    FN:Forrest Gump
    ORG:Bubba Gump Shrimp Co.
    TITLE:Shrimp Man
    PHOTO;MEDIATYPE=image/gif:http://www.example.com/dir_photos/my_photo.gif
    TEL;TYPE=work,voice;VALUE=uri:tel:+1-111-555-1212
    TEL;TYPE=home,voice;VALUE=uri:tel:+1-404-555-1212
    ADR;TYPE=WORK;PREF=1;LABEL="100 Waters Edge\nBaytown\, LA 30314\nUnited States of America":;;100 Waters Edge;Baytown;LA;30314;United States of America
    ADR;TYPE=HOME;LABEL="42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
    EMAIL:forrestgump@example.com
    REV:20080424T195243Z
    x-qq:21588891
    END:VCARD

## 함께 보기

  - [마이크로포맷](../Page/마이크로포맷.md "wikilink")
  - [국제 인터넷 표준화 기구](../Page/국제_인터넷_표준화_기구.md "wikilink")

## 외부 링크

  - [Internet mail Consortium - Personal Data Interchange](https://web.archive.org/web/20150906130553/http://www.imc.org/pdi/)
  - [vCard: The Electronic Business Card (Version 2.1)](https://web.archive.org/web/20120501162958/http://www.imc.org/pdi/vcard-21.doc) vCard 2.1 specification (Sept-18-1996)
  - [Representing vCard Objects in RDF](https://www.w3.org/TR/vcard-rdf/) - [W3C](../Page/W3C.md "wikilink") ontology
  - RFC 2425 — A MIME Content-Type for Directory Information
  - RFC 2426 — vCard MIME Directory Profile
  - RFC 2739 — Calendar Attributes for vCard and LDAP
  - RFC 4122 — UUID URN namespace (could be used for UID type)
  - RFC 4770 — vCard Extensions for Instant Messaging
  - RFC 6350 — vCard Format Specification
  - RFC 6351 — xCard: vCard XML Representation
  - RFC 6473 — vCard KIND:application
  - RFC 6474 — vCard Format Extensions: Place of Birth, Place and Date of Death
  - RFC 6715 — vCard Format Extensions: Representing vCard Extensions Defined by the Open Mobile Alliance (OMA) Converged Address Book (CAB) Group
  - RFC 6868 — Parameter Value Encoding in iCalendar and vCard
  - RFC 7095 — jCard: The JSON Format for vCard

[분류:파일 포맷](https://ko.wikipedia.org/wiki/분류:파일_포맷 "wikilink") [분류:인터넷 표준](https://ko.wikipedia.org/wiki/분류:인터넷_표준 "wikilink")