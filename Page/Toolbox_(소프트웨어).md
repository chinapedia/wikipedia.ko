> This article is converted from Wikipedia: [Toolbox \(\)](https://ko.wikipedia.org/wiki/Toolbox_\(\)).


**ToolboX**는 컴퓨터 프로그래밍을 학술 과목에 접목하여 비전공자들에게 소개하도록 고안된 [통합 개발 환경이다](../Page/통합_개발_환경.md "wikilink").\[1\]\[2\] 학생들이 문제를 해결할 때 노트북이나 블랙보드에서 수행되는 것과 마찬가지로, 컴퓨터 언어로 표현할 수 있는 일련의 계산 (예: [알고리즘](../Page/알고리즘.md "wikilink") 방식)을 수행한다는 전제를 기반으로 디자인되었다.

ToolboX는 환경 및 학술 콘텐츠 외에도 학생들의 사용 데이터를 수집하고 [인공지능](../Page/인공지능.md "wikilink")을 기반으로 하는 [빅데이터](https://ko.wikipedia.org/wiki/빅데이터 "wikilink") 알고리즘을 통해 처리한다. ([Guadalinex](https://ko.wikipedia.org/wiki/:en:Guadalinex "wikilink") 및 [Guadalinfo](https://ko.wikipedia.org/wiki/:es:Guadalinfo "wikilink") 저장소에 통합된 이후에 안달루시아 지역에서만 백만 명의 학생들이 접근할 수 있게 되었다.)\[3\] 이러한 기술은 교육 및 자원 계획을 개선할 수 있도록 학생 커뮤니티에 관한 정보를 얻는데 사용될 수 있다. 이러한 정보의 예로 영재 학생, ADHD 및 실독증을 가진 학생을 사전 진단 할 수 있다.\[4\]

## 기능

ToolboX는 선생님이 강의실이나 컴퓨터실에서 사용할 수있는 교육자료이다. 프로그램이 시작되면 명령 창, 프로그램을 작성하는 [텍스트 편집기](https://ko.wikipedia.org/wiki/텍스트_편집기 "wikilink") 및 그래픽 창으로 이루어진 간단한 개발 환경이 표시된다. 문제목록을 정하고 나면 학생은 프로그램을 작성하여 문제를 해결해야한다. 명령 창에서 실행되어야 할 도움말 명령과 프로그램 디버깅 및 실행을위한 다른 명령을 제공하기도 한다. 프로그램에 의해 계산 된 솔루션이 정확하면 전체 목록이 완료 될 때까지 다음 문제가 표시된다.사용 된 프로그래밍 언어는 교육, 과학 및 공학에서 널리 사용되는 과학적 프로그래밍 언어인 [GNU Octave이다](../Page/GNU_옥타브.md "wikilink").

## 문제 정의

ToolboX는 다양한 학문 분야의 문제를 표현하는 [problegram](https://ko.wikipedia.org/wiki/:es:problegrama "wikilink") 의 개념을 기반으로한다. 정의에는 문제, 팁, wiki 도움말, 해당 (알파) 숫자 솔루션, 제안 된 프로그램 (다른 언어) 및 문제를 푼 후 해당 문제에 대한 핵심정리 같은 정보가 포함된다. 문제 (또는 모듈)의 관계는 [JSON](../Page/JSON.md "wikilink") 형식의 파일 이름이있는 목록이다.

` {`
` "class": "wordproblem",`
` "statement": "Determine $$ \left(\frac{2}{3}\right)^2$$",`
` "solution":  "4/9",`
` "tip"    : ["Raise numerator and denominator to the same power."],`
` "keyword": ["mathematics", "rationals"],`
` "wiki"   : ["\poweroffraction"],`
` "hint" : {`
`   "js"    : "",`
`   "octave": ""`
` },`
` "program" : {`
`   "js"    : "`
` numerator   = pow(2, 2);`
` denominator = pow(3, 2);`
` solution = numerator / denominator;`
` },`
`   "octave": "`
` numerator   = 2^2`
` denominator = 3^2`
` solution = numerator / denominator"`
` },`
` "takehomemessage": "The power of a fraction derives from the product of fractions.",`
` "author": "ToolboX",`
` "URL"   : "toolbox.uma.es",`
` "CC"    : "BY-NC-SA 3.0"`
` }`

## 설치

ToolboX는 Guadalinex 저장소\[5\]의 안달루시아 공공센터와 안달루시안 농촌 지역의 Guadalinfo\[6\]네트워크에서 설치할 수 있다. 이 네트워크를 이용하지 않는다면 아래의 두 가지 방법을 통해 설치할 수도 있다.

### deb file을 통해 설치하는 방법

[데비안](../Page/데비안.md "wikilink") 기반의 리눅스 배포판 ([Ubuntu](https://ko.wikipedia.org/wiki/Ubuntu "wikilink"), Stretch, [Raspbian](../Page/라즈비안.md "wikilink"), [Lubuntu](https://ko.wikipedia.org/wiki/루분투 "wikilink"))이 설치된 컴퓨터에서 ToolboX는 다음 단계에 따라 [deb](http://toolbox.uma.es/download/toolbox_latest.deb) file을 통해 설치할수 있다.

``` bash
$ wget -N --quiet toolbox.uma.es/download/toolbox_latest.deb
$ sudo apt-get update
$ sudo dpkg -i toolbox_latest.deb
  dpkg: dependency problems prevent ...
  [other messages]
$ sudo apt-get -f install
  [other messages]
  Setting up [dependency]
  ...
```

[Ubuntu_version_history\#Ubuntu_18.04_LTS_(Bionic_Beaver)](https://ko.wikipedia.org/wiki/우분투_버전_역사 "wikilink")

``` bash
$ wget -N --quiet toolbox.uma.es/download/toolbox_latest.deb
$ sudo apt-get update
$ sudo gdebi toolbox_latest.deb
  ...
```

### ISO file을 통해 설치하는 방법

[ISO file](https://web.archive.org/web/20180512043648/http://toolbox.uma.es/download/toolbox_1.0_64.iso) 을 먼저 다운로드 한 다음 UNetbootin을 설치해야한다. 그 후 [USB](../Page/USB.md "wikilink") (+ 4GB)를 연결하면 UNetbootin이 실행되며 ISO 파일은 영구 저장소가있는 라이브 버전으로 구워진다. (이 과정은 USB를 지우므로 필요하다면 반드시 미리 복사해 놓아야 한다.)

1.  다운로드 한 ISO file을 선택한다.
2.  영구 저장 장치의 크기를 지정한다. (예 : 1000MB) (선택사항)
3.  USB가 연결된 유닛을 선택한다.

복사 프로세스가 완료되면 부팅 방법으로 선택된 USB의 라이브 버전에서 시스템이 다시 시작된다. (이 경우 PC에서는 [ESC](https://ko.wikipedia.org/wiki/ESC "wikilink"), [F2](https://ko.wikipedia.org/wiki/F2 "wikilink") 또는 [F9](https://ko.wikipedia.org/wiki/F9 "wikilink"), Mac에서는 [Alt 키와](../Page/Alt_키.md "wikilink") 같은 특수 키를 눌러 부팅을 중단하는 과정을 거쳐야 할 수 있다.) [BIOS에](../Page/바이오스.md "wikilink") 들어가 원하는 [부팅](../Page/부팅.md "wikilink") 방식을 선택한다. 시스템이 라이브 버전에서 부팅되면 왼쪽 상단 모서리에서 주 메뉴에 액세스 할 수 있고 *Programming* 카테고리에서 *ToolboX*를 찾을 수 있다.

## 사용

ToolboX를 실행하면 화면은 시스템 콘솔, 텍스트 편집기, 그래픽 창 세 영역으로 구분된다. 콘솔에 'task' 또는 'help' 명령을 입력하면 작업 모듈과 사용 가능한 명령 목록에 대한 정보가 제공된다. 'task'명령으로 작업이 로드되면 'tip'과 'wiki'가 추가 정보를 제공한다. 각 작업은 텍스트 편집기에서 프로그램을 입력하고 콘솔에서 'go'명령을 통해 실행된다.

## 배포

버전 0.0에서는 스페인 교육 시스템에 맞추어 모든 대학 예비 과목에 대한 문제 목록을 포함했으며, 교사가 온라인으로 신청하면 학생들에게 USB flash drive 형태로 제공되었다.\[7\] 이 드라이브에는 라이브 [리눅스 배포판](../Page/리눅스_배포판.md "wikilink"), [GNU Octave](../Page/GNU_옥타브.md "wikilink") 프로그래밍 언어 해석기, ToolboX 및 필요한 소프트웨어가 들어 있다.\[8\]

ToolboX는 GNU GPLv3 라이센스로 배포된다. 첫 번째 버전에는 대학 취학 전 교육 (수학, 물리 및 화학) 과목의 과제가 포함되어 있다.\[9\]\[10\] 소스코드 [source code](http://bitbucket.org/umafoss/toolbox) 는 공용저장소에서 사용 가능하다.

## 각주

## 외부 링크

  - [Averroes blog](https://blogsaverroes.juntadeandalucia.es/toolbox/) (Council of Andalusia, Board of Education)
  - [official website](https://toolbox.uma.es/)

[분류:교육용 프로그래밍 언어](https://ko.wikipedia.org/wiki/분류:교육용_프로그래밍_언어 "wikilink")

1.  Vico, Francisco (2017년). "[ToolboX: Una estrategia transversal para la enseñanza de la programación en entornos educativos](http://www.aenui.net/ojs/index.php?journal=revision&page=article&op=view&path%5B%5D=333)". *ReVisión*. **10** (2): 53–68. ISSN [1989-1199.](https://www.worldcat.org/title/revision/oclc/802407747)
2.  Vico, Francisco (2016년 9월 14일). *[Proyecto ToolboX](http://www.congresocedi.es/es/ei-18) *. Workshop Educación en Informática sub-18 (ei\<18). V Congreso Español de Informática. Salamanca. p. 2. 2016년 9월 10일에 확인함.
3.  Vico, Francisco (2018년 6월 28일). "[Inteligencia Artificial para analizar el progreso de los estudiantes con ToolboX](https://www.educaciontrespuntocero.com/experiencias/hablanlosprofes/inteligencia-artificial-toolbox/86202.html)". *Educación 3.0.* Check date values in: `|date=` (help)
4.  Castillo, Ignacio (2018년 7월 22일). ""[Programar será tan importante como saber leer o escribir](https://www.laopiniondemalaga.es/malaga/2018/07/22/programar-sera-importante-leer-o/1021894.html)"". *La opinión de Málaga*.
5.  Castillo, Ignacio (2018년 7월 15일). ""[Los profesores son la clave del éxito del proceso de transformación digital](https://www.laopiniondemalaga.es/malaga/2018/07/15/profesores-son-clave-exito-proceso/1020174.html)"". *La opinión de Málaga*.
6.  Maldonado, Encarna (2017년 3월 20일). "[Don Alejandro y la pandilla del Minecraft](https://www.malagahoy.es/malaga/Don-Alejandro-pandilla-Minecraft_0_1119188525.html)". *Málaga hoy*.
7.
8.
9.  Maldonado, Encarna (2016년 9월 12일). "[El padre de Alba te enseña a programar](https://www.malagahoy.es/malaga/padre-Alba-ensena-programar_0_1062494233.html)". *Málaga hoy*.
10. Maldonado, Encarna (2017년 9월 24일). "[La 'caja de la programación' aterriza en los colegios](https://www.malagahoy.es/malaga/caja-programacion-aterriza-colegios_0_1175582783.html)". *Málaga hoy*.