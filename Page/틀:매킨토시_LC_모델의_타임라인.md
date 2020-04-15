> This article is converted from Wikipedia: [틀:매킨토시 LC 모델의 타임라인](https://ko.wikipedia.org/wiki/틀:매킨토시_LC_모델의_타임라인).


<timeline> DateFormat=mm/dd/yyyy Period = from:07/01/1990 till:04/01/1997 Define $skip = at:end \# Force a blank line Define $dayunknown = 15 \# what day to use if it's actually not known ImageSize= width:600 height:auto barincrement:21 TimeAxis = orientation:horizontal PlotArea = right:5 left:20 bottom:75 top:5 Legend = orientation:vertical position:bottom columns:3

Colors =

`    id:bg         value:white`
`    id:020        value:rgb(1,0.96,0.7) legend:Motorola_68020`
`    id:0401       value:rgb(0.9,0.9,1) legend:Motorola_68030`
`    id:0401       value:rgb(0.9,0.9,1) legend:Motorola_68030`
`    id:0402       value:rgb(0.85,0.85,1)`
`    id:portable2  value:rgb(0.8,0.9,1)`
`    id:portable   value:rgb(0.75,0.85,1) legend:Motorola_68LC040`
`    id:powerpc    value:rgb(1,0.85,0.85) legend:PowerPC`
`    id:line       value:rgb(0.2,0.2,0.2)`
`    id:lightline  value:rgb(0.8,0.8,0.8)`
`    id:lighttext  value:rgb(0.5,0.5,0.5)`
`    id:current    value:rgb(0.9,0.9,0.9) legend:Other_Macs`

BackgroundColors = canvas:bg ScaleMajor = gridcolor:lighttext unit:year increment:1 start:01/01/1991 ScaleMinor = gridcolor:lightline unit:month increment:1 start:07/01/1990

BarData =

` Barset:pizza`
` Barset:aio`
` Barset:desktop`
` Barset:reference`

PlotData=

` width:15 textcolor:black`

` barset:pizza`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:020 from:10/15/1990 till:03/23/1992 text:"`[`LC`](https://ko.wikipedia.org/wiki/Macintosh_LC "wikilink")`"`
` barset:break`
`   color:0401 from:03/23/1992 till:03/15/1993 text:"`[`LC``   ``II`](https://ko.wikipedia.org/wiki/Macintosh_LC_II "wikilink")`"`
`   color:0401 from:10/18/1993 till:02/14/1994 text:"`[`LC``   ``III+`](https://ko.wikipedia.org/wiki/Macintosh_LC_III "wikilink")`"`
`   color:portable from:10/21/1993 till:07/15/1996 text:"`[`LC``   ``475`](https://ko.wikipedia.org/wiki/Macintosh_LC_475 "wikilink")`"`
` barset:break`
`   color:0402 from:02/10/1993 till:02/14/1994 text:"`[`LC``   ``III`](https://ko.wikipedia.org/wiki/Macintosh_LC_III "wikilink")`"`

` barset:aio`
`   color:0401 from:06/28/1993 till:02/02/1994 text:"`[`LC``   ``520`](https://ko.wikipedia.org/wiki/Macintosh_LC_520 "wikilink")`"`
`   $skip`
`   $skip`
` barset:break`
`   color:0402 from:02/02/1994 till:03/23/1995 text:"`[`LC``   ``550`](https://ko.wikipedia.org/wiki/Macintosh_LC_550 "wikilink")`"`
`   color:portable from:11/03/1994 till:03/02/1996 text:"`[`LC``   ``575`](https://ko.wikipedia.org/wiki/Macintosh_LC_575 "wikilink")`"`
`   $skip`
` barset:break`
`   $skip`
`   $skip`
`   color:portable2 from:04/03/1995 till:03/02/1996 text:"`[`LC``   ``580`](https://ko.wikipedia.org/wiki/Macintosh_LC_580 "wikilink")`"`
` barset:break`
`   color:powerpc from:04/03/1995 till:03/01/1997 text:"`[`5200``   ``LC``   ``/``   ``5300``   ``LC`](https://ko.wikipedia.org/wiki/Power_Macintosh_5200_LC "wikilink")`"`
`   $skip`
`   $skip`
` barset:desktop`
`   color:portable from:07/18/1994 till:03/02/1996 text:"`[`LC``   ``630`](https://ko.wikipedia.org/wiki/Macintosh_LC_630 "wikilink")`"`

` barset:reference`
`   color:current from:start till:08/01/1992 text:"`[`Macintosh``   ``II`](https://ko.wikipedia.org/wiki/Macintosh_II_series "wikilink")`"`
` barset:break`
`   color:current from:08/01/1992 till:04/01/1993 text:"|`[`Performa`](https://ko.wikipedia.org/wiki/Macintosh_Performa "wikilink")`"`
` barset:break`
`   color:current from:04/01/1993 till:10/01/1993 text:"|`[`Centris`](https://ko.wikipedia.org/wiki/Macintosh_Centris "wikilink")`"`
` barset:break`
`   color:current from:10/01/1993 till:05/01/1994 text:"|`[`Quadra`](https://ko.wikipedia.org/wiki/Macintosh_Quadra "wikilink")`"`
` barset:break`
`   color:current from:05/01/1994 till:03/01/1997 text:"|`[`Power``   ``Macintosh`](https://ko.wikipedia.org/wiki/Power_Macintosh "wikilink")`"`

</timeline>