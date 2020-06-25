> This article is converted from Wikipedia: [Enscript](https://ko.wikipedia.org/wiki/Enscript).


**GNU enscript**  [컴퓨터 프로그램은](../Page/컴퓨터_프로그램.md "wikilink")  텍스트 파일을 [pdf](../Page/PDF.md "wikilink"),[PostScript](../Page/포스트스크립트.md "wikilink"), [RTF](../Page/서식_있는_텍스트_포맷.md "wikilink"),또는 HTML 형식등으로 변환하여주는 [명령어형](https://ko.wikipedia.org/wiki/리눅스_명령어 "wikilink") 프로그램이다. 변환시킬 대상파일 형식이 주어지지 않은 경우 입력 파일은 주어진 enscript 프로세스 [표준으로](../Page/표준_스트림.md "wikilink") 대체된다. Enscript는 명령어 형 프로그램이므로 [파이프라인등을](../Page/명령어_파이프라인.md "wikilink") 연계사용하여 확장할 수 있는 다른 형식의 출력이 미디어,텍스트 [인코딩](https://ko.wikipedia.org/wiki/인코딩 "wikilink")등  많은 옵션을 사용할 수 있는 사용자 정의 출력이 가능하다. 이것은 [GNU GPL](https://ko.wikipedia.org/wiki/GNU_일반_공중_사용권 "wikilink") 버전 3하에 배포되고있다.\[1\]

대용량 고속처리에도 불구하고 [유니코드](../Page/유니코드.md "wikilink") 등 완전한 [인코딩](https://ko.wikipedia.org/wiki/인코딩 "wikilink")은 미지원될수있다.

## 도움말(help)

`> enscript --help`
`Usage: enscript [OPTION]... [FILE]...`
`Mandatory arguments to long options are mandatory for short options too.`
` -#                         an alias for option -n, --copies`
` -1                         same as --columns=1`
` -2                         same as --columns=2`
`     --columns=NUM          specify the number of columns per page`
` -a, --pages=PAGES          specify which pages are printed`
` -A, --file-align=ALIGN     align separate input files to ALIGN`
` -b, --header=HEADER        set page header`
` -B, --no-header            no page headers`
` -c, --truncate-lines       cut long lines (default is to wrap)`
` -C[START], --line-numbers[=START]`
`                            precede each line with its line number`
` -d                         an alias for option --printer`
` -D, --setpagedevice=KEY[:VALUE]`
`                            pass a page device definition to output`
` -e[CHAR], --escapes[=CHAR]       enable special escape interpretation`
` -E[LANG], --highlight[=LANG]     highlight source code`
` -f, --font=NAME            use font NAME for body text`
` -F, --header-font=NAME     use font NAME for header texts`
` -g, --print-anyway         nothing (compatibility option)`
` -G                         same as --fancy-header`
`     --fancy-header[=NAME]  select fancy page header`
` -h, --no-job-header        suppress the job header page`
` -H[NUM], --highlight-bars[=NUM]  specify how high highlight bars are`
` -i, --indent=NUM           set line indent to NUM characters`
` -I, --filter=CMD           read input files through input filter CMD`
` -j, --borders              print borders around columns`
` -J,                        an alias for option --title`
` -k, --page-prefeed         enable page prefeed`
` -K, --no-page-prefeed      disable page prefeed`
` -l, --lineprinter          simulate lineprinter, this is an alias for:`
`                              --lines-per-page=66, --no-header, --portrait,`
`                              --columns=1`
` -L, --lines-per-page=NUM   specify how many lines are printed on each page`
` -m, --mail                 send mail upon completion`
` -M, --media=NAME           use output media NAME`
` -n, --copies=NUM           print NUM copies of each page`
` -N, --newline=NL           select the newline character.  Possible`
``                            values for NL are: n (`\n') and r (`\r').``
` -o                         an alias for option --output`
` -O, --missing-characters   list missing characters`
`` -p, --output=FILE          leave output to file FILE.  If FILE is `-',``
`                            leave output to stdout.`
` -P, --printer=NAME         print output to printer NAME`
` -q, --quiet, --silent      be really quiet`
` -r, --landscape            print in landscape mode`
` -R, --portrait             print in portrait mode`
` -s, --baselineskip=NUM     set baselineskip to NUM`
` -S, --statusdict=KEY[:VALUE]`
`                            pass a statusdict definition to the output`
` -t, --title=TITLE          set banner page's job title to TITLE.  Option`
`                            sets also the name of the input file stdin.`
` -T, --tabsize=NUM          set tabulator size to NUM`
` -u[TEXT], --underlay[=TEXT]      print TEXT under every page`
` -U, --nup=NUM              print NUM logical pages on each output page`
` -v, --verbose              tell what we are doing`
` -V, --version              print version number`
` -w, --language=LANG        set output language to LANG`
` -W, --options=APP,OPTION   pass option OPTION to helper application APP`
` -X, --encoding=NAME        use input encoding NAME`
` -z, --no-formfeed          do not interpret form feed characters`
` -Z, --pass-through         pass through PostScript and PCL files`
`                            without any modifications`
`Long-only options:`
` --color[=bool]             create color outputs with states`
` --continuous-page-numbers  count page numbers across input files.  Don't`
`                            restart numbering at beginning of each file.`
` --download-font=NAME       download font NAME`
` --extended-return-values   enable extended return values`
` --filter-stdin=NAME        specify how stdin is shown to the input filter`
` --footer=FOOTER            set page footer`
` --h-column-height=HEIGHT   set the horizontal column height to HEIGHT`
` --help                     print this help and exit`
` --help-highlight           describe all supported --highlight languages`
`                            and file formats`
` --highlight-bar-gray=NUM   print highlight bars with gray NUM (0 - 1)`
` --list-media               list names of all known media`
` --margins=LEFT:RIGHT:TOP:BOTTOM`
`                            adjust page marginals`
` --mark-wrapped-lines[STYLE]`
`                            mark wrapped lines in the output with STYLE`
` --non-printable-format=FMT specify how non-printable chars are printed`
` --nup-columnwise           layout pages in the N-up printing columnwise`
` --nup-xpad=NUM             set the page x-padding of N-up printing to NUM`
` --nup-ypad=NUM             set the page y-padding of N-up printing to NUM`
` --page-label-format=FMT    set page label format to FMT`
` --ps-level=LEVEL           set the PostScript language level that enscript`
`                            should use`
` --printer-options=OPTIONS  pass extra options to the printer command`
` --rotate-even-pages        rotate even-numbered pages 180 degrees`
` --slice=NUM                print vertical slice NUM`
` --style=STYLE              use highlight style STYLE`
` --swap-even-page-margins   swap left and right side margins for each even`
`                            numbered page`
` --toc                      print table of contents`
` --ul-angle=ANGLE           set underlay text's angle to ANGLE`
` --ul-font=NAME             print underlays with font NAME`
` --ul-gray=NUM              print underlays with gray value NUM`
` --ul-position=POS          set underlay's starting position to POS`
` --ul-style=STYLE           print underlays with style STYLE`
` --word-wrap                wrap long lines from word boundaries`

## 사용 예

pdf 출력

`> enscript sample.txt  -o  sample.pdf`

## 외부 링크

  - [공식 사이트](https://www.gnu.org/software/enscript/)
  - [리눅스는 출력 가이드](https://web.archive.org/web/20180910052135/http://www.eecs.utk.edu/resources/it/eecs-it-knowledge-base/printing/linux-printing-guide/advanced-linux-printing/)

## 참고

[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink")

1.  (GNU)Report bugs to \<bug-enscript@gnu.org\>.