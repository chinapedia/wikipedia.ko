> This article is converted from Wikipedia: [Rsync](https://ko.wikipedia.org/wiki/Rsync).


**rsync**는 컴퓨터 시스템 상에서 파일을 효율적으로 전송하고 동기화하기 위한 유틸리티의 하나로, 파일의 타임스탬프와 크기를 검사함으로써 이루어진다.\[1\] [파일 동기화와](https://ko.wikipedia.org/wiki/파일_동기화 "wikilink") [파일 전송](https://ko.wikipedia.org/wiki/파일_전송 "wikilink") 프로그램으로 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 시스템과 함수에서 흔히 볼 수 있다. rsync 알고리즘은 [델타 인코딩의](https://ko.wikipedia.org/wiki/델타_인코딩 "wikilink") 일종이며 네트워크 이용률을 최소화하기 위해 사용된다. [Zlib](../Page/Zlib.md "wikilink")을 사용하여 추가적인 [데이터 압축을](../Page/데이터_압축.md "wikilink") 하는데 사용할 수 있으며,\[2\] [SSH이나](../Page/시큐어_셸.md "wikilink") [stunnel](https://ko.wikipedia.org/wiki/stunnel "wikilink")은 데이터 보안을 위해 사용할 수 있다.

Rsync는 일반적으로 서로 다른 두 개의 시스템 간에 파일과 디렉터리를 동기화하기 위해 사용된다. 이를테면 `rsync local-file user@remote-host:remote-file`를 사용하면 rsync는 SSH를 사용하여 `user` 자격으로 `remote-host`에 접속하게 된다.\[3\] 연결이 되면 원격 호스트의 rsync를 호출한 다음 두 개의 프로그램이 전송이 필요한 로컬 파일의 일부를 결정함으로써 원격 파일이 로컬 파일과 일치할 수 있게 된다.

Rsync는 [데몬](../Page/데몬_\(컴퓨팅\).md "wikilink") 모드로도 동작이 가능하며 네이티브 rsync 프로토콜로 파일을 서비스하고 수신할 수 있다. ("<rsync://>" 문법 사용).

[GNU GPLv](../Page/GNU_일반_공중_사용_허가서.md "wikilink")3로 배포되었다.\[4\]\[5\]\[6\]\[7\]

## rsync 응용 프로그램

<table>
<thead>
<tr class="header">
<th><p>프로그램</p></th>
<th><p>운영 체제</p></th>
<th></th>
<th><p>설명</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>리눅스</p></td>
<td><p>macOS</p></td>
<td><p>윈도우</p></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Back_In_Time" title="wikilink">Back In Time</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/BackupAssist" title="wikilink">BackupAssist</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/cwRsync" title="wikilink">cwRsync</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/Grsync" title="wikilink">Grsync</a></p></td>
<td></td>
<td></td>
<td><p>[8]</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://ko.wikipedia.org/wiki/GS_RichCopy_360" title="wikilink">GS RichCopy 360</a></p></td>
<td></td>
<td></td>
<td><p>[9]</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://ko.wikipedia.org/wiki/LuckyBackup" title="wikilink">LuckyBackup</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><a href="https://rclone.org/">Rclone</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><a href="../Page/Robocopy.md" title="wikilink">Robocopy</a></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## 같이 보기

  - [casync](https://ko.wikipedia.org/wiki/casync "wikilink")
  - [원격 차분 압축](https://ko.wikipedia.org/wiki/원격_차분_압축 "wikilink")
  - [TCP/UDP의 포트 목록](https://ko.wikipedia.org/wiki/TCP/UDP의_포트_목록 "wikilink")

## 각주

## 외부 링크

  -
  - [rsync algorithm](http://rsync.samba.org/tech_report/) - 1998-11-09

[분류:1996년 소프트웨어](https://ko.wikipedia.org/wiki/분류:1996년_소프트웨어 "wikilink") [분류:데이터 동기화](https://ko.wikipedia.org/wiki/분류:데이터_동기화 "wikilink") [분류:네트워크 파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_파일_전송_프로토콜 "wikilink") [분류:유닉스 네트워크 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_네트워크_관련_소프트웨어 "wikilink") [분류:자유 백업 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_백업_소프트웨어 "wikilink")

1.
2.
3.
4.
5.
6.  Rasch, David; Burns, Randal; [*In-Place Rsync: File Synchronization for Mobile and Wireless Devices*](http://hssl.cs.jhu.edu/ip-rsync/ip-rsync.pdf) , Department of Computer Science, Johns Hopkins University
7.
8.  [Grsync for Windows](http://grsync-win.sourceforge.net/)
9.  [GS RichCopy 360 Enterprise for Windows](http://www.gurusquad.com/Replication/GSRichCopy360Enterprise/)