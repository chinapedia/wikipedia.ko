> This article is converted from Wikipedia: [Tar \( \)](https://ko.wikipedia.org/wiki/Tar_\(_\)).


**타르**(tar)는 [컴퓨터](../Page/컴퓨터.md "wikilink")에서, 테입 아카이브(Tape Archive)를 위해 고안된 [파일 형식과](https://ko.wikipedia.org/wiki/파일_형식 "wikilink") 이런 형식의 파일을 다루는데 사용되는 프로그램을 의미한다. 파일 형식은 초기 [유닉스](../Page/유닉스.md "wikilink") 시대에 만들어졌고 [POSIX](../Page/POSIX.md "wikilink").1-1988 과 POSIX.1-2001 에 의해 표준화되었다.

초기에는 [테입](../Page/테이프_드라이브.md "wikilink") 백업 목적으로, 순차적 입출력 장치에 직접 쓰도록 개발되었으나, 현재는, [배포](https://ko.wikipedia.org/wiki/배포 "wikilink") 또는 [아카이브](../Page/아카이브.md "wikilink") 용도로 많은 파일을 디렉토리 구조, 파일 속성들을 보존하면서 하나의 큰 파일로 묶는 데 주로 사용된다.

## 파일 형식

### 헤더

pre-POSIX.1-1988 (i.e. v7) tar 헤더는 다음과 같다:

| 필드 오프셋 | 필드 크기 | 필드                              |
| ------ | ----- | ------------------------------- |
| 0      | 100   | 파일 이름                           |
| 100    | 8     | 파일 모드                           |
| 108    | 8     | 소유자의 숫자로 된 사용자 ID               |
| 116    | 8     | 그룹의 숫자로 된 사용자 ID                |
| 124    | 12    | 파일 크기 (바이트, 옥탈 베이스)             |
| 136    | 12    | 마지막 수정 시간. 숫자로 된 유닉스 시간 형식 (옥탈) |
| 148    | 8     | 헤더 레코드를 위한 체크섬                  |
| 156    | 1     | 링크 표시자 (파일 유형)                  |
| 157    | 100   | 링크된 파일의 이름                      |

pre-POSIX.1-1988 **링크 표시자**(Link indicator) 필드는 다음의 값을 가질 수 있다:

| 값                                                                                                  | 의미                                     |
| -------------------------------------------------------------------------------------------------- | -------------------------------------- |
| '0' 또는 ([ASCII](https://ko.wikipedia.org/wiki/ASCII "wikilink") [NUL](../Page/널_문자.md "wikilink")) | 일반 파일                                  |
| '1'                                                                                                | [하드 링크](../Page/하드_링크.md "wikilink")   |
| '2'                                                                                                | [심볼릭 링크](../Page/심볼릭_링크.md "wikilink") |

링크 지시자 필드

## 사용

### Tarpipe

tarpipe는 tar 유틸리티의 [stdout](https://ko.wikipedia.org/wiki/stdout "wikilink") 파일로 아카이브를 만들어서 [표준 입력에](https://ko.wikipedia.org/wiki/표준_입력 "wikilink") 다른 tar 프로세스로 파이프 처리하는 방식이며, 압축이 풀리는 위치는 다른 디렉터리이다. 이 과정은 모든 특수 파일들을 포함한 원본 디렉터리 트리 전체를 복사한다. 이를테면 다음과 같다:

`tar cf - `*`srcdir`*` | (cd `*`destdir`*` && tar xv)`

### 소프트웨어 배포

tar 포맷은 [오픈 소스](../Page/오픈_소스.md "wikilink") [소프트웨어 배포용으로](https://ko.wikipedia.org/wiki/소프트웨어_배포 "wikilink") 광범위하게 사용되고 있다.

## 압축 파일의 확장자

[섬네일과](https://ko.wikipedia.org/wiki/파일:Targzip.svg "wikilink") 같은 압축 방식과 함께 종종 사용된다. 그림에서 볼 수 이듯이, 아카이브 내의 파일들은 하나의 단위로 병합되어 압축된다.\]\]

| 긴 형태      | 짧은 형태             |
| --------- | ----------------- |
| .tar.bz2  | .tb2, .tbz, .tbz2 |
| .tar.gz   | .tgz              |
| .tar.lz   |                   |
| .tar.lzma | .tlz              |
| .tar.xz   | .txz              |
| .tar.Z    | .tZ               |

파일 확장자

## 같이 보기

  - [압축 소프트웨어의 비교](https://ko.wikipedia.org/wiki/압축_소프트웨어의_비교 "wikilink")

## 외부 링크

  - Includes documentation on how different implementations store various types of information and specialize headers.

  -
  -
  -
  -
  -
  -
[분류:GNU 프로젝트 소프트웨어](https://ko.wikipedia.org/wiki/분류:GNU_프로젝트_소프트웨어 "wikilink") [분류:유닉스 보관 및 압축 관련 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_보관_및_압축_관련_유틸리티 "wikilink") [분류:백업 소프트웨어](https://ko.wikipedia.org/wiki/분류:백업_소프트웨어 "wikilink") [분류:아카이브 포맷](https://ko.wikipedia.org/wiki/분류:아카이브_포맷 "wikilink") [분류:자유 백업 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_백업_소프트웨어 "wikilink")