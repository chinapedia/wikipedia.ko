> This article is converted from Wikipedia: [Vmlinux](https://ko.wikipedia.org/wiki/Vmlinux).


[섬네일](https://ko.wikipedia.org/wiki/파일:Linux-kernel-vmlinux.png "wikilink") [리눅스](../Page/리눅스.md "wikilink") 시스템에서 **`vmlinux`**는 리눅스가 지원하는 [목적 파일](../Page/목적_파일.md "wikilink") 포맷들 중 하나에서 [리눅스 커널을](../Page/리눅스_커널.md "wikilink") 포함하는 [정적으로 링크된](../Page/정적_라이브러리.md "wikilink") [실행 파일이며](../Page/실행_파일.md "wikilink"), [ELF](https://ko.wikipedia.org/wiki/ELF_파일_형식 "wikilink"), [COFF](https://ko.wikipedia.org/wiki/COFF "wikilink"), [a.out](https://ko.wikipedia.org/wiki/a.out "wikilink")을 포함한다. `vmlinux` 파일은 커널 [디버깅](https://ko.wikipedia.org/wiki/디버깅 "wikilink"), [심볼 테이블](https://ko.wikipedia.org/wiki/심볼_테이블 "wikilink") 생성 등의 작업을 위해 필요하지만 멀티부트 헤더, [부트섹터](https://ko.wikipedia.org/wiki/부트섹터 "wikilink"), 셋업 루틴을 추가함으로써 [운영 체제 커널로서](https://ko.wikipedia.org/wiki/운영_체제_커널 "wikilink") 사용되기 전에 부팅이 가능한 상태여야 한다.

## 용어

전통적으로 [유닉스](../Page/유닉스.md "wikilink") 플랫폼은 커널 이미지 `/unix`를 호출하였다. [가상 메모리의](../Page/가상_메모리.md "wikilink") 개발과 함께 이 기능을 지원했던 커널들은 이와 구별하기 위해 `vm-` 두문자를 부여받았다. `vmlinux`라는 이름은 [vmunix](https://ko.wikipedia.org/wiki/vmunix "wikilink")의 돌연변이이며, `vmlinuz` 끝의 문자 `z`는 압축되었다는 것을 의미한다. (이를테면 [gzip](https://ko.wikipedia.org/wiki/gzip "wikilink"))\[1\]

## 위치

전통적으로 커널은 파일 시스템 계층의 [루트 디렉터리에](https://ko.wikipedia.org/wiki/루트_디렉터리 "wikilink") 위치하였다. 그러나 이 부트로더는 [바이오스](../Page/바이오스.md "wikilink") 드라이버를 사용하여 [하드 디스크에](https://ko.wikipedia.org/wiki/하드_디스크 "wikilink") 접근해야 했으므로 일부 [i386](https://ko.wikipedia.org/wiki/i386 "wikilink") 시스템에서의 제한으로 인해 하드 디스크의 [처음 1024 실린더가](https://ko.wikipedia.org/wiki/실린더_1024 "wikilink") 어드레싱가능하다는 것을 의미했다.

이를 극복하기 위해 리눅스 배포자들은 [부트로더](https://ko.wikipedia.org/wiki/부트로더 "wikilink")와 커널 관련 파일을 저장하기 위해 사용자가 드라이브의 처음 부분에 [파티션을](https://ko.wikipedia.org/wiki/디스크_파티션 "wikilink") 생성하도록 권장하였다. [GRUB](../Page/GRUB.md "wikilink"), [LILO](../Page/LILO.md "wikilink"), [SYSLINUX](https://ko.wikipedia.org/wiki/SYSLINUX "wikilink")는 일반적인 부트로더들이다.

이 파티션은 `/boot`라는 파일시스템 계층에 마운트된다. 이것은 나중에 [파일시스템 계층구조 표준](https://ko.wikipedia.org/wiki/파일시스템_계층구조_표준 "wikilink")(FHS)에 의해 표준화되었고 이 표준은 현재 리눅스 커널 이미지는 `/` 또는 `/boot`에 위치할 것을 요구하지만 실제로 이를 강제할 기술적인 제한은 존재하지 않는다.\[2\]

## 오브젝트 포맷

다음은 x86-64 [젠투](../Page/젠투_리눅스.md "wikilink") 2.6.29 실행 커널 이미지에 있는 ELF 헤더이다.

``` console
$ readelf -h vmlinux
ELF Header:
  Magic:   7f 45 4c 46 02 01 01 00 00 00 00 00 00 00 00 00
  Class:                             ELF64
  Data:                              2's complement, little endian
  Version:                           1 (current)
  OS/ABI:                            UNIX - System V
  ABI Version:                       0
  Type:                              EXEC (Executable file)
  Machine:                           Advanced Micro Devices X86-64
  Version:                           0x1
  Entry point address:               0x1000000
  Start of program headers:          64 (bytes into file)
  Start of section headers:          13951312 (bytes into file)
  Flags:                             0x0
  Size of this header:               64 (bytes)
  Size of program headers:           56 (bytes)
  Number of program headers:         5
  Size of section headers:           64 (bytes)
  Number of section headers:         45
  Section header string table index: 42
```

## 같이 보기

  - [리눅스 커널](../Page/리눅스_커널.md "wikilink")
  - [initrd](https://ko.wikipedia.org/wiki/initrd "wikilink")

## 추가 문헌

  -
  -
## 각주

## 외부 링크

  - [Boot process](http://www.faqs.org/docs/kernel_2_4/lki-1.html)

[분류:리눅스 커널](https://ko.wikipedia.org/wiki/분류:리눅스_커널 "wikilink")

1.
2.