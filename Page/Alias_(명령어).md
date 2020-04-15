> This article is converted from Wikipedia: [Alias \(명령어\)](https://ko.wikipedia.org/wiki/Alias_\(명령어\)).


[컴퓨팅](../Page/컴퓨팅.md "wikilink")에서 **alias**는 다양한 [명령 줄 인터프리터](../Page/명령_줄_인터페이스.md "wikilink")(워드를 다른 문자열로 치환할 수 있는 [유닉스 셸](../Page/유닉스_셸.md "wikilink"), [4DOS](../Page/4DOS.md "wikilink")/[4NT](https://ko.wikipedia.org/wiki/4NT "wikilink"), [윈도우 파워셸](https://ko.wikipedia.org/wiki/윈도우_파워셸 "wikilink") 등의 [셸](../Page/셸.md "wikilink"))의 명령어이다. 시스템 명령어를 단축시키기 위해 주로 사용되며, 그 외에 주기적으로 사용되는 명령어에 기본 변수를 추가하기 위해 사용된다. [MS-DOS](../Page/MS-DOS.md "wikilink")와 [마이크로소프트 윈도우](../Page/마이크로소프트_윈도우.md "wikilink") 운영 체제의 앨리어스 기능은 [도스키](https://ko.wikipedia.org/wiki/도스키 "wikilink")(DOSKey) 명령 줄 유틸리티를 통해 제공된다.

alias는 셸 세션이 생존하는 동안에만 지속된다. 주로 사용되는 별칭들은 셸의 구성 파일(csh의 경우 `~/.cshrc` 또는 시스템 전역 `/etc/csh.cshrc`, 배시의 경우 `~/.bashrc` 또는 시스템 전역 `/etc/bashrc` 또는 `/etc/bash.bashrc` for bash)에서 설정할 수 있으며 일치하는 셸 세션이 시작되자마자 이용이 가능하다. alias 명령어들은 설정 파일에 직접 기록하거나 별도의 파일에서 [source시켜서](https://ko.wikipedia.org/wiki/source_\(명령어\) "wikilink") 쓸 수 있으며 이름은 보통 .alias(여러 개의 셸을 사용할 경우 .alias-bash, alias-csh 등)로 명명한다.

## 별칭 만들기

### 유닉스

비영구적인 별칭은 alias 명령에 이름/값 쌍을 인자로 지정하여 만들 수 있다. [유닉스 셸에서](../Page/유닉스_셸.md "wikilink") 문법은 다음과 같다:

``` sh
 alias copy='cp'
```

### C 셸

이와 동일한 [C 셸이나](../Page/C_셸.md "wikilink") [tcsh](https://ko.wikipedia.org/wiki/tcsh "wikilink") 셸의 문법은 다음과 같다:

``` csh
 alias copy "cp"
```

이 별칭의 의미는 `copy` 명령을 셸에서 읽으면 `cp`로 바꾸어서 대신 명령이 실행되게끔 하는 것을 뜻한다.

### 4DOS

4DOS/4NT 셸에서 다음의 문법을 사용하여 `cp`를 4DOS의 `copy` 명령어의 별칭으로 정의할 수 있다:

`alias cp copy`

### 윈도우 파워셸

윈도우 파워셸에서 새로운 별칭을 만들려면 `new-alias` cmdlet을 사용하면 된다:

``` ps1
 new-alias ci copy-item
```

실행 시 `copy-item` cmdlet으로 치환되는 `ci`라는 이름의 새로운 별칭을 만든다.

파워셸에서 별칭은 명령의 기본 인자를 지정하기 위해 사용하는 것은 불가능하다. 이는 파워셸 환경 변수 중 하나인 $PSDefaultParameterValues 콜렉션에 항목들을 추가함으로써 수행할 수 있다.

## 역사

유닉스에서 alias는 [C 셸에](../Page/C_셸.md "wikilink") 도입되었으며 [tcsh](https://ko.wikipedia.org/wiki/tcsh "wikilink")와 [배시와](../Page/배시_\(유닉스_셸\).md "wikilink") 같은 파생 셸들에도 생존해 있다. C 셸의 별칭들은 하나의 줄까지로 제한되었다. 단순한 바로 가기 명령을 만드는 데는 유용하였으나 더 복잡한 구성체에는 적합하지 않았다. 구 버전의 [본 셸은](../Page/본_셸.md "wikilink") alias를 제공하지 않았으나 csh alias 개념보다 더 강력한 기능들을 제공하였다. csh의 alias 개념은 [배시와](../Page/배시_\(유닉스_셸\).md "wikilink") [콘 셸](../Page/콘_셸.md "wikilink")(ksh)에 도입되었다.

## 별칭 제거

유닉스 셸과 4DOS/4NT에서 별칭들은 `unalias` 명령어를 실행하여 제거할 수 있다:

``` bash
 unalias copy          # Removes the copy alias
 unalias -a            # The -a switch will remove all aliases; not available in 4DOS/4NT
```

``unalias *             # 4DOS/4NT equivalent of `unalias -a` - wildcards are supported``

윈도우 파워셸에서 별칭은 `remove-item`을 사용하여 alias:\\ 드라이브를 통해 제거할 수 있다:

``` powershell
 remove-item alias:ci  # Removes the ci alias
```

## 일반적인 별칭

배시 셸에서 일부 흔히 쓰이는 별칭들은 다음과 같다:

``` bash
alias ls='ls --color=auto' # use colors
alias la='ls -Fa'          # list all files
alias ll='ls -Fls'         # long listing format

alias rm='rm -i'           # prompt before overwrite (but dangerous, see rm for a better approach)
alias cp='cp -i'           # prompt before overwrite (same general problem as the rm)
alias mv='mv -i'           # prompt before overwrite (same general problem as the rm)

alias vi='vim'             # use improved vi editor
```

Standard aliases of Windows PowerShell include:

``` PowerShell
 new-alias cd set-location

 new-alias ls get-childitem
 new-alias dir get-childitem

 new-alias echo write-output
 new-alias ps get-process
 new-alias kill stop-process
```

## 외부 링크

  -
  - [Bash man page for alias](http://www.ss64.com/bash/alias.html)

  - [The alias Command](http://linfo.org/alias.html) by The Linux Information Project (LINFO)

  - [Find out if a command is aliased to another command](https://web.archive.org/web/20150402180603/https://www.linux-tips.org/article/80/find-out-if-a-command-is-aliased-to-another-command)

[Alias](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:윈도우 관리](https://ko.wikipedia.org/wiki/분류:윈도우_관리 "wikilink")