> This article is converted from Wikipedia: [:Cpulist](https://ko.wikipedia.org/wiki/:Cpulist).


<includeonly> {{\#ifeq:|head|{{(\!}} class="wikitable"}} =\!

|section=

|model={{\#switch:

`| head = 모델`
`번호`
`| {{#if: ``|[`<http://ark.intel.com/products/>` ``]|`` }}`

}}

|sspec={{\#switch:

`| head = s스펙`
`번호`
`| {{#if:``|`` }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|* ``{{#if:``| (``)}} }} {{#if:``|``}} }} }}`

}}

|freq={{\#switch:

`| head = 주파수`
`| {{#if: ``{{#switch: ``|clarkdale|arrandale|lynnfield|clarksfield|bloomfield|gainestown=533|pineview=667|lincroft|tunnelcreek|sandybridge|sandybridge_e|skylake_e|kabylake_x|ivybridge|haswell|skylake=400|baytrail=333|}}|`
`    {{#if: ``|`
`      {{#expr: ({{#switch: ``|pineview=667|baytrail=333|lincroft|tunnelcreek|sandybridge|sandybridge_e|skylake_e|kabylake_x|ivybridge|haswell|skylake=400|533}} }}}`
`          | 50 = 50`
`          | 60 = 60`
`          | 66 | 67 = 200 / 3`
`          | 100 = 100`
`          | 133 = 400 / 3`
`          | 333 = 83.2`
`          | 400 = 100`
`          | 533 = 400 / 3`
`          | 666 | 667 = 500 / 3`
`          | 800 = 200`
`          | 1067 | 1066 = 800 / 3`
`          | 1333 = 1000 / 3`
`          | 1600 = 400`
`          }} * `
`         {{#ifexpr: (``|pineview=667|baytrail=332.8|lincroft|tunnelcreek|sandybridge|sandybridge_e|skylake_e|kabylake_x|ivybridge|haswell|skylake=400|533}} }}} / 4 * ``) < 990|) round 0|/ 1000) round 2}}`
`      }} {{#ifexpr: (``|pineview=667|baytrail=332.8|lincroft|tunnelcreek|sandybridge|sandybridge_e|skylake_e|kabylake_x|ivybridge|haswell|skylake=400|533}} }}} / 4 * ``) < 990| {{#if: ``|MHz|MHz}}| {{#if: ``|GHz|GHz}} }}`
`    |{{#if: ``|{{#ifexpr: `` < 10|`` {{#if: ``|GHz|GHz}}|`` {{#if: ``|MHz|MHz}} }} }}`
`    }}`
`  |{{#if: ``|{{#ifexpr: `` < 10|`` {{#if: ``|GHz|GHz}}|`` {{#if: ``|MHz|MHz}} }} }}`

`  }}`

}}

|cores =

`| head = 코어`
`| gulftown`
`| gulftownup = 6`
`| clarkdale`
`| arrandale = 2`
`| beckton = 8`
`| bloomfield`
`| gainestown`
`| lynnfield`
`| clarksfield`
`| jasperforest`
`| baytrail = 4`
`| silverthorne`
`| diamondville`
`| pineview`
`| lincroft`
`| tunnelcreek = 1`
`| dunnington = 6`
`| harpertown`
`| yorkfield = 4`
`| wolfdale`
`| penryn`
`| penrynulv = 2`
`| tigerton`
`| clovertown`
`| kentsfield = 4`
`| woodcrest`
`| conroe`
`| merom`
`| sossaman`
`| yonah = 2`
`| dothan`
`| banias`
`| tualatin`
`| copperminet | coppermine | cascades`
`| tanner | drake | katmai`
`| dixon | mendocino | covington | tonga | deschutes`
`| klamath | p6`
`| tillamook | p55ctp | p55lm | p55c`
`| p54ct | p5t | p24ct | p24t | p54lm | p54cqs | p54cm | p54cs | p54c`
`| p5 = 1`

}} }}}

|threads = {{\#switch:

`| head = 코어`
`(스레드)`
`| ``  (``)`

}}

