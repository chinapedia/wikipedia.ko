> This article is converted from Wikipedia: [Pstree](https://ko.wikipedia.org/wiki/Pstree).


[섬네일에서의](https://ko.wikipedia.org/wiki/파일:Pstree_freebsd.png "wikilink") pstree 출력.\]\] **pstree**는 실행 중인 프로세스를 [트리](https://ko.wikipedia.org/wiki/트리 "wikilink")형태로 보여주는 유닉스 명령어이다. 이 명령은 [ps](https://ko.wikipedia.org/wiki/ps "wikilink") 명령어보다 더욱 시각적으로 보기 좋다. 트리의 루트는 [init 프로세스가](https://ko.wikipedia.org/wiki/init_프로세스 "wikilink") 되거나 사용자가 지정한 프로세스가 된다.

## 예

**pstree pid**

``` console
user@host ~$ pstree 1066
rsyslogd─┬─{in:imjournal}
         └─{rs:main Q:Reg}
```

**pstree username**

``` console
user@host ~# pstree username
dbus-daemon───{dbus-daemon}

dbus-launch

bash───firefox─┬─6*[{Analysis Helper}]
               ├─{BgHangManager}
               ├─{Cache2 I/O}
               ├─{Compositor}
               ├─{GMPThread}
               ├─{Gecko_IOThread}
               ├─{Hang Monitor}
               ├─{ImageBridgeChil}
               ├─{ImageIO}
               ├─{JS Watchdog}
               ├─{Link Monitor}
               ├─{Socket Thread}
               ├─{SoftwareVsyncTh}
               ├─{StreamTrans #1}
               ├─{Timer}
               └─{gmain}
```

## 외부 링크

  - [The psmisc package](http://psmisc.sourceforge.net/)

  - [The pstree Command](http://www.linfo.org/pstree.html) by The Linux Information Project (LINFO)

  - [Gnome Process Tree](http://gnopstree.sourceforge.net/)

  -
[분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")