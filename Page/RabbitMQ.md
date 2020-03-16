> This article is converted from Wikipedia: [RabbitMQ](https://ko.wikipedia.org/wiki/RabbitMQ).


[섬네일](https://ko.wikipedia.org/wiki/파일:Wmcs_dns.pdf "wikilink") **RabbitMQ**는 오픈 소스 [메시지 브로커](../Page/메시지_브로커.md "wikilink") 소프트웨어([메시지 지향 미들웨어](../Page/메시지_지향_미들웨어.md "wikilink"))로서, [AMQP](../Page/AMQP.md "wikilink")를 구현하였으며 그 이후로 [STOMP](https://ko.wikipedia.org/wiki/STOMP "wikilink") ,[MQTT](../Page/MQTT.md "wikilink") 등의 프로토콜을 지원하기 위해 [플러그인](../Page/플러그인.md "wikilink") 구조와 함께 확장되고 있다.

메시지를 생산하는 생산자(Producer)가 메시지를 큐에 저장해 두면, 메시지를 수신하는 소비자(Consumer)가 메시지를 가져와 처리하는 Publish/Subscribe 방식의 메시지 전달 브로커이다.

## 예

### 송신

``` python
#!/usr/bin/env python
import pika
connection = pika.BlockingConnection(pika.ConnectionParameters(host='localhost'))
channel = connection.channel()
channel.queue_declare(queue='hello')
channel.basic_publish(exchange='', routing_key='hello', body='Hello World!')
print(" [x] Sent 'Hello World!'")
connection.close()
```

### 수신

``` python
#!/usr/bin/env python
import pika
connection = pika.BlockingConnection(pika.ConnectionParameters(host='localhost'))
channel = connection.channel()
channel.queue_declare(queue='hello')
print(' [*] Waiting for messages. To exit press CTRL+C')
def callback(ch, method, properties, body):
    print(" [x] Received %r" % body)
channel.basic_consume('hello', callback)
channel.start_consuming()
```

## 외부 링크

  -
[분류:메시지 지향 미들웨어](https://ko.wikipedia.org/wiki/분류:메시지_지향_미들웨어 "wikilink") [분류:모질라 라이선스 소프트웨어](https://ko.wikipedia.org/wiki/분류:모질라_라이선스_소프트웨어 "wikilink")