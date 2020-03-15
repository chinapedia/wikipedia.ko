> This article is converted from Wikipedia: [S.M.A.R.T.](https://ko.wikipedia.org/wiki/S.M.A.R.T.).


**S.M.A.R.T.**(, "자가 진단, 분석, 보고 기술", 간단히 SMART)는 [컴퓨터](../Page/컴퓨터.md "wikilink") [하드 디스크 드라이브의](https://ko.wikipedia.org/wiki/하드_디스크_드라이브 "wikilink") 신뢰성을 검사하여 잠재적인 실패 가능성을 진단, 보고하는 감시 체계이다.

S.M.A.R.T가 실패를 예측할 때 사용자는 드라이브를 교체하여 예기치 않은 과전압 문제나 데이터 손실을 막을 수 있다. 제조업체는 S.M.A.R.T. 데이터를 이용하여 문제 여부를 발견하고 추후의 드라이브 설계시 참고하여 이를 예방할 수 있다.

## 배경

[하드 디스크 실패는](https://ko.wikipedia.org/wiki/하드_디스크_드라이브_실패 "wikilink") 두 가지 기본 분류 가운데 하나에 기인한다:

  - 저장소 표면의 기계적 마모, 점진적 감손과 같은 느린 처리로 인한 예측할 수 있는 실패가 일어날 수 있다. 모니터링을 통해 이러한 실패가 일어날 가능성이 있는지 결정할 수 있다.
  - 아무런 경고 없이 예측할 수 없는 실패가 갑자기 일어날 수 있다. 전자 부품의 결함에서부터 갑작스런 기계적 실패(부적절한 관리로 인한 가능성)에 이르기까지 범위는 다양하다.

기계적인 문제가 모든 드라이브 실패의 약 60%를 차지한다.\[1\]

## 알려진 ATA S.M.A.R.T. 특성

| [12px](https://ko.wikipedia.org/wiki/파일:Dark_Green_Arrow_Up.svg "wikilink")   | 높은 값일수록 좋음                     |
| ----------------------------------------------------------------------------- | ------------------------------ |
| [12px](https://ko.wikipedia.org/wiki/파일:Dark_Green_Arrow_Down.svg "wikilink") | 낮은 값일수록 좋음                     |
| **위험: 분홍색 행**                                                                 | 갑작스러운 고장에 대한 잠재적인 가능성을 나타내는 수치 |

범례

<table>
<thead>
<tr class="header">
<th><p>ID</p></th>
<th><p>16진</p></th>
<th><p>특성 이름</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01</p></td>
<td><p>0x01</p></td>
<td><p>읽기 오류율 (Read Error Rate)</p></td>
</tr>
<tr class="even">
<td><p>02</p></td>
<td><p>0x02</p></td>
<td><p>처리량 성능</p></td>
</tr>
<tr class="odd">
<td><p>03</p></td>
<td><p>0x03</p></td>
<td><p>스핀 업 시간</p></td>
</tr>
<tr class="even">
<td><p>04</p></td>
<td><p>0x04</p></td>
<td><p>시작/정지 횟수</p></td>
</tr>
<tr class="odd">
<td><p>05</p></td>
<td><p>0x05</p></td>
<td><p>재할당된 섹터 수 (Reallocated Sectors Count)</p></td>
</tr>
<tr class="even">
<td><p>06</p></td>
<td><p>0x06</p></td>
<td><p>읽기 경로 마진</p></td>
</tr>
<tr class="odd">
<td><p>07</p></td>
<td><p>0x07</p></td>
<td><p>탐색 오류율</p></td>
</tr>
<tr class="even">
<td><p>08</p></td>
<td><p>0x08</p></td>
<td><p>탐색 시간 성능</p></td>
</tr>
<tr class="odd">
<td><p>09</p></td>
<td><p>0x09</p></td>
<td><p>사용 시간 (POH)</p></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>0x0A</p></td>
<td><p>스핀 재시도 횟수</p></td>
</tr>
<tr class="odd">
<td><p>11</p></td>
<td><p>0x0B</p></td>
<td><p>재측정 재시도 / 측정 재시도 수</p></td>
</tr>
<tr class="even">
<td><p>12</p></td>
<td><p>0x0C</p></td>
<td><p>사용 횟수 (Power Cycle Count)</p></td>
</tr>
<tr class="odd">
<td><p>13</p></td>
<td><p>0x0D</p></td>
<td><p>소프트 읽기 오류 속도</p></td>
</tr>
<tr class="even">
<td><p>180</p></td>
<td><p>0xB4</p></td>
<td><p>총 비사용 예약 블록 수</p></td>
</tr>
<tr class="odd">
<td><p>181</p></td>
<td><p>0xB5</p></td>
<td><p>총 프로그램 실패 수 / 비-4K 정렬 액세스 수</p></td>
</tr>
<tr class="even">
<td><p>183</p></td>
<td><p>0xB7</p></td>
<td><p>SATA 다운시프트 오류 수 / 런타임 불량 블록</p></td>
</tr>
<tr class="odd">
<td><p>184</p></td>
<td><p>0xB8</p></td>
<td><p>앤드 투 앤드 오류 정정 횟수</p></td>
</tr>
<tr class="even">
<td><p>185</p></td>
<td><p>0xB9</p></td>
<td><p>헤드 안정성</p></td>
</tr>
<tr class="odd">
<td><p>186</p></td>
<td><p>0xBA</p></td>
<td><p>유도 Op-진동 감지</p></td>
</tr>
<tr class="even">
<td><p>187</p></td>
<td><p>0xBB</p></td>
<td><p>회복 불가능 오류 수</p></td>
</tr>
<tr class="odd">
<td><p>188</p></td>
<td><p>0xBC</p></td>
<td><p>명령 제한 시간 초과 (Command Timeout)</p></td>
</tr>
<tr class="even">
<td><p>189)</p></td>
<td><p>0xBD</p></td>
<td><p>높은 플라이 쓰기 횟수 (High Fly Writes)</p></td>
</tr>
<tr class="odd">
<td><p>190</p></td>
<td><p>0xBE</p></td>
<td><p>공기 온도 (Airflow Temperature (WDC) resp. Airflow Temperature Celsius (HP))</p></td>
</tr>
<tr class="even">
<td><p>190</p></td>
<td><p>0xBE</p></td>
<td><p>100부터 온도 차이</p></td>
</tr>
<tr class="odd">
<td><p>191</p></td>
<td><p>0xBF</p></td>
<td><p>충격에 의한 오류율 (G-sense Error Rate)</p></td>
</tr>
<tr class="even">
<td><p>192</p></td>
<td><p>0xC0</p></td>
<td><p>전원 차단에 의한 자기 헤드 대피 횟수 (Power-off Retract Count / Emergency Retract Cycle Count (후지쯔)[2])</p></td>
</tr>
<tr class="odd">
<td><p>193</p></td>
<td><p>0xC1</p></td>
<td><p>로드 사이클 수, 로드/언로드 사이클 수 (Load Cycle Count, Load/Unload Cycle Count (후지쯔))</p></td>
</tr>
<tr class="even">
<td><p>194</p></td>
<td><p>0xC2</p></td>
<td><p>장치 온도 (Temperature resp. Temperature Celsius)</p></td>
</tr>
<tr class="odd">
<td><p>195</p></td>
<td><p>0xC3</p></td>
<td><p>회복된 하드웨어 ECC</p></td>
</tr>
<tr class="even">
<td><p>196</p></td>
<td><p>0xC4</p></td>
<td><p>재할당 이벤트 수</p></td>
</tr>
<tr class="odd">
<td><p>197</p></td>
<td><p>0xC5</p></td>
<td><p>보류 중인 섹터 수</p></td>
</tr>
<tr class="even">
<td><p>198</p></td>
<td><p>0xC6</p></td>
<td><p>회복 불가능 섹터 수 (Uncorrectable Sector Count /</p>
<p>Offline Uncorrectable /</p>
<p>Off-Line Scan Uncorrectable Sector Count[3])</p></td>
</tr>
<tr class="odd">
<td><p>199</p></td>
<td><p>0xC7</p></td>
<td><p>울트라 DMA CRC 오류 수</p></td>
</tr>
<tr class="even">
<td><p>200</p></td>
<td><p>0xC8</p></td>
<td><p>멀티-존 오류율[4]</p></td>
</tr>
<tr class="odd">
<td><p>200</p></td>
<td><p>0xC8</p></td>
<td><p>읽기 오류율 (후지쯔)</p></td>
</tr>
<tr class="even">
<td><p>201</p></td>
<td><p>0xC9</p></td>
<td><p>소프트 읽기 오류율 /</p>
<p>TA Counter Detected</p></td>
</tr>
<tr class="odd">
<td><p>202</p></td>
<td><p>0xCA</p></td>
<td><p>데이터 주소 마크 오류 /</p>
<p>TA Counter Increased</p></td>
</tr>
<tr class="even">
<td><p>203</p></td>
<td><p>0xCB</p></td>
<td><p>런아웃 취소</p></td>
</tr>
<tr class="odd">
<td><p>204</p></td>
<td><p>0xCC</p></td>
<td><p>소프트 ECC 수정</p></td>
</tr>
<tr class="even">
<td><p>205</p></td>
<td><p>0xCD</p></td>
<td><p>서멀 애스퍼리티 레이트 (TAR)</p></td>
</tr>
<tr class="odd">
<td><p>206</p></td>
<td><p>0xCE</p></td>
<td><p>플라잉 높이</p></td>
</tr>
<tr class="even">
<td><p>207</p></td>
<td><p>0xCF</p></td>
<td><p>스핀 고전류</p></td>
</tr>
<tr class="odd">
<td><p>208</p></td>
<td><p>0xD0</p></td>
<td><p>스핀 버즈</p></td>
</tr>
<tr class="even">
<td><p>209</p></td>
<td><p>0xD1</p></td>
<td><p>오프라인 탐색 성능</p></td>
</tr>
<tr class="odd">
<td><p>210</p></td>
<td><p>0xD2</p></td>
<td><p>쓰기 도중 진동</p></td>
</tr>
<tr class="even">
<td><p>211</p></td>
<td><p>0xD3</p></td>
<td><p>쓰기 도중 진동</p></td>
</tr>
<tr class="odd">
<td><p>212</p></td>
<td><p>0xD4</p></td>
<td><p>쓰기 도중 충격</p></td>
</tr>
<tr class="even">
<td><p>220</p></td>
<td><p>0xDC</p></td>
<td><p>디스크 교대</p></td>
</tr>
<tr class="odd">
<td><p>221</p></td>
<td><p>0xDD</p></td>
<td><p>G-센스 오류 속도</p></td>
</tr>
<tr class="even">
<td><p>222</p></td>
<td><p>0xDE</p></td>
<td><p>로드된 시간</p></td>
</tr>
<tr class="odd">
<td><p>223</p></td>
<td><p>0xDF</p></td>
<td><p>로드/언로드 재시도 수</p></td>
</tr>
<tr class="even">
<td><p>224</p></td>
<td><p>0xE0</p></td>
<td><p>로드 마찰</p></td>
</tr>
<tr class="odd">
<td><p>225</p></td>
<td><p>0xE1</p></td>
<td><p>로드/언로드 주기 수</p></td>
</tr>
<tr class="even">
<td><p>226</p></td>
<td><p>0xE2</p></td>
<td><p>'In'-타임 로드</p></td>
</tr>
<tr class="odd">
<td><p>227</p></td>
<td><p>0xE3</p></td>
<td><p>토크 증폭 수</p></td>
</tr>
<tr class="even">
<td><p>228</p></td>
<td><p>0xE4</p></td>
<td><p>전원 차단에 의한 자기 헤드 대피 주기</p></td>
</tr>
<tr class="odd">
<td><p>230</p></td>
<td><p>0xE6</p></td>
<td><p>GMR 헤드 진폭</p></td>
</tr>
<tr class="even">
<td><p>230</p></td>
<td><p>0xE6</p></td>
<td><p>드라이브 수명 보호 상태</p></td>
</tr>
<tr class="odd">
<td><p>231</p></td>
<td><p>0xE7</p></td>
<td><p>온도</p></td>
</tr>
<tr class="even">
<td><p>231</p></td>
<td><p>0xE7</p></td>
<td><p>남은 SSD 수명</p></td>
</tr>
<tr class="odd">
<td><p>232</p></td>
<td><p>0xE8</p></td>
<td><p>여유 내구도</p></td>
</tr>
<tr class="even">
<td><p>232</p></td>
<td><p>0xE8</p></td>
<td><p>가용 예약 공간</p></td>
</tr>
<tr class="odd">
<td><p>233</p></td>
<td><p>0xE9</p></td>
<td><p>켜져있는 시간</p></td>
</tr>
<tr class="even">
<td><p>233</p></td>
<td><p>0xE9</p></td>
<td><p>미디어 소모 표시기</p></td>
</tr>
<tr class="odd">
<td><p>234</p></td>
<td><p>0xEA</p></td>
<td><p>평균 삭제 수 AND Maximum Erase Count</p></td>
</tr>
<tr class="even">
<td><p>235</p></td>
<td><p>0xEB</p></td>
<td><p>Good Block Count AND System(Free) Block Count</p></td>
</tr>
<tr class="odd">
<td><p>240</p></td>
<td><p>0xF0</p></td>
<td><p>헤드 플라잉 시간</p></td>
</tr>
<tr class="even">
<td><p>240</p></td>
<td><p>0xF0</p></td>
<td><p>전송 오류율, 헤드 비행시간 (Transfer Error Rate (후지쯔))</p></td>
</tr>
<tr class="odd">
<td><p>241</p></td>
<td><p>0xF1</p></td>
<td><p>호스트 총 기록량 (Total LBAs Written)</p></td>
</tr>
<tr class="even">
<td><p>242</p></td>
<td><p>0xF2</p></td>
<td><p>호스트 총 읽기량 (Total LBAs Read)</p></td>
</tr>
<tr class="odd">
<td><p>250</p></td>
<td><p>0xFA</p></td>
<td><p>읽기 오류 재시도율</p></td>
</tr>
<tr class="even">
<td><p>254</p></td>
<td><p>0xFE</p></td>
<td><p>낙하 보호</p></td>
</tr>
</tbody>
</table>

## 각주

## 외부 링크

  - [Out SMART Your Hard Drive](http://prefetch.net/articles/diskdrives.smart.html) Using the *smartmontools* program to monitor S.M.A.R.T. values

[분류:컴퓨터 저장 매체](https://ko.wikipedia.org/wiki/분류:컴퓨터_저장_매체 "wikilink")

1.  .
2.
3.
4.