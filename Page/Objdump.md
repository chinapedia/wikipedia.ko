> This article is converted from Wikipedia: [Objdump](https://ko.wikipedia.org/wiki/Objdump).


**objdump**는 [GNU 바이너리 유틸리티의](https://ko.wikipedia.org/wiki/GNU_바이너리_유틸리티 "wikilink") 일부로서, 라이브러리, 컴파일된 오브젝트 모듈, 공유 오브젝트 파일, 독립 실행파일등의 바이너리 파일들의 정보를 보여주는 프로그램이다. **objdump**는 [ELF](https://ko.wikipedia.org/wiki/ELF "wikilink") 파일을 [어셈블리어](https://ko.wikipedia.org/wiki/어셈블리어 "wikilink")로 보여주는 [역어셈블러](../Page/역어셈블러.md "wikilink")로 사용될 수 있다.

예를 들자면 오브젝트 파일을 [역어셈블](../Page/역어셈블러.md "wikilink") 하기 위해서 아래와 같이 쓴다:

`objdump -Dslx `*`file`*

**objdump**는 오브젝트 파일들의 내용을 읽을때 [BFD](https://ko.wikipedia.org/wiki/Binary_File_Descriptor_library "wikilink") 라이브러리를 사용한다. readelf([GNU Binutils에](https://ko.wikipedia.org/wiki/GNU_Binutils "wikilink") 역시 포함되어 있다.)는 **objdump**처럼 [ELF](https://ko.wikipedia.org/wiki/ELF "wikilink") 파일들을 읽을 수 있지만 [BFD](https://ko.wikipedia.org/wiki/Binary_File_Descriptor_library "wikilink") 라이브러리를 사용하지 않는다.

[GNU](https://ko.wikipedia.org/wiki/GNU "wikilink") 프로젝트는 높은 기능을 갖춘 **objdump** 프로그램을 [GNU Binutils](https://ko.wikipedia.org/wiki/GNU_Binutils "wikilink") 패키지에 포함시키고 있다.

## 출력 예제

`$ objdump -D -M intel file.bin | grep main.: -A20`

``` objdump-nasm
  4004ed:   55                      push   rbp
  4004ee:   48 89 e5                mov    rbp,rsp
  4004f1:   c7 45 ec 00 00 00 00    mov    DWORD PTR [rbp-0x14],0x0
  4004f8:   c7 45 f0 01 00 00 00    mov    DWORD PTR [rbp-0x10],0x1
  4004ff:   c7 45 f4 02 00 00 00    mov    DWORD PTR [rbp-0xc],0x2
  400506:   c7 45 f8 03 00 00 00    mov    DWORD PTR [rbp-0x8],0x3
  40050d:   c7 45 fc 04 00 00 00    mov    DWORD PTR [rbp-0x4],0x4
  400514:   c7 45 ec 00 00 00 00    mov    DWORD PTR [rbp-0x14],0x0
  40051b:   eb 13                   jmp    400530 <main+0x43>
  40051d:   8b 05 15 0b 20 00       mov    eax,DWORD PTR [rip+0x200b15]        # 601038 <globalA>
  400523:   83 e8 01                sub    eax,0x1
  400526:   89 05 0c 0b 20 00       mov    DWORD PTR [rip+0x200b0c],eax        # 601038 <globalA>
  40052c:   83 45 ec 01             add    DWORD PTR [rbp-0x14],0x1
  400530:   8b 05 02 0b 20 00       mov    eax,DWORD PTR [rip+0x200b02]        # 601038 <globalA>
  400536:   39 45 ec                cmp    DWORD PTR [rbp-0x14],eax
  400539:   7c e2                   jl     40051d <main+0x30>
  40053b:   5d                      pop    rbp
  40053c:   c3                      ret
  40053d:   0f 1f 00                nop    DWORD PTR [rax]
```

## 외부 링크

  - [맨페이지의 설명](http://www.linuxmanpages.com/man1/objdump.1.php)

[분류:유닉스 프로그래밍 도구](https://ko.wikipedia.org/wiki/분류:유닉스_프로그래밍_도구 "wikilink") [분류:역어셈블러](https://ko.wikipedia.org/wiki/분류:역어셈블러 "wikilink")