> This article is converted from Wikipedia: [틀:애플 II 계열 연표](https://ko.wikipedia.org/wiki/틀:애플_II_계열_연표).


<timeline> DateFormat=mm/dd/yyyy Period = from:01/01/1976 till:03/15/1996 Define $skip = at:end \# Force a blank line Define $dayunknown = 15 \# what day to use if it's actually not known ImageSize= width:620 height:auto barincrement:21 TimeAxis = orientation:horizontal PlotArea = right:5 left:20 bottom:75 top:5 Legend = orientation:vertical position:bottom columns:4

Colors =

`    id:bg         value:white`
`    id:mba        value:rgb(0.85,0.85,0.85) `
`    id:mba2       value:rgb(0.9,0.9,0.9) `
`    id:ap1        value:rgb(1,1,0.55) legend:Apple_1`
`    id:0402       value:rgb(0.95,0.65,0.95) legend:Apple_//`
`    id:040        value:rgb(0.9,0.6,0.9) `
`    id:0502       value:rgb(0.65,0.85,1) legend:Apple_IIe`
`    id:050        value:rgb(0.6,0.8,1)`
`    id:apiii      value:rgb(1,0.55,0.65) legend:Apple_III`
`    id:apiii-b    value:rgb(1,0.5,0.6) `
`    id:portable2  value:rgb(0.6,0.9,0.5)`
`    id:portable   value:rgb(0.65,0.95,0.55) legend:Apple_IIc`
`    id:special2    value:rgb(1,0.8,0.5)`
`    id:special    value:rgb(1,0.7,0.4) legend:Apple_IIGS`
`    id:line       value:rgb(1,0,0)`
`    id:lightline  value:rgb(0.9,0.9,0.9)`
`    id:lighttext  value:rgb(0.6,0.6,0.6)`
`    id:current    value:rgb(0.8,0.8,0.8) legend:Lisa/Macintosh`

BackgroundColors = canvas:bg ScaleMajor = gridcolor:lighttext unit:year increment:1 start:01/01/1976 ScaleMinor = gridcolor:lightline unit:month increment:3 start:01/01/1976

BarData =

` Barset:apple`
` Barset:null`
` Barset:macintosh`

PlotData=

` width:15 textcolor:black`

` barset:apple`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:ap1 from:07/01/1976 till:09/01/1977 text:"`[`Apple``   ``I`](../Page/애플_I.md "wikilink")`"`
`   color:040 from:04/01/1977 till:06/01/1979 text:"`[`Apple``   ``II`](../Page/애플_II.md "wikilink")`"`
`   color:apiii-b from:09/01/1980 till:12/01/1983 text:"`[`Apl.``   ``III`](../Page/애플_III.md "wikilink")`"`
`   color:050 from:01/01/1983 till:03/01/1985 text:"`[`Apple``   ``IIe`](https://ko.wikipedia.org/wiki/애플_IIe "wikilink")`"`
`   color:portable from:04/01/1984 till:09/01/1986 text:"`[`Apple``   ``IIc`](https://ko.wikipedia.org/wiki/애플_IIc "wikilink")`"`
`   color:special from:09/01/1986 till:10/01/1989 text:"`[`Apple``   ``IIGS`](../Page/애플_IIGS.md "wikilink")`"`
` barset:break`
`   $skip`
`   color:0402 from:06/01/1979 till:12/01/1982 text:"`[`Applie``   ``II``   ``Plus`](../Page/애플_II_플러스.md "wikilink")`"`
`   color:apiii from:12/01/1981 till:12/01/1983 text:"`[`III``   ``Revised`](../Page/애플_III.md "wikilink")`"`
`   color:0502 from:03/01/1985 till:01/01/1987 text:"`[`Enhanced`](https://ko.wikipedia.org/wiki/애플_IIe "wikilink")`"`
`   color:portable2 from:09/01/1986 till:09/01/1988 text:"`[`Mem``   ``Exp.`](https://ko.wikipedia.org/wiki/애플_IIc "wikilink")`"`
`   color:special2 from:10/01/1989 till:12/01/1992 text:"`[`Apple``   ``IIGS``   ``(1``   ``MB)`](../Page/애플_IIGS.md "wikilink")`"`
` barset:break`
`   $skip`
`   $skip`
`   color:apiii-b from:12/01/1983 till:04/01/1984 text:"`[`III``   ``Plus`](https://ko.wikipedia.org/wiki/애플_III_Plus "wikilink")`"`
`   color:050 from:01/01/1987 till:11/01/1993 text:"`[`Apple``   ``IIe``   ``Platinum`](https://ko.wikipedia.org/wiki/애플_IIe "wikilink")`"`
`   color:portable from:09/01/1988 till:09/01/1990 text:"`[`Apple``   ``IIc``   ``Plus`](https://ko.wikipedia.org/wiki/애플_IIc_Plus "wikilink")`"`
`   $skip`
` barset:break`
`   $skip`
`   $skip`
`   $skip`
`   $skip`
`   color:0502 from:03/01/1991 till:05/01/1995 text:"`[`Apple``   ``IIe``   ``Card`](https://ko.wikipedia.org/wiki/애플_IIe_카드 "wikilink")`*"`
`   $skip`

` barset:macintosh`
`   color:mba from:01/01/1983 till:01/01/1984 text:"`[`Lisa`](../Page/애플_리사.md "wikilink")`"`
` barset:break`
`   color:mba2 from:01/01/1984 till:01/01/1986 text:"`[`Macintosh`](../Page/매킨토시_128K.md "wikilink")`"`
` barset:break`
`   color:mba from:01/01/1986 till:04/01/1987 text:"`[`Plus`](https://ko.wikipedia.org/wiki/매킨토시_플러스 "wikilink")`"`
` barset:break`
`   color:mba2 from:04/01/1987 till:10/01/1990 text:"`[`Macintosh``   ``II`](../Page/매킨토시_II.md "wikilink")`"`
` barset:break`
`   color:mba from:10/01/1990 till:04/01/1995 text:"`[`Macintosh``   ``LC`](../Page/매킨토시_LC.md "wikilink")`"`
` barset:break`
`   color:mba2 from:04/01/1995 till:end text:"`[`PPC`](https://ko.wikipedia.org/wiki/파워PC_600 "wikilink")`"`

TextData =

` fontsize:S`
` textcolor:lighttext`
` pos:(490,110)`
` text:*requires Macintosh LC`

</timeline>