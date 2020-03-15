> This article is converted from Wikipedia: [Fread](https://ko.wikipedia.org/wiki/Fread).


**fread** 함수는 스트림에서 바이너리 데이터를 읽어 버퍼에 저장하는 [표준 C 라이브러리](https://ko.wikipedia.org/wiki/표준_C_라이브러리 "wikilink") 함수이다.

## 정의

`<`[`stdio.h`](https://ko.wikipedia.org/wiki/stdio.h "wikilink")`>` 헤더 파일에 다음과 같이 정의되어 있다.

``` c
size_t fread (void * DstBuf, size_t ElementSize, size_t Count, FILE * FileStream)
```

### 인수

각 인수는 다음과 같은 의미를 가지고 있다.

  - `DstBuf`
    입력받은 데이터를 저장할 버퍼의 주소
  - `ElementSize`
    원소 1개의 크기
  - `Count`
    입력 받을 원소의 개수
  - `FileStream`
    [파일 스트림](https://ko.wikipedia.org/wiki/파일_스트림 "wikilink")

### 반환값

실제로 읽어들인 원소의 개수를 반환한다. 반환값이 `Count`보다 작으면 오류나 [파일 끝](https://ko.wikipedia.org/wiki/파일_끝 "wikilink")(EOF)의 경우이다.

## 동작

[파일 스트림으로부터](https://ko.wikipedia.org/wiki/파일_스트림 "wikilink") `ElementSize`크기의 바이너리 데이터를 `Count`회 읽어 `DstBuf`에 저장한다. `Count`회 입력이 완료되거나 [EOF를](https://ko.wikipedia.org/wiki/파일_끝 "wikilink") 입력받았을 때, 혹은 오류가 발생했을 때 입력을 마친다. 함수가 종료될 때 입력이 완료된 곳까지 [파일 포인터를](https://ko.wikipedia.org/wiki/파일_포인터 "wikilink") 이동시키고 실제로 읽어들인 원소의 개수를 반환한다.

## 예제

``` c
 #include <stdio.h>

 int main(void)
 {
     FILE *file_ptr;
     char arr[6];
     size_t iCount;

     file_ptr = fopen("sample.txt", "rb");
     if(file_ptr==NULL) return 1;

     iCount = fread(arr, sizeof(char), sizeof(arr), file_ptr);
     fclose(file_ptr);

     return 0;
 }
```

위 예제는 sample.txt에서 6바이트를 읽어(파일이 6바이트보다 크다는 가정 하에) `arr`에 저장하고 읽은 바이트 수를 `iCount`에 저장한다.

## 같이 보기

  - [`fwrite`](https://ko.wikipedia.org/wiki/fwrite "wikilink")

[분류:stdio.h](https://ko.wikipedia.org/wiki/분류:stdio.h "wikilink") [분류:C 표준 라이브러리](https://ko.wikipedia.org/wiki/분류:C_표준_라이브러리 "wikilink")