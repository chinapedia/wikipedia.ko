> This article is converted from Wikipedia: [Cgroups](https://ko.wikipedia.org/wiki/Cgroups).


**cgroups**(control groups의 약자)는 [프로세스](https://ko.wikipedia.org/wiki/프로세스 "wikilink")들의 [자원의 사용](https://ko.wikipedia.org/wiki/시스템_자원 "wikilink")(CPU, 메모리, 디스크 입출력, 네트워크 등)을 제한하고 격리시키는 [리눅스 커널](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 기능이다.

[구글](https://ko.wikipedia.org/wiki/구글 "wikilink")의 엔지니어들이 2006년에 이 기능에 대한 작업에 착수하였고 당시 이름은 "프로세스 컨테이너"(process container)였다.\[1\] 2007년 말에 리눅스 커널 문맥에서 "컨테이너"라는 용어의 의미가 여러 개이므로 혼란을 방지하기 위해 이름이 "컨트롤 그룹"(control groups)으로 변경되었으며, 컨트롤 그룹 기능은 2008년 1월에 출시된 커널 버전 2.6.24에 [리눅스 커널 메인라인으로](https://ko.wikipedia.org/wiki/리눅스_커널 "wikilink") 병합되었다.\[2\] 그 뒤로 개발자들은 수많은 새로운 기능과 컨트롤러들을 추가해오고 있는데, 이를테면 [kernfs](https://ko.wikipedia.org/wiki/kernfs "wikilink") 지원,\[3\] [방화벽](https://ko.wikipedia.org/wiki/방화벽 "wikilink"),\[4\] 통합된 계층구조를 포함한다.\[5\]

## 채택

다양한 프로젝트들이 cgroups를 기반으로 사용하고 있으며, 여기에는 [코어OS](https://ko.wikipedia.org/wiki/코어OS "wikilink"), [도커](../Page/도커_\(소프트웨어\).md "wikilink"), [하둡](https://ko.wikipedia.org/wiki/아파치_하둡 "wikilink"), [Jelastic](https://ko.wikipedia.org/wiki/Jelastic "wikilink"), [Kubernetes](https://ko.wikipedia.org/wiki/Kubernetes "wikilink"),\[6\] [lmctfy](https://ko.wikipedia.org/wiki/lmctfy "wikilink") (Let Me Contain That For You), [LXC](../Page/LXC.md "wikilink") (리눅스 컨테이너/LinuX Containers), systemd, [Mesos](https://ko.wikipedia.org/wiki/Apache_Mesos "wikilink"), Mesosphere,\[7\] [HTCondor](https://ko.wikipedia.org/wiki/HTCondor "wikilink") 등이 있으며 메인라인 리눅스 커널에 채택된지 3년이 지난 2010년 11월에 [레드햇 엔터프라이즈 리눅스](https://ko.wikipedia.org/wiki/레드햇_엔터프라이즈_리눅스 "wikilink") 6과 같은 주요 리눅스 배포판에도 또한 채택되었다.\[8\]

## 같이 보기

  - [운영 체제 수준 가상화](../Page/운영_체제_수준_가상화.md "wikilink")
  - [프로세스 그룹](https://ko.wikipedia.org/wiki/프로세스_그룹 "wikilink")

## 각주

## 외부 링크

  - [Linux kernel documentation on cgroups](https://www.kernel.org/doc/Documentation/cgroup-v2.txt)
  - [Linux kernel Namespaces and cgroups by Rami Rosen](http://www.haifux.org/lectures/299/netLec7.pdf)
  - [Namespaces and cgroups, the basis of Linux containers (including cgroups v2)](http://www.netdevconf.org/1.1/proceedings/slides/rosen-namespaces-cgroups-lxc.pdf), slides of a talk by Rami Rosen, Netdev 1.1, Seville, Spain, 2016
  - \[//lwn.net/Articles/679786 Understanding the new control groups API\], [LWN.net](../Page/LWN.net.md "wikilink"), by Rami Rosen, March 2016
  - [Large-scale cluster management at Google with Borg](https://static.googleusercontent.com/media/research.google.com/en/us/pubs/archive/43438.pdf), April 2015, by Abhishek Verma, Luis Pedrosa, Madhukar Korupolu, David Oppenheimer, Eric Tune and John Wilkes
  - \[<https://msdn.microsoft.com/en-us/library/windows/desktop/ms684161(v=vs.85>).aspx Job Objects\], similar feature on Windows

[분류:리눅스 커널의 인터페이스](https://ko.wikipedia.org/wiki/분류:리눅스_커널의_인터페이스 "wikilink") [분류:리눅스 커널 특징](https://ko.wikipedia.org/wiki/분류:리눅스_커널_특징 "wikilink") [분류:운영 체제 보안](https://ko.wikipedia.org/wiki/분류:운영_체제_보안 "wikilink")

1.
2.
3.
4.
5.
6.
7.
8.  <https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/pdf/6.0_Release_Notes/Red_Hat_Enterprise_Linux-6-6.0_Release_Notes-en-US.pdf>