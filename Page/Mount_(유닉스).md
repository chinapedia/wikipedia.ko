> This article is converted from Wikipedia: [Mount \(유닉스\)](https://ko.wikipedia.org/wiki/Mount_\(유닉스\)).


사용자가 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 머신에서 [파일에](../Page/컴퓨터_파일.md "wikilink") 접근하려면 그에 앞서 파일을 포함하고 있는 [파일 시스템을](../Page/파일_시스템.md "wikilink") **mount** 명령어를 이용하여 마운트된 상태여야 한다. **mount**는 [SD 카드](../Page/SD_카드.md "wikilink"), [USB 저장소](../Page/USB_대용량_저장소_장치_유형.md "wikilink"), [DVD](../Page/DVD.md "wikilink"), 기타 이동식 저장소에 자주 사용된다.

mount 명령어는 [운영 체제에게](../Page/운영_체제.md "wikilink") [파일 시스템이](../Page/파일_시스템.md "wikilink") 사용 준비가 되어있음을 지시하고 이를 전반 파일 시스템 계층 구조(마운트 지점)에 있는 특정 지점에 연결시킨 다음, 접근에 관련한 옵션을 설정한다. 마운트를 통해 파일 시스템, 파일, 디렉터리, 장치, 특수 파일을 사용자가 사용할 수 있게 한다. 이와 반대되는 명령어인 **umount**는 운영 체제에게 파일 시스템을 마운트 지점으로부터 연결을 해제할 것을 지시하며 컴퓨터로부터 분리되어 더 이상 접근을 하지 못하게 한다.

mount와 umount 명령어는 변경 사항을 적용하기 위해서는 [루트 사용자](https://ko.wikipedia.org/wiki/루트_사용자 "wikilink") 권한이 필요하다. 루트 사용자는 `/etc/`[`fstab`](https://ko.wikipedia.org/wiki/fstab "wikilink") 파일에서 마운트 가능한 사용자에 대해 파일 시스템을 지정할 수 있다.

## 사용법

마운트된 모든 파티션 보기:

``` console
$ mount
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
/dev/sda1 on /boot type ext3 (rw)
/tmp on /var/tmp type none (rw,noexec,nosuid,bind)
10.4.0.4:/srv/export/setup_server on /nfs/setup_server type nfs (ro,addr=10.4.0.4)
```

아래의 예는 HDD(하드 디스크 드라이브)의 두 번째 파티션을 마운트한다:

``` bash
$ mount /dev/hda2 /media/PHOTOS
```

마운트를 해제하는 명령은 다음과 같다 (물리 디스크 파티션 해제):

``` bash
$ umount /dev/hda2
```

(마운트 지점을 가리켜 해제):

``` bash
$ umount /media/PHOTOS
```

특정 옵션을 사용하여 파티션을 다시 마운트하려면 다음과 같이 입력한다:

``` bash
$ mount -o remount,rw /dev/hda2
```

## 같이 보기

  - [마운트](https://ko.wikipedia.org/wiki/마운트 "wikilink")

## 외부 링크

  -
  -
  -
  -
  -
[분류:유닉스 파일 시스템 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_파일_시스템_관련_소프트웨어 "wikilink")