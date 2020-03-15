> This article is converted from Wikipedia: [FTPS](https://ko.wikipedia.org/wiki/FTPS).


**FTPS**(FTP Secure, FTP-SSL, FTPES, S-FTP)는 일반적으로 쓰이는 [파일 전송 프로토콜](https://ko.wikipedia.org/wiki/파일_전송_프로토콜 "wikilink")(FTP)의 확장으로, 기존의 FTP에 [전송 계층 보안](https://ko.wikipedia.org/wiki/전송_계층_보안 "wikilink")(TLS)과 [보안 소켓 계층](https://ko.wikipedia.org/wiki/전송_계층_보안 "wikilink")(SSL) 암호화 프로토콜에 대한 지원이 추가되었다.

FTPS는 [SSH 파일 전송 프로토콜](../Page/SSH_파일_전송_프로토콜.md "wikilink")(SFTP)나 [파일 전송 프로토콜](https://ko.wikipedia.org/wiki/시큐어_FTP "wikilink")(Secure FTP)와는 다르다.

## 배경

파일 전송 프로토콜은 1971년 [아파넷](https://ko.wikipedia.org/wiki/아파넷 "wikilink")이라는 과학 연구 네트워크에 사용할 목적으로 초안이 작성되었다.\[1\] 당시 아파넷의 접근이 소수의 군사 지역과 대학교, 프로토콜 내의 데이터 보안 및 개인 정보 요구 없이 운영이 가능한 조그마한 사용자 커뮤니티에 국한되었다.

1994년 인터넷 브라우저 회사 [넷스케이프](https://ko.wikipedia.org/wiki/넷스케이프 "wikilink")는 [애플리케이션 계층](https://ko.wikipedia.org/wiki/애플리케이션_계층 "wikilink") 래퍼 [보안 소켓 레이어를](https://ko.wikipedia.org/wiki/전송_계층_보안 "wikilink") 개발, 출시하였다.\[2\] 이 프로토콜은 개인화된 안전한 방식으로 애플리케이션들이 네트워크를 통해 통신할 수 있게 하였다. [TCP와](https://ko.wikipedia.org/wiki/전송_제어_프로토콜 "wikilink") 같은 신뢰할 수 있는 연결을 사용하는 프로토콜에 보안을 추가할 수 있었지만, HTTP를 가지고 HTTPS를 형성하기 위해 넷스케이프에 흔히 사용되었다.

1996년 말 [RFC](https://ko.wikipedia.org/wiki/RFC "wikilink")의 초안 출판과 더불어 SSL 프로토콜이 마침내 FTP에 적용되었다.\[3\] 그 직후 공식 [IANA](https://ko.wikipedia.org/wiki/IANA "wikilink") 포트가 등록되었다. 그러나 RFC는 2005년까지도 완성되지는 못했다.\[4\]

## 같이 보기

  - [시큐어 카피](https://ko.wikipedia.org/wiki/시큐어_카피 "wikilink")
  - [SSH 파일 전송 프로토콜](../Page/SSH_파일_전송_프로토콜.md "wikilink") (SFTP)

## 각주

<references />

## 외부 링크

  - [Overview of FTPS, and lists of clients, servers, and proxies supporting FTPS](http://www.ford-hutchinson.com/~fh-1-pfh/ftps-ext.html)

[분류:네트워크 파일 전송 프로토콜](https://ko.wikipedia.org/wiki/분류:네트워크_파일_전송_프로토콜 "wikilink") [분류:전송 계층 보안](https://ko.wikipedia.org/wiki/분류:전송_계층_보안 "wikilink")

1.  [RFC-265: File Transfer Protocol (FTP)](http://tools.ietf.org/html/rfc265)
2.  [The SSL Protocol, Feb. 9th, 1995](http://www.mozilla.org/projects/security/pki/nss/ssl/draft02.html)
3.  [RFC draft, Secure FTP Over SSL, revision 1996-11-26](http://tools.ietf.org/id/draft-murray-auth-ftp-ssl-00.txt)
4.  [RFC-4217: Securing FTP with TLS](https://ko.wikipedia.org/wiki/rfc:4217 "wikilink")