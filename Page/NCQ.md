> This article is converted from Wikipedia: [NCQ](https://ko.wikipedia.org/wiki/NCQ).


[섬네일](https://ko.wikipedia.org/wiki/파일:NCQ.svg "wikilink") **NCQ**(Native Command Queuing)은 특정 상황에서 SATA 장치의 성능을 향상시키기 위해 도입된 기술로, 입출력(I/O) 요청을 우선 큐에 보관한 다음, 전체 헤드의 움직임을 최소화할 수 있도록 요청의 순서를 재배열한 다음 실행하는 방식이다. 이 방식은 I/O가 많이 일어나는 서버 등의 장비에 주로 사용된다.

## 역사

NCQ는 [PATA](https://ko.wikipedia.org/wiki/PATA "wikilink")와 [SCSI](../Page/SCSI.md "wikilink")에 사용되던 [TCQ](https://ko.wikipedia.org/wiki/TCQ "wikilink")에서 유래한다.

## 원리

PATA TCQ와 크게 다르지는 않다. 골자는 큐에 I/O 요청을 보관하고 전체 헤드의 움직임을 최소화할 수 있는 최적의 경로로 재배열해서 실행하는 것이다. 최대 큐 길이는 32 명령어이다 (실제 이용되는 것은 31개)\[1\]\[2\].

## 효과

헤드의 움직임이 줄어들게 되므로 물리적 마모가 줄어들고 내구성이 좋아져 [MTBF](https://ko.wikipedia.org/wiki/MTBF "wikilink") 가 길어지는 효과가 있다.

NCQ는 많은 I/O 수의 부하에서는 성능에 상당히 긍정적인 효과가 있다.\[3\]\[4\] 그러나 순수 대역폭에 손해를 보며 개인용 컴퓨터 수준의 낮은 I/O 수의 부하에서는 성능이 떨어지는 경우가 많아서 기본적으로 사용하지 않는 경우가 많다.

## 참조

<references />

[분류:컴퓨터 버스](https://ko.wikipedia.org/wiki/분류:컴퓨터_버스 "wikilink") [분류:기억 장치](https://ko.wikipedia.org/wiki/분류:기억_장치 "wikilink")

1.  [PDF white paper on NCQ from Intel and Seagate](http://www.seagate.com/content/pdf/whitepaper/D2c_tech_paper_intc-stx_sata_ncq.pdf)
2.  [Volume 1 of the final draft of the ATA-7 standard](http://www.t13.org/Documents/UploadedDocuments/docs2004/d1532v1r4b-ATA-ATAPI-7.pdf)
3.
4.