> This article is converted from Wikipedia: [틀:SGI 컴퓨터 타임라인](https://ko.wikipedia.org/wiki/틀:SGI_컴퓨터_타임라인).


<timeline> DateFormat=mm/dd/yyyy Period = from:01/01/1984 till:01/01/2011 Define $now = 09/01/2007 Define $skip = at:end \# Force a blank line Define $dayunknown = 15 \# what day to use if it's actually not known Define $monthunknown = 06 \# what month to use if it's not actually known ImageSize= width:850 height:auto barincrement:25 TimeAxis = orientation:horizontal PlotArea = right:5 left:5 bottom:60 top:5 Legend = orientation:vertical position:bottom columns:4

Colors =

`    id:bg         value:white`
`    id:m68k1      value:rgb(0.4,0.9,0.8) legend:M680x0`
`    id:m68k2      value:rgb(0.4,1,0.9) `
`    id:mips1      value:rgb(0.75,0.4,1) legend:MIPS`
`    id:mips2      value:rgb(0.85,0.4,0.90)`
`    id:x861       value:rgb(0.60,0.60,1) legend:Itanium`
`    id:x862       value:rgb(0.55,0.55,0.8) legend:X86`
`    id:lightline  value:rgb(0.9,0.9,0.9)`
`    id:lighttext  value:rgb(0.5,0.5,0.5)`

BackgroundColors = canvas:bg ScaleMajor = gridcolor:lighttext unit:year increment:2 start:01/01/1985

BarData =

` barset:terminal`
` barset:workstationlow`
` barset:workstationmid`
` barset:workstationhigh`
` barset:server`
` barset:workstationaltixbased`

PlotData=

` width:15 textcolor:black`

` barset:terminal`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:m68k1 from:$monthunknown/$dayunknown/1984 till:$monthunknown/$dayunknown/1986 text:"`[`1000/1200`](https://ko.wikipedia.org/wiki/SGI_IRIS "wikilink")`"`
` barset:break`
`   color:m68k2 from:$monthunknown/$dayunknown/1986 till:$monthunknown/$dayunknown/1988 text:"`[`2000/2200`](https://ko.wikipedia.org/wiki/SGI_IRIS "wikilink")`"`

` barset:workstationlow`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:m68k1 from:$monthunknown/$dayunknown/1984 till:$monthunknown/$dayunknown/1986 text:"`[`1400`](https://ko.wikipedia.org/wiki/SGI_IRIS "wikilink")`"`
` barset:break`
`   color:m68k2 from:$monthunknown/$dayunknown/1986 till:$monthunknown/$dayunknown/1987 text:"`[`2300`](https://ko.wikipedia.org/wiki/SGI_IRIS "wikilink")`"`
` barset:break`
`   color:m68k1 from:$monthunknown/$dayunknown/1987 till:$monthunknown/$dayunknown/1988 text:"`[`3000`](https://ko.wikipedia.org/wiki/SGI_IRIS "wikilink")`"`
` barset:break`
`   color:mips1 from:10/$dayunknown/1988 till:$monthunknown/$dayunknown/1992 text:"Personal Iris"`
` barset:break`
`   color:mips2 from:$monthunknown/$dayunknown/1993 till:$monthunknown/$dayunknown/1996 text:"`[`Indy`](https://ko.wikipedia.org/wiki/SGI_Indy "wikilink")`"`
` barset:break`
`   color:mips1 from:$monthunknown/$dayunknown/1996 till:08/$dayunknown/2001 text:"`[`O2`](https://ko.wikipedia.org/wiki/SGI_O2 "wikilink")`"`
` barset:break`
`   color:mips2 from:08/$dayunknown/2001 till:01/$dayunknown/2002 text:"`[`O2+`](https://ko.wikipedia.org/wiki/SGI_O2 "wikilink")`"`

` barset:workstationmid`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:mips2 from:$monthunknown/$dayunknown/1986 till:$monthunknown/$dayunknown/1989 text:"Professional Iris"`
` barset:break`
`   color:mips1 from:$monthunknown/$dayunknown/1990 till:$monthunknown/$dayunknown/1994 text:"`[`Indigo`](https://ko.wikipedia.org/wiki/SGI_Indigo "wikilink")`"`
` barset:break`
`   color:mips2 from:01/$dayunknown/1992 till:12/$dayunknown/1997 text:"`[`Crimson`](https://ko.wikipedia.org/wiki/SGI_Crimson "wikilink")`"`
` barset:break`
`   color:mips1 from:01/$dayunknown/2002 till:12/26/2006 text:"`[`Fuel`](https://ko.wikipedia.org/wiki/SGI_Fuel "wikilink")`"`

` barset:workstationhigh`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:mips1 from:10/$dayunknown/1988 till:12/$dayunknown/1991 text:"PowerSeries"`
` barset:break`
`   color:mips1 from:$monthunknown/$dayunknown/1992 till:$monthunknown/$dayunknown/1997 text:"`[`Indigo²`](https://ko.wikipedia.org/wiki/SGI_Indigo²_and_Challenge_M "wikilink")`"`
` barset:break`
`   color:mips2 from:$monthunknown/$dayunknown/1997 till:$monthunknown/$dayunknown/2000 text:"`[`Octane`](https://ko.wikipedia.org/wiki/SGI_Octane "wikilink")`"`
` barset:break`
`   color:mips1 from:$monthunknown/$dayunknown/2000 till:06/25/2004 text:"`[`Octane2`](https://ko.wikipedia.org/wiki/SGI_Octane2 "wikilink")`"`
` barset:break`
`   color:mips2 from:06/$dayunknown/2003 till:12/25/2006 text:"`[`Tezro`](https://ko.wikipedia.org/wiki/SGI_Tezro "wikilink")`"`

` barset:server`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:mips1 from:$monthunknown/$dayunknown/1992 till:$monthunknown/$dayunknown/1997 text:"`[`Challenge``   ``M`](https://ko.wikipedia.org/wiki/SGI_Indigo²_and_Challenge_M "wikilink")`"`
` barset:break`
`   color:mips2 from:$monthunknown/$dayunknown/1996 till:01/$dayunknown/2002 text:"`[`Origin``   ``200`](https://ko.wikipedia.org/wiki/SGI_Origin_200 "wikilink")`"`
` barset:break`
`   color:mips1 from:10/09/2001 till:12/31/2003 text:"Origin 300"`
` barset:break`
`   color:x861 from:$monthunknown/$dayunknown/2005 till:12/$dayunknown/2006 text:"`[`Altix``   ``350`](https://ko.wikipedia.org/wiki/SGI_Altix "wikilink")`"`
` barset:break`
`   color:x862 from:12/$dayunknown/2006 till:end text:"Altix 450, Altix XE"`

` barset:workstationaltixbased`
`   shift:(5,-5) anchor:from fontsize:s`
`   color:x861 from:04/26/2005 till:$monthunknown/$dayunknown/2010 text:"`[`SGI``   ``Prism`](https://ko.wikipedia.org/wiki/SGI_Prism "wikilink")`"`

</timeline>