|turbo={{\#switch:

`| head = `[`터보`](https://ko.wikipedia.org/wiki/인텔_터보_부스트 "wikilink")
`| ``}}`

}}

|turboboost={{\#switch:

`| head = `[`터보``   ``부스트`](https://ko.wikipedia.org/wiki/인텔_터보_부스트 "wikilink")
`모든 코어/최대`
`| ``/`

}}

|burst={{\#switch:

`| head = Burst`
`| {{#if: ``|`` GHz|``}}`

}}

|uncore={{\#switch:

`| head = `[`언코어`
`속도`](https://ko.wikipedia.org/wiki/언코어 "wikilink")
`| {{#if: ``{{#switch: ``|clarkdale|arrandale|lynnfield|clarksfield|bloomfield|gainestown=533|pineview=667|lincroft=100|tunnelcreek=100|}}|`
`  {{#if: ``|`
`      {{#expr: ({{#switch: ``|pineview=667|lincroft=100|tunnelcreek=100|533}} }}}`
`          | 50 = 50`
`          | 60 = 60`
`          | 66 | 67 = 200 / 3`
`          | 100 = 100`
`          | 133 = 400 / 3`
`          | 400 = 100`
`          | 533 = 400 / 3`
`          | 666 | 667 = 500 / 3`
`          | 800 = 200`
`          | 1067 | 1066 = 800 / 3`
`          | 1333 = 1000 / 3`
`          | 1600 = 400`
`          }} * `
`         {{#ifexpr: (`` / 4 * ``) < 9900|) round 0|/ 1000) round 2}}`
`      }} {{#ifexpr: (`` / 4 * ``) < 9900| {{#if: ``|MHz|MHz}}| {{#if: ``|GHz|GHz}} }}`
`    |{{#if: ``|{{#ifexpr: `` < 10|`` {{#if: ``|GHz|GHz}}|`` {{#if: ``|MHz|MHz}} }} }}`
`    }}`
`  |{{#if: ``|{{#ifexpr: `` < 10|`` {{#if: ``|GHz|GHz}}|`` {{#if: ``|MHz|MHz}} }} }}`

`  }}`

}}

|l1={{\#switch:

`| head = `[`L1`
`캐시`](https://ko.wikipedia.org/wiki/CPU_캐시 "wikilink")
`| tillamook | p55ctp | p55lm | p55c = {{#switch: `
`   | 16 | 32 = {{#expr: ``/2}} + {{#expr: ``/2}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`   | `` {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}{{#if: ``| (?)}}`
` }}`
`| p54ct | p5t | p24ct | p24t | p54lm | p54cqs | p54cm | p54cs | p54c = {{#switch: `
`   | 16 | 32 = {{#expr: ``/2}} + {{#expr: ``/2}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`   | `` {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}{{#if: ``| (?)}}`
` }}`
`| p5 = {{#switch: `
`   | 16 | 32 = {{#expr: ``/2}} + {{#expr: ``/2}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`   | `` {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}{{#if: ``| (?)}}`
` }}`
`| `

}}

|l2={{\#switch:

`| head = `[`L2`
`캐시`](https://ko.wikipedia.org/wiki/CPU_캐시 "wikilink")
`| silverthorne`
`| diamondville`
`| pineview`
`| lincroft`
`| tunnelcreek = `` {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`| wolfdale`
`| penrynulv`
`| penryn`
`| woodcrest`
`| conroe`
`| merom`
`| sossaman`
`| yonah`
`| dothan`
`| banias`
`| tualatin`
`| copperminet | coppermine | cascades`
`| tanner | drake | katmai`
`| dixon | mendocino | covington | tonga | deschutes`
`| klamath | p6 = {{#switch: `
`  | 0 = `
`  | 128 = 128 {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`  | 256 = 256 {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`  | 512 = 512 {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`  | 1   | 2   | 3   | 4   | 6   =`
`       `` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`  | {{#if: ``|`` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")` (?)]|MiB (?)}} }}`
` }}`
`| tigerton`
`| clovertown`
`| harpertown`
`| dunnington`
`| yorkfield`
`| kentsfield = {{#switch: `
`  | 2   | 3   | 4   | 6   | 8   | 12 =`
`       2 × {{#expr: ``/2}} {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`  | {{#if: ``|`` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")` (?)]|MiB (?)}} }}`
` }}`
`| skylake_e = `` × 1}}} {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`| lynnfield`
`| clarksfield`
`| jasperforest`
`| bloomfield`
`| sandybridge`
`| sandybridge_e`
`| kabylake_x`
`| ivybridge`
`| haswell`
`| skylake`
`| gainestown = `` × 256}}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`| clarkdale`
`| arrandale = `` × 256}}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`| gulftown`
`| gulftownup = `` × 256}}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`| beckton = `` × 256}}} {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`| baytrail = {{#switch: `
`  | 512 = 512 {{#if: ``|`[`KiB`](https://ko.wikipedia.org/wiki/키비바이트 "wikilink")`|KiB}}`
`  |`` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
` }}`
`| `

}}

|l3={{\#switch:

`| head = `[`L3`
`캐시`](https://ko.wikipedia.org/wiki/CPU_캐시 "wikilink")
`| lynnfield`
`| clarksfield`
`| bloomfield`
`| gainestown`
`| jasperforest`
`| sandybridge|sandybridge_e|ivybridge|haswell|skylake|skylake_e|kabylake_x = `` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`| clarkdale`
`| arrandale = `` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`| gulftown`
`| dunnington`
`| gulftownup = `` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`| beckton = `` {{#if: ``|`[`MiB`](https://ko.wikipedia.org/wiki/메비바이트 "wikilink")`|MiB}}`
`| `

}}

|iobus={{\#switch:

`| head = I/O 버스`
`| beckton = {{#if:``|4 × `` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|4 × 6.4 GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}}}`
`| gulftown`
`| gainestown = {{#if:``|2 × `` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|2 × 6.4 GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}}}`
`| gulftownup`
`| bloomfield = {{#if:``|1 × `` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|1 × 6.4 GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}}}`
`| clarkdale`
`| arrandale`
`| lynnfield`
`| clarksfield`
`| pineview`
`| lincroft = {{#if: ``|`[`DMI`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI}}`
`| sandybridge`
`| ivybridge`
`| haswell = {{#if: ``|`[`DMI``   ``2.0`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI 2.0}}`
`| skylake = {{#if: ``|`[`DMI``   ``3.0`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI 3.0}}`
`| skylake_e = {{#if:``|`` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|UPI}}|{{#if: ``|`[`DMI``   ``3.0`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI 3.0}}}}`
`| kabylake_x = {{#if: ``|`[`DMI``   ``3.0`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI 3.0}}`
`| sandybridge_e = {{#if:``|`` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|`
`                                  {{#if: ``|`[`DMI``   ``2.0`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI 2.0}}}}`
`| tunnelcreek = {{#if: ``|`[`PCIe`](https://ko.wikipedia.org/wiki/PCI_익스프레스 "wikilink")`|PCIe}}`
`| jasperforest = {{#if:``|1 × `` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|`
`                                  {{#if: ``|`[`DMI`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI}}}}`
`| {{#if:``|``|`
`   {{#if:``|`` GT/s {{#if: ``|`[`QPI`](https://ko.wikipedia.org/wiki/퀵패스_인터커넥트 "wikilink")`|QPI}}|`
`    {{#if:``|`` MT/s {{#if: ``|`[`FSB`](https://ko.wikipedia.org/wiki/프론트_사이드_버스 "wikilink")`|FSB}}|`
`     {{#if:``|{{#if: ``|`[`DMI`](https://ko.wikipedia.org/wiki/다이렉트_미디어_인터페이스 "wikilink")`|DMI}}|`
`      {{#if:``|`` GT/s {{#if: ``|`[`HT`](https://ko.wikipedia.org/wiki/하이퍼트랜스포트 "wikilink")`}} }}`
`     }}`
`    }}`
`   }}`
`  }}`

}}

|fsb={{\#switch:

`| head = `[`FSB`](https://ko.wikipedia.org/wiki/프론트_사이드_버스 "wikilink")
`| diamondville = `` {{#if: ``|MT/s|MT/s}}`
`| dunnington`
`| harpertown`
`| yorkfield`
`| wolfdale`
`| penrynulv`
`| penryn`
`| tigerton`
`| clovertown`
`| kentsfield`
`| woodcrest`
`| conroe`
`| merom`
`| sossaman`
`| yonah`
`| dothan`
`| banias`
`| tualatin`
`| copperminet | coppermine | cascades`
`| tanner | drake | katmai`
`| dixon | mendocino | covington | tonga | deschutes`
`| klamath | p6 = {{#if: ``|`` {{#if: ``|MT/s|MT/s}}}}`
`| {{#if: ``|`` {{#if: ``|MT/s|MT/s}}}}`

}}

|mult={{\#switch:

`| head = `[`배수`](https://ko.wikipedia.org/wiki/CPU_배수 "wikilink")
`| {{#if:``|``×}}`

}}

|gfxclock={{\#switch:

`| head = GPU`
`주파수`
`| {{#if:``|`` {{#if: ``|MHz|MHz}}|``}}`

}}

|mem={{\#switch:

`| head = `[`메모리`](https://ko.wikipedia.org/wiki/메모리_컨트롤러 "wikilink")
`| gainestown`
`| bloomfield  = `` }}}`
`| gulftown`
`| gulftownup`
`| sandybridge_e`
`| skylake_e`
`| kabylake_x`
`| jasperforest= `` }}}`
`| beckton     = `` }}}`
`| lynnfield`
`| clarksfield = `` }}}`
`| arrandale`
`| clarkdale   = `` }}}`
`| `

}}

|connectivity = {{\#switch:

`| head = 연결`
`| {{#if: ``|``|``}}`

}}

|volt = {{\#switch:

`| head = `[`전압`](https://ko.wikipedia.org/wiki/CPU_코어_전압 "wikilink")
`| {{#if:``|``|`
`   {{#if:``|``{{#if:``|-``}} V}}`
`  }}`

}}

|sdp = {{\#switch:

`| head = `[`SDP`](https://ko.wikipedia.org/wiki/열_설계_전력 "wikilink")
`| {{#if: ``|`` W|``}}`

}}

|tdp = {{\#if:| {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:|\*  W }} {{\#if:| W}} }} |{{\#switch:

`| head = `[`TDP`](https://ko.wikipedia.org/wiki/열_설계_전력 "wikilink")
`| lynnfield   = `` W`
`| bloomfield  = `` W`
`| clarkdale   = `` W`
`| clarksfield = `` W`
`| arrandale   = `` W`
`| clovertown`
`| harpertown`
`| tigerton    = `` W`
`| dunnington  = `` W`
`| merom`
`| penryn      = `` W`
`| penrynulv   = `` W`
`| woodcrest`
`| wolfdale`
`| conroe      = `` W`
`| yorkfield`
`| kentsfield  = `` W`
`| sossaman    = `` W`
`| yonah       = `` W`
`| dothan      = `` W`
`| banias      = `` W`
`| baytrail    = `
`| {{#if: ``|`` W}}`

}} }}

|sock = {{\#if:| {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|\*  }} {{\#if:|}} }} |{{\#switch:

`| head = `[`소켓`](https://ko.wikipedia.org/wiki/CPU_소켓 "wikilink")
`| haswell =  {{#switch: `
`                  |bga | BGA | FC-BGA10`
`                  | 1364 = {{#if: ``|`[`BGA-1364`](https://ko.wikipedia.org/wiki/BGA-1364 "wikilink")`|BGA-1364}}`
`                  | 1168 = {{#if: ``|`[`BGA-1168`](https://ko.wikipedia.org/wiki/BGA-1168 "wikilink")`|BGA-1168}}`
`                  | 1234 = {{#if: ``|`[`BGA-1234`](https://ko.wikipedia.org/wiki/BGA-1234 "wikilink")`|BGA-1234}}`
`                  |pga |PGA |PGA946 |PGA946B`
`                  | 946 |946B = {{#if: ``|`[`소켓``   ``G3`](https://ko.wikipedia.org/wiki/인텔_소켓_G3 "wikilink")`|소켓 G3}}`
`                  | ``|`[`소켓``   ``G3`](https://ko.wikipedia.org/wiki/인텔_소켓_G3 "wikilink")`|소켓 G3}}}}}`
`                  | 1150 = {{#if: ``|`[`LGA``   ``1150`](../Page/LGA_1150.md "wikilink")`|LGA 1150}}`
`                 }}`
`| skylake =  {{#switch: `
`                  |bga | BGA | FC-BGA10`
`                  | 1515 = {{#if: ``|`[`BGA``   ``1515`](https://ko.wikipedia.org/wiki/BGA_1515 "wikilink")`|BGA 1515}}`
`                  | 1440 = {{#if: ``|`[`BGA``   ``1440`](https://ko.wikipedia.org/wiki/BGA_1440 "wikilink")`|BGA 1440}}`
`                  | 1356 |1356B = {{#if: ``|`[`BGA``   ``1356`](https://ko.wikipedia.org/wiki/BGA_1356 "wikilink")`|BGA 1356}}`
`                  | 1151 = {{#if: ``|`[`LGA``   ``1151`](../Page/LGA_1151.md "wikilink")`|LGA 1151}}`
`              | 2066 = {{#if: ``|`[`LGA``   ``2066`](https://ko.wikipedia.org/wiki/LGA_2066 "wikilink")`|LGA 2066}}`
`              | 3647 = {{#if: ``|`[`LGA``   ``3647`](https://ko.wikipedia.org/wiki/LGA_3647 "wikilink")`|LGA 3647}}`
`                 }}`
`| gainestown`
`| gulftown`
`| gulftownup`
`| bloomfield`
`| jasperforest = {{#if: ``|`[`LGA``   ``1366`](https://ko.wikipedia.org/wiki/LGA_1366 "wikilink")`|LGA 1366}}`
`| beckton    = {{#if: ``|`[`LGA``   ``1567`](https://ko.wikipedia.org/wiki/LGA_1567 "wikilink")`|LGA 1567}}`
`| lynnfield`
`| clarkdale  = {{#if: ``|`[`LGA``   ``1156`](https://ko.wikipedia.org/wiki/LGA_1156 "wikilink")`|LGA 1156}}`
`| arrandale`
`| clarksfield =  {{#switch: `
`                  |bga | BGA | FC-BGA10`
`                  | 1288 = {{#if: ``|`[`BGA-1288`](https://ko.wikipedia.org/wiki/BGA-1288 "wikilink")`|BGA-1288}}`
`                  |pga |PGA |PGA988 |PGA988A`
`                  | 988 |988A = {{#if: ``|`[`소켓``   ``G1`](https://ko.wikipedia.org/wiki/소켓_G1 "wikilink")`|소켓 G1}}`
`                  | ``|`[`소켓``   ``G1`](https://ko.wikipedia.org/wiki/소켓_G1 "wikilink")`|소켓 G1}}}}}`
`                 }}`
`| dothan`
`| banias = ``|`[`소켓``   ``479`](https://ko.wikipedia.org/wiki/소켓_479 "wikilink")`|소켓 479}} }}}`
`| sossaman`
`| yonah`
`| merom = ``|`[`소켓``   ``M`](https://ko.wikipedia.org/wiki/소켓_M "wikilink")`|소켓 M}} }}}`
`| penryn = ``|`[`소켓``   ``P`](https://ko.wikipedia.org/wiki/소켓_P "wikilink")`|소켓 P}} }}}`
`| penrynulv = ``|`[`μFC-BGA``   ``956`](https://ko.wikipedia.org/wiki/μFC-BGA_956 "wikilink")`|μFC-BGA 956}} }}}`
`| silverthorne`
`| diamondville = {{#ifeq: ``|441|`
`       {{#if: ``|`[`BGA``   ``441`](https://ko.wikipedia.org/wiki/BGA_441 "wikilink")`|BGA 441}}|`
`       {{#if: ``|`[`BGA``   ``437`](https://ko.wikipedia.org/wiki/BGA_437 "wikilink")`|BGA 437}} }}`
`| pineview`
`| lincroft = {{#if: ``|`[`FC-BGA``   ``518`](https://ko.wikipedia.org/wiki/FC-BGA_518 "wikilink")`|FC-BGA 518}}`
`| tunnelcreek = {{#if: ``|`[`FC-BGA``   ``676`](https://ko.wikipedia.org/wiki/FC-BGA_676 "wikilink")`|FC-BGA 676}}`
`| tigerton`
`| dunnington = {{#if: ``|`[`소켓``   ``604`](https://ko.wikipedia.org/wiki/소켓_604 "wikilink")`|소켓 604}}`
`| woodcrest`
`| clovertown`
`| harpertown = ``|`[`LGA``   ``771`](https://ko.wikipedia.org/wiki/LGA_771 "wikilink")`|LGA 771}} }}}`
`| wolfdale`
`|  conroe`
`|  yorkfield`
`|  kentsfield  =  ``|`[`LGA``   ``775`](https://ko.wikipedia.org/wiki/LGA_775 "wikilink")`|LGA 775}} }}}`
`| {{#switch: `
`    | 2066 = {{#if: ``|`[`LGA``   ``2066`](https://ko.wikipedia.org/wiki/LGA_2066 "wikilink")`|LGA 2066}}`
`    | 3647 = {{#if: ``|`[`LGA``   ``3647`](https://ko.wikipedia.org/wiki/LGA_3647 "wikilink")`|LGA 3647}}`
`  | 2011-3 = {{#if: ``|`[`LGA``   ``2011`](https://ko.wikipedia.org/wiki/LGA_2011 "wikilink")`|LGA 2011-3}}`
`  | 2011-1 = {{#if: ``|`[`LGA``   ``2011`](https://ko.wikipedia.org/wiki/LGA_2011 "wikilink")`|LGA 2011-1}}`
`  | 2011 = {{#if: ``|`[`LGA``   ``2011`](https://ko.wikipedia.org/wiki/LGA_2011 "wikilink")`|LGA 2011}}`
`  | 1366 = {{#if: ``|`[`LGA``   ``1366`](https://ko.wikipedia.org/wiki/LGA_1366 "wikilink")`|LGA 1366}}`
`  | 1364 = {{#if: ``|`[`BGA``   ``1364`](https://ko.wikipedia.org/wiki/BGA_1364 "wikilink")`|BGA 1364}}`
`  | 1356-3 = {{#if: ``|`[`LGA``   ``1356-3`](https://ko.wikipedia.org/wiki/LGA_1356-3 "wikilink")`|LGA 1356-3}}`
`  | 1356 = {{#if: ``|`[`LGA``   ``1356`](https://ko.wikipedia.org/wiki/LGA_1356 "wikilink")`|LGA 1356}}`
`  | 1288 = {{#if: ``|`[`BGA``   ``1288`](https://ko.wikipedia.org/wiki/BGA_1288 "wikilink")`|LGA 1288}}`
`  | 1284 = {{#if: ``|`[`BGA``   ``1284`](https://ko.wikipedia.org/wiki/BGA_1284 "wikilink")`|BGA 1284}}`
`  | 1234 = {{#if: ``|`[`BGA``   ``1234`](https://ko.wikipedia.org/wiki/BGA_1234 "wikilink")`|BGA 1234}}`
`  | 1168 = {{#if: ``|`[`BGA``   ``1168`](https://ko.wikipedia.org/wiki/BGA_1168 "wikilink")`|BGA 1168}}`
`  | 1152`
`  | 1156 = {{#if: ``|`[`LGA``   ``1156`](https://ko.wikipedia.org/wiki/LGA_1156 "wikilink")`|LGA 1156}}`
`  | 1155 = {{#if: ``|`[`LGA``   ``1155`](https://ko.wikipedia.org/wiki/LGA_1155 "wikilink")`|LGA 1155}}`
`  | 1150 = {{#if: ``|`[`LGA``   ``1150`](../Page/LGA_1150.md "wikilink")`|LGA 1150}}`
`  | 1151 = {{#if: ``|`[`LGA``   ``1151`](../Page/LGA_1151.md "wikilink")`|LGA 1151}}`
`  | 1023 = {{#if: ``|`[`BGA``   ``1023`](https://ko.wikipedia.org/wiki/BGA_1023 "wikilink")`|BGA 1023}}`
`  | 988A = {{#if: ``|`[`소켓``   ``G1`](https://ko.wikipedia.org/wiki/소켓_G1 "wikilink")`|소켓 G1}}`
`  | 988B = {{#if: ``|`[`소켓``   ``G2`](https://ko.wikipedia.org/wiki/소켓_G2 "wikilink")`|소켓 G2}}`
`  | 956 = {{#if: ``|`[`μFC-BGA``   ``956`](https://ko.wikipedia.org/wiki/μFC-BGA_956 "wikilink")`|μFC-BGA 956}}`
`  | 946B = {{#if: ``|`[`소켓``   ``G3`](https://ko.wikipedia.org/wiki/소켓_G3 "wikilink")`|소켓 G3}}`
`  | Socket J`
`  | J`
`  | 775 = {{#if: ``|`[`LGA``   ``775`](https://ko.wikipedia.org/wiki/LGA_775 "wikilink")`|LGA 775}}`
`  | 771 = {{#if: ``|`[`LGA``   ``771`](https://ko.wikipedia.org/wiki/LGA_771 "wikilink")`|LGA 771}}`
`  | 604 = {{#if: ``|`[`소켓``   ``604`](https://ko.wikipedia.org/wiki/소켓_604 "wikilink")`|소켓 604}}`
`  | 603 = {{#if: ``|`[`소켓``   ``603`](https://ko.wikipedia.org/wiki/소켓_603 "wikilink")`|소켓 603}}`
`  | 559 = {{#if: ``|`[`micro-FCBGA8``   ``559`](https://ko.wikipedia.org/wiki/micro-FCBGA8_559 "wikilink")`|micro-FCBGA8 559}}`
`  | 462 = {{#if: ``|`[`소켓``   ``462`](https://ko.wikipedia.org/wiki/소켓_462 "wikilink")`|소켓 462}}`
`  | N`
`  | 478 = {{#if: ``|`[`소켓``   ``478`](https://ko.wikipedia.org/wiki/소켓_478 "wikilink")`|소켓 478}}`
`  | 479 = {{#if: ``|`[`소켓``   ``479`](https://ko.wikipedia.org/wiki/소켓_479 "wikilink")`|소켓 479}}`
`  | 441 = {{#if: ``|`[`BGA``   ``441`](https://ko.wikipedia.org/wiki/BGA_441 "wikilink")`|BGA 441}}`
`  | 437 = {{#if: ``|`[`BGA``   ``437`](https://ko.wikipedia.org/wiki/BGA_437 "wikilink")`|BGA 437}}`
`  | 423 = {{#if: ``|`[`소켓``   ``423`](https://ko.wikipedia.org/wiki/소켓_423 "wikilink")`|소켓 423}}`
`  | 370 = {{#if: ``|`[`소켓``   ``370`](https://ko.wikipedia.org/wiki/소켓_370 "wikilink")`|소켓 370}}`
`  | 4 = {{#if: ``|`[`소켓``   ``4`](https://ko.wikipedia.org/wiki/소켓_4 "wikilink")`|소켓 4}}`
`  | 5 = {{#if: ``|`[`소켓``   ``5`](https://ko.wikipedia.org/wiki/소켓_5 "wikilink")`|소켓 5}}`
`  | 6 = {{#if: ``|`[`소켓``   ``6`](https://ko.wikipedia.org/wiki/소켓_6 "wikilink")`|소켓 6}}`
`  | 7 = {{#if: ``|`[`소켓``   ``7`](https://ko.wikipedia.org/wiki/소켓_7 "wikilink")`|소켓 7}}`
`  | M = {{#if: ``|`[`소켓``   ``M`](https://ko.wikipedia.org/wiki/소켓_M "wikilink")`|소켓 M}}`
`  | P = {{#if: ``|`[`소켓``   ``P`](https://ko.wikipedia.org/wiki/소켓_P "wikilink")`|소켓 P}}`
`  | A = {{#if: ``|`[`슬롯``   ``A`](https://ko.wikipedia.org/wiki/슬롯_A "wikilink")`|슬롯 A}}`
`  | B = {{#if: ``|`[`슬롯``   ``B`](https://ko.wikipedia.org/wiki/슬롯_B "wikilink")`|슬롯 B}}`
`  | 2 = {{#if: ``|`[`슬롯``   ``2`](https://ko.wikipedia.org/wiki/슬롯_2 "wikilink")`|슬롯 2}}`
`  | `
`}}`

}} }}

|gfxmodel = {{\#switch:

`| head = GPU`
`모델`
`| sandybridge|ivybridge|haswell|baytrail|skylake = {{#switch: `
`  |4eu = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")` (4 EUs)|HD 그래픽스 (4 EUs)}}`
`  |6eu = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")` (6 EUs)|HD 그래픽스 (6 EUs)}}`
`  |10eu = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")` (10 EUs)|HD 그래픽스 (10 EUs)}}`
`  |12eu = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")` (12 EUs)|HD 그래픽스 (12 EUs)}}`
`  |16eu = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")` (16 EUs)|HD 그래픽스 (16 EUs)}}`
`  |gt1`
`  |GT1`
`  |1`
`  |2000 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 2000}}`
`  |gt2`
`  |GT2`
`  |2`
`  |3000 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 3000}}`
`  |p3000`
`  |P3000`
`  |P = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 P3000}}`
`  |2500 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 2500}}`
`  |4000 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 4000}}`
`  |P4000 = {{#if: ``|`[`HD``   ``그래픽스``   ``P4000`](https://ko.wikipedia.org/wiki/HD_그래픽스_P4000 "wikilink")`|HD 그래픽스 P4000}}`
`  |4200 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 4200}}`
`  |4400 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 4400}}`
`  |4600 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 4600}}`
`  |P4600 = {{#if: ``|`[`HD``   ``그래픽스``   ``P4600`](https://ko.wikipedia.org/wiki/HD_그래픽스_P4600 "wikilink")`|HD 그래픽스 P4600}}`
`  |P4700 = {{#if: ``|`[`HD``   ``그래픽스``   ``P4700`](https://ko.wikipedia.org/wiki/HD_그래픽스_P4700 "wikilink")`|HD 그래픽스 P4700}}`
`  |5000 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 5000}}`
`  |5100 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 그래픽스 5100}}`
`  |5200 = {{#if: ``|`[`아이리스``   ``프로``   ``그래픽스``   ``5200`](https://ko.wikipedia.org/wiki/아이리스_프로_그래픽스_5200 "wikilink")`|아이리스 프로 그래픽스 5200}}`
`  |5300 = {{#if: ``|`[`HD``   ``그래픽스``   ``5300`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 5300}}`
`  |5500 = {{#if: ``|`[`HD``   ``그래픽스``   ``5500`](https://ko.wikipedia.org/wiki/HD_그래픽스_5500 "wikilink")`|HD 그래픽스 5500}}`
`  |5600 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 5600}}`
`  |P5700 = {{#if: ``|`[`HD``   ``그래픽스``   ``P5700`](https://ko.wikipedia.org/wiki/HD_그래픽스_P5700 "wikilink")`|HD 그래픽스 P5700}}`
`  |6000 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 6000}}`
`  |6100 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 그래픽스 6100}}`
`  |6200 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 프로 그래픽스 6200}}`
`  |P6300 = {{#if: ``|`[`인텔``   ``HD``   ``및``   ``아이리스``   ``그래픽스`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 프로 그래픽스 P6300}}`
`  |400 = {{#if: ``|`[`HD``   ``그래픽스``   ``400`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 400}}`
`  |405 = {{#if: ``|`[`HD``   ``그래픽스``   ``405`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 405}}`
`  |500 = {{#if: ``|`[`HD``   ``그래픽스``   ``500`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 500}}`
`  |505 = {{#if: ``|`[`HD``   ``그래픽스``   ``505`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 505}}`
`  |510 = {{#if: ``|`[`HD``   ``그래픽스``   ``510`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 510}}`
`  |515 = {{#if: ``|`[`HD``   ``그래픽스``   ``515`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 515}}`
`  |520 = {{#if: ``|`[`HD``   ``그래픽스``   ``520`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 520}}`
`  |530 = {{#if: ``|`[`HD``   ``그래픽스``   ``530`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 530}}`
`  |P530 = {{#if: ``|`[`HD``   ``그래픽스``   ``P530`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 P530}}`
`  |535 = {{#if: ``|`[`HD``   ``그래픽스``   ``535`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 535}}`
`  |540 = {{#if: ``|`[`아이리스``   ``그래픽스``   ``540`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 그래픽스 540}}`
`  |550 = {{#if: ``|`[`아이리스``   ``그래픽스``   ``550`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 그래픽스 550}}`
`  |P555 = {{#if: ``|`[`아이리스``   ``프로``   ``그래픽스``   ``P555`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 프로 그래픽스 P555}}`
`  |580 = {{#if: ``|`[`아이리스``   ``프로``   ``그래픽스``   ``580`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 프로 그래픽스 580}}`
`  |P580 = {{#if: ``|`[`아이리스``   ``프로``   ``그래픽스``   ``P580`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 프로 그래픽스 P580}}`
`  |610 = {{#if: ``|`[`HD``   ``그래픽스``   ``610`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 610}}`
`  |615 = {{#if: ``|`[`HD``   ``그래픽스``   ``615`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 615}}`
`  |620 = {{#if: ``|`[`HD``   ``그래픽스``   ``620`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 620}}`
`  |630 = {{#if: ``|`[`HD``   ``그래픽스``   ``630`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 630}}`
`  |P630 = {{#if: ``|`[`HD``   ``그래픽스``   ``P630`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|HD 그래픽스 P630}}`
`  |640 = {{#if: ``|`[`아이리스``   ``플러스``   ``그래픽스``   ``640`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 플러스 그래픽스 640}}`
`  |650 = {{#if: ``|`[`아이리스``   ``플러스``   ``그래픽스``   ``650`](../Page/인텔_HD_및_아이리스_그래픽스.md "wikilink")`|아이리스 플러스 그래픽스 650}}`
`  | {{#if: ``|`` (?)|`` }}`
`}}`
`| `

}}

|date = {{\#switch:

`| head = 출시일`
`| `

}}

|part = {{\#switch:

`| head = 부품`
`번호`
`| {{#if:``|``  {{#if: ``|* `` }} {{#if:``|* `` }} {{#if:``|* `` }} {{#if:``|* `` }} {{#if:``|* `` }} {{#if:``|* `` }} {{#if:``|* `` }} {{#if:``|``}} }} }}`

}}

|price = {{\#switch:

`| head = 출시`
`가격 (`[`USD`](https://ko.wikipedia.org/wiki/미국_달러 "wikilink")`)`
`| `

}}

}}</includeonly><noinclude> [\*](https://ko.wikipedia.org/wiki/분류:마이크로프로세서_목록 "wikilink") </noinclude>