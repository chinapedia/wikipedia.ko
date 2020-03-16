> This article is converted from Wikipedia: [Cron](https://ko.wikipedia.org/wiki/Cron).


소프트웨어 유틸리티 **cron**은 [유닉스 계열](../Page/유닉스_계열.md "wikilink") 컴퓨터 [운영 체제의](../Page/운영_체제.md "wikilink") 시간 기반 [잡 스케줄러이다](https://ko.wikipedia.org/wiki/잡_스케줄러 "wikilink"). 소프트웨어 환경을 설정하고 관리하는 사람들은 작업을 고정된 시간, 날짜, 간격에 주기적으로 실행할 수 있도록 스케줄링하기 위해 cron을 사용한다.

## 개요

cron은 셸 명령어들이 주어진 일정에 주기적으로 실행하도록 규정해놓은 crontab (cron table) 파일에 의해 구동된다. crontab 파일들은 잡 목록 및 cron [데몬에](../Page/데몬_\(컴퓨팅\).md "wikilink") 대한 다른 명령들이 보관된 위치에 저장되어 있다. 사용자들은 자신들만의 개개의 crontab 파일들을 가질 수 있으며, 가끔은 /etc 또는 /etc의 하위 디렉터리에 시스템 관리자들만이 편집할 수 있는, 시스템 전반에 영향을 미치는 crontab 파일이 존재하는 경우도 있다.

### 예

다음은 cron 사용자의 기본 셸이 [본 셸](../Page/본_셸.md "wikilink") 호환이라는 가정 하에 매일 자정 이후 1분 째에 아파치 오류 로그를 삭제한다.

``` bash
1 0 * * *  printf > /var/log/apache/error_log
```

아래의 예는 매일 20시 (오후 8시)에 export_dump.sh라는 셸 프로그램을 실행한다.

``` bash
0 20 * * * /home/oracle/scripts/export_dump.sh
```

### 구성 파일

사용자를 위한 구성 파일은 *crontab -e*를 호출하여 편집할 수 있다.

이 파일의 문법은 다음과 같다:

```
 # ┌───────────── min (0 - 59)
 # │ ┌────────────── hour (0 - 23)
 # │ │ ┌─────────────── day of month (1 - 31)
 # │ │ │ ┌──────────────── month (1 - 12)
 # │ │ │ │ ┌───────────────── day of week (0 - 6) (0 to 6 are Sunday to Saturday, or use names; 7 is Sunday, the same as 0)
 # │ │ │ │ │
 # │ │ │ │ │
 # * * * * *  command to execute
```

## 같이 보기

  - [at (유닉스)](https://ko.wikipedia.org/wiki/at_\(유닉스\) "wikilink")
  - [스케줄링 (컴퓨팅)](../Page/스케줄링_\(컴퓨팅\).md "wikilink")
  - [유닉스 명령어 목록](../Page/유닉스_명령어_목록.md "wikilink")

## 외부 링크

  -
  - [GNU cron](http://www.gnu.org/software/mcron/) (mcron)

[분류:표준 유닉스 프로그램](https://ko.wikipedia.org/wiki/분류:표준_유닉스_프로그램 "wikilink") [분류:유닉스 SUS2008 유틸리티](https://ko.wikipedia.org/wiki/분류:유닉스_SUS2008_유틸리티 "wikilink") [분류:유닉스 프로세스 및 작업 관리 관련 소프트웨어](https://ko.wikipedia.org/wiki/분류:유닉스_프로세스_및_작업_관리_관련_소프트웨어 "wikilink")