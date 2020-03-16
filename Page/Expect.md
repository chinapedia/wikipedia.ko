> This article is converted from Wikipedia: [Expect](https://ko.wikipedia.org/wiki/Expect).


**Expect**은 [Don Libes가](https://ko.wikipedia.org/wiki/Don_Libes "wikilink") 개발한 [Tcl](../Page/Tcl.md "wikilink") 스크립팅 언어의 확장 기능으로서 [터미널](../Page/단말기.md "wikilink") 인터페이스를 노출하는 프로그램과의 상호작용을 자동화하기 위한 프로그램이다. Expect는 원래 1990년 [유닉스](../Page/유닉스.md "wikilink") 시스템을 위해 개발되었으나 그 뒤로 [마이크로소프트 윈도우와](../Page/마이크로소프트_윈도우.md "wikilink") 다른 운영 체제용으로 이용이 가능해졌다.

## 기초

Expect는 [텔넷](../Page/텔넷.md "wikilink"), [파일 전송 프로토콜](../Page/파일_전송_프로토콜.md "wikilink"), [passwd](https://ko.wikipedia.org/wiki/passwd "wikilink"), [fsck](https://ko.wikipedia.org/wiki/fsck "wikilink"), [rlogin](https://ko.wikipedia.org/wiki/rlogin "wikilink"), [tip](https://ko.wikipedia.org/wiki/tip "wikilink"), [SSH와](../Page/시큐어_셸.md "wikilink") 같은 상호작용 [응용 프로그램의](../Page/응용_소프트웨어.md "wikilink") 제어를 자동화하기 위해 사용된다. Expect는 [의사 터미널](https://ko.wikipedia.org/wiki/의사_터미널 "wikilink")(유닉스)을 사용하거나 콘솔을 에뮬레이트(윈도우)하고 대상 프로그램을 시작한 다음 마치 인간 세상에서 하는 것처럼 해당 프로그램과 통신하며 이는 터미널이나 콘솔 인터페이스를 통해 이루어진다. 또다른 Tcl 확장 기능인 [Tk](https://ko.wikipedia.org/wiki/Tk "wikilink")는 [그래픽 사용자 인터페이스를](../Page/그래픽_사용자_인터페이스.md "wikilink") 제공하기 위해 사용할 수 있다.

Expect는 [정규 표현식](https://ko.wikipedia.org/wiki/정규_표현식 "wikilink") 패턴 매칭과 일반 프로그램 기능들이 있으므로 단순한 스크립트들이 [프로그래밍 언어](../Page/프로그래밍_언어.md "wikilink"), [매크로](../Page/매크로_\(컴퓨터_과학\).md "wikilink"), 기타 프로그램 매커니즘이 결여된 텔넷, FTP, SSH 등의 프로그램들을 똑똑하게 제어할 수 있게 한다.

## 사용법

'autoexpect'라는 도구를 사용하여 expect 스크립트의 생성을 자동화할 수 있다. 이 도구는 동작을 관찰하여 휴리스틱을 사용하여 expect를 생성한다. 생성된 코드의 크기가 클 수 있고 다소 아리송할 수 있지만 생성된 스크립트를 트윅하여 정확한 코드를 얻어내는 것이 가능하다.

``` tcl
# Assume $remote_server, $my_user_id, $my_password, and $my_command were read in earlier
# in the script.
# Open a telnet session to a remote server, and wait for a username prompt.
spawn telnet $remote_server
expect "username:"
# Send the username, and then wait for a password prompt.
send "$my_user_id\r"
expect "password:"
# Send the password, and then wait for a shell prompt.
send "$my_password\r"
expect "%"
# Send the prebuilt command, and then wait for another shell prompt.
send "$my_command\r"
expect "%"
# Capture the results of the command into a variable. This can be displayed, or written to disk.
set results $expect_out(buffer)
# Exit the telnet session, and wait for a special end-of-file character.
send "exit\r"
expect eof
```

다른 예로 FTP를 자동화하는 스크립트는 다음과 같다:

``` tcl
# Set timeout parameter to a proper value.
# For example, the file size is indeed big and the network speed is really one problem,
# you'd better set this parameter a value.
set timeout -1
# Open an ftp session to a remote server, and wait for a username prompt.
spawn ftp $remote_server
expect "username:"
# Send the username, and then wait for a password prompt.
send "$my_user_id\r"
expect "password:"
# Send the password, and then wait for an ftp prompt.
send "$my_password\r"
expect "ftp>"
# Switch to binary mode, and then wait for an ftp prompt.
send "bin\r"
expect "ftp>"
# Turn off prompting.
send "prompt\r"
expect "ftp>"
# Get all the files
send "mget *\r"
expect "ftp>"
# Exit the ftp session, and wait for a special end-of-file character.
send "bye\r"
expect eof
```

아래는 (비밀번호와 함께) SFTP를 자동화하는 예이다:

``` tcl
#!/usr/bin/env expect -f

# procedure to attempt connecting; result 0 if OK, 1 otherwise
proc connect {passw} {
  expect {
    "Password:" {
      send "$passw\r"
        expect {
          "sftp*" {
            return 0
          }
        }
    }
  }
  # timed out
  return 1
}

#read the input parameters
set user [lindex $argv 0]
set passw [lindex $argv 1]
set host [lindex $argv 2]
set location [lindex $argv 3]
set file1 [lindex $argv 4]
set file2 [lindex $argv 5]

#puts "Argument data:\n";
#puts "user: $user";
#puts "passw: $passw";
#puts "host: $host";
#puts "location: $location";
#puts "file1: $file1";
#puts "file2: $file2";

#check if all were provided
if { $user == "" || $passw == "" || $host == "" || $location == "" || $file1 == "" || $file2 == "" } {
  puts "Usage: <user> <passw> <host> <location> <file1 to send> <file2 to send>\n"
  exit 1
}

#sftp to specified host and send the files
spawn sftp $user@$host

set rez [connect $passw]
if { $rez == 0 } {
  send "cd $location\r"
  set timeout -1
  send "put $file2\r"
  send "put $file1\r"
  send "ls -l\r"
  send "quit\r"
  expect eof
  exit 0
}
puts "\nError connecting to server: $host, user: $user and password: $passw!\n"
exit 1
```

이 예에서처럼 명령 줄 인수로 비밀번호를 사용하는 것은 커다란 보안 구멍인데, 해당 머신의 다른 사용자가 [ps를](../Page/Ps_\(유닉스\).md "wikilink") 실행함으로써 이 비밀번호를 읽어낼 수 있다. 그러나 인수로 비밀번호를 지정하지 않고 비밀번호를 직접 물어보게 하는 코드를 추가할 수 있다. 이것이 더 안전한 편이다. 아래의 예를 참고할 것.

``` tcl
stty -echo
send_user -- "Enter Password: "
expect_user -re "(.*)\n"
send_user "\n"
stty echo
set PASS $expect_out(1,string)
```

사용자 머신에서 자동화하는 ssh 로그인의 다른 예는 다음과 같다:

``` tcl
#timeout is a predefined variable in expect which by default is set to 10 sec
#spawn_id is another default variable in expect.
#It is good practice to close spawn_id handle created by spawn command
set timeout 60
spawn ssh $user@machine
while {1} {
  expect {

    eof                          {break}
    "The authenticity of host"   {send "yes\r"}
    "password:"                  {send "$password\r"}
    "*\]"                        {send "exit\r"}
  }
}
wait
close $spawn_id
```

## 대안

C\#, 자바, 스칼라, 그루비, 펄, 파이썬, 루비, 셸, Go와 같은 다른 언어로 된 다양한 프로젝트는 Expect와 같은 기능을 구현한다. 이들은 일반적으로 원래의 Expect의 복제물은 아니지만 유사한 개념의 양상을 보인다.

### C\#

  - [Expect.NET](https://web.archive.org/web/20131224094314/http://blog.iwanek.eu/expect-net/) — Expect functionality for C\# (.NET)
  - [DotNetExpect](https://github.com/CBonnell/dotnetexpect) — An Expect-inspired console automation library for .NET

### 자바

  - [expect4j](https://github.com/cverges/expect4j) — an attempt at a Java clone of the original Expect
  - [ExpectJ](http://expectj.sourceforge.net/) — a Java implementation of the Unix expect utility
  - [Expect-for-Java](https://github.com/ronniedong/Expect-for-Java) — pure Java implementation of the Expect tool
  - [expect4java](https://github.com/iTransformers/expect4java)  - a Java implementation of the Expect tool, but supports nested clousures. There is also wrapper for Groovy language DSL.

### 스칼라

  - [scala-expect](https://github.com/Lasering/scala-expect) — a Scala implementation of a very small subset of the Expect tool.

### 그루비

  - [expect4groovy](https://github.com/iTransformers/expect4groovy)  - a Groovy DSL implementation of Expect tool.

### 펄

  - [Expect.pm](http://sourceforge.net/projects/expectperl) — [펄](../Page/펄.md "wikilink") module (newest version at [metacpan.org](https://metacpan.org/pod/Expect))

### 파이썬

  - [Pexpect](https://github.com/pexpect/pexpect) — [Python](../Page/파이썬.md "wikilink") module for controlling interactive programs in a pseudo-terminal
  - [winpexpect](https://pypi.python.org/pypi/winpexpect) — port of pexpect to the Windows platform

### 루비

  - [RExpect](https://web.archive.org/web/20170311165445/http://rubyforge.org/projects/rexpect) — a drop in replacement for the expect.rb module in the standard library.
  - [Expect4r](https://github.com/jesnault/expect4r) — Interact with Cisco IOS, IOS-XR, and Juniper JUNOS CLI

### 셸

  - [Empty](http://empty.sourceforge.net) — expect-like utility to run interactive commands in the UNIX shell-scripts

### Go

  - [GoExpect](https://github.com/google/goexpect) - expect-like package for the Go language

## 각주

## 추가 문헌

  -
  - "[Advanced Programming in Expect: A Bulletproof Interface](https://web.archive.org/web/20180408033212/http://www.cotse.com/dlf/man/expect/bulletproof1.htm)"

## 외부 링크

  -
  -
  - [Expect page](http://wiki.tcl.tk/201) — on The Tcler's Wiki

  - [IBM Blog](https://www.ibm.com/developerworks/community/blogs/brian/entry/when_to_use_expect_scripting_and_when_to_avoid_it10?lang=en)

[분류:스크립트 언어](https://ko.wikipedia.org/wiki/분류:스크립트_언어 "wikilink") [분류:Tk](https://ko.wikipedia.org/wiki/분류:Tk "wikilink") [분류:자동화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자동화_소프트웨어 "wikilink")