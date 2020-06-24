> This article is converted from Wikipedia: [Dig](https://ko.wikipedia.org/wiki/Dig).


**dig** (domain information groper)는 [도메인 네임 시스템](../Page/도메인_네임_시스템.md "wikilink") (DNS) [네임서버](https://ko.wikipedia.org/wiki/네임서버 "wikilink")에 질의하기 위한 네트워크 관리 [명령 줄 인터페이스](../Page/명령_줄_인터페이스.md "wikilink") 툴이다.

dig는 네트워크 트러블슈팅과 교육적인 목적에 유용하다. dig는 반복적인 명령 줄 모드 또는 배치 모드에서 작동할 수 있다. 특정한 네임 서버가 명령에 명시되지 않으면, 이것은 [resolv.conf](https://ko.wikipedia.org/wiki/resolv.conf "wikilink") 파일에 설정된 운영 체제 기본 resolver를 사용한다. 쿼리에 매개변수가 없으면 DNS 루트 존에 질의한다.

dig는 [국제화 도메인 네임](https://ko.wikipedia.org/wiki/국제화_도메인_네임 "wikilink") (IDN) 질의를 지원한다.

dig는 BIND 도메인 네임 서버 소프트웨어의 한 부분이다. dig는 [nslookup](https://ko.wikipedia.org/wiki/nslookup "wikilink")과 host 같은 오래된 툴들을 대체한다.

## 사용 예시

아래의 예시에서 dig는 도메인 example.com에서 레코드 정보의 any 타입을 질의하기 위해 사용된다.

``` console
$ dig example.com any
; <<>> DiG 9.6.1 <<>> example.com any
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 4016
;; flags: qr rd ra; QUERY: 1, ANSWER: 4, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;example.com.                   IN      ANY

;; ANSWER SECTION:
example.com.            172719  IN      NS      a.iana-servers.net.
example.com.            172719  IN      NS      b.iana-servers.net.
example.com.            172719  IN      A       208.77.188.166
example.com.            172719  IN      SOA     dns1.icann.org. hostmaster.icann.org. 2007051703 7200 3600 1209600 86400

;; Query time: 1 msec
;; SERVER: ::1#53(::1)
;; WHEN: Wed Aug 12 11:40:43 2009
;; MSG SIZE  rcvd: 154
```

숫자 172719는 [Time to live](../Page/Time_to_live.md "wikilink") 값을 보여준다.

질의들은 특정한 레코드를 위해 지정된 DNS 서버로 보내질 수 있다; 여기서는, MX records:

``` console
$ dig wikimedia.org MX @ns0.wikimedia.org
; <<>> DiG 9.6.1 <<>> wikimedia.org MX @ns0.wikimedia.org
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 61144
;; flags: qr aa rd; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 2
;; WARNING: recursion requested but not available

;; QUESTION SECTION:
;wikimedia.org.                 IN      MX

;; ANSWER SECTION:
wikimedia.org.          3600    IN      MX      10 mchenry.wikimedia.org.
wikimedia.org.          3600    IN      MX      50 lists.wikimedia.org.

;; ADDITIONAL SECTION:
mchenry.wikimedia.org.  3600    IN      A       208.80.152.186
lists.wikimedia.org.    3600    IN      A       91.198.174.5

;; Query time: 73 msec
;; SERVER: 208.80.152.130#53(208.80.152.130)
;; WHEN: Wed Aug 12 11:51:03 2009
;; MSG SIZE  rcvd: 109
```

## 같이 보기

  - DNS 레코드 타입 목록
  - [nslookup](https://ko.wikipedia.org/wiki/nslookup "wikilink")
  - [후이즈](../Page/후이즈.md "wikilink")
  - [host (유닉스)](https://ko.wikipedia.org/wiki/host_\(유닉스\) "wikilink")

## 각주

Paul Albitz and Cricket Liu. DNS and BIND, 5th Edition. Nutshell Series. O'Reilly and Associates, Inc., 2006.

## 외부 링크

  - [How to use dig to query DNS name servers](http://www.madboa.com/geek/dig/)

[분류:도메인 네임 시스템](https://ko.wikipedia.org/wiki/분류:도메인_네임_시스템 "wikilink")