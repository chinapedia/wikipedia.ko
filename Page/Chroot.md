> This article is converted from Wikipedia: [Chroot](https://ko.wikipedia.org/wiki/Chroot).


[유닉스](https://ko.wikipedia.org/wiki/유닉스 "wikilink") [운영 체제에서](https://ko.wikipedia.org/wiki/운영_체제 "wikilink") **chroot**는 현재 실행 중인 프로세스와 [차일드 프로세스](https://ko.wikipedia.org/wiki/차일드_프로세스 "wikilink") 그룹에서 [루트 디렉터리를](https://ko.wikipedia.org/wiki/루트_디렉터리 "wikilink") 변경하는 작업이다.

이렇게 수정된 환경에서 실행되는 프로그램은 지정된 디렉터리 트리 밖의 파일들의 이름을 지정할 수 없으므로(즉, 일반적으로는 접근이 불가능하므로) chroot 감옥으로 부른다. chroot는 chroot(2) [시스템 호출이나](https://ko.wikipedia.org/wiki/시스템_호출 "wikilink") chroot(8) 래퍼 프로그램을 가리킬 수 있다.

## 역사

chroot 시스템 호출은 1979년 버전 7 유닉스의 개발 중에 도입되었으며, 1982년 3월 18일 [빌 조이가](https://ko.wikipedia.org/wiki/빌_조이 "wikilink") BSD에 추가하였다.

## 이용 목적

chroot는 다음의 목적에 유용하게 쓰일 수 있다:

  - 테스트 및 개발
  - 의존성 제어
  - 호환성
  - 복구
  - 권한 분리

## 리눅스 호스트 커널 가상 파일 시스템 및 구성 파일

리눅스에서 chroot 환경을 사용하려면 커널 가상 파일 시스템과 구성 파일 또한 host에서 chroot로 마운트/복사되어야 한다.

``` sh
# Mount Kernel Virtual File Systems
TARGETDIR="/mnt/chroot"
mount -t proc proc $TARGETDIR/proc
mount -t sysfs sysfs $TARGETDIR/sys
mount -t devtmpfs devtmpfs $TARGETDIR/dev
mount -t tmpfs tmpfs $TARGETDIR/dev/shm
mount -t devpts devpts $TARGETDIR/dev/pts

# Copy /etc/hosts
/bin/cp -f /etc/hosts $TARGETDIR/etc/

# Copy /etc/resolv.conf
/bin/cp -f /etc/resolv.conf $TARGETDIR/etc/resolv.conf

# Link /etc/mtab
chroot $TARGETDIR rm /etc/mtab 2> /dev/null
chroot $TARGETDIR ln -s /proc/mounts /etc/mtab
```

## chroot 상의 그래픽 응용 프로그램

다음의 방식을 이용하여 chroot로 된 환경에서 그래픽 응용 프로그램을 구동할 수 있다.\[1\]\[2\]

  - [xhost](https://ko.wikipedia.org/wiki/xhost "wikilink")
  - [Xnest](https://ko.wikipedia.org/wiki/Xnest "wikilink") 또는 더 현대적인 [Xephyr](https://ko.wikipedia.org/wiki/Xephyr "wikilink")
  - X11 포워드 (ssh-X) 기능을 이용하여 chroot [SSH](https://ko.wikipedia.org/wiki/시큐어_셸 "wikilink") 접근
  - [xchroot](http://www.elstel.org/xchroot/)
  - X11 [VNC](https://ko.wikipedia.org/wiki/VNC "wikilink") 서버 및 환경 외 VNC 클라이언트 접속

## 같이 보기

  - [sudo](https://ko.wikipedia.org/wiki/sudo "wikilink")
  - [샌드박스 (컴퓨터 보안)](https://ko.wikipedia.org/wiki/샌드박스_\(컴퓨터_보안\) "wikilink")

## 각주

<references />

## 외부 링크

  -
  -
  -
  - [Integrating GNU/Linux with Android using chroot](http://whiteboard.ping.se/Android/Debian)

[분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink") [분류:가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:가상화_소프트웨어 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:시스템 호출](https://ko.wikipedia.org/wiki/분류:시스템_호출 "wikilink") [분류:자유 가상화 소프트웨어](https://ko.wikipedia.org/wiki/분류:자유_가상화_소프트웨어 "wikilink")

1.  <http://wiki.mandriva.com/en/Development/Howto/Chroot#Launch_X_Applications_inside_the_chroot>
2.