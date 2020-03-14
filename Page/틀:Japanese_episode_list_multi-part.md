> This article is converted from Wikipedia: [:Japanese episode list multi-part](https://ko.wikipedia.org/wiki/:Japanese_episode_list_multi-part).


<includeonly>

<tr class="vevent" style="text-align: center; background: #{{
  #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
    #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
      #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
    }} | {{
      #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
    }}
  }} | {{
    #if: {{{TopColor|}}} | {{{TopColor}}} | {{
      #if: {{{ShortSummary|}}} | F2F2F2
    }}
  }}
}}">

{{

` #ifeq: {{`
`   #if: `` | {{`
`     #iferror: {{ #expr: 1 <= `` and `` <= 6 }} | 0`
`   }} | 1`
` }} | 0`
` | `
` `

<td style="border-bottom: 3px solid #{{ <!-- Sanity check failed. Give warning -->
    #if: {{{LineColor|}}} | {{{LineColor|}}} | CCF
  }}" colspan="{{
    #expr: {{
      #ifeq: {{{DirectedBy|¬}}}      | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{WrittenBy|¬}}}       | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{Aux1|¬}}}            | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{Aux2|¬}}}            | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{Aux3|¬}}}            | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{Aux4|¬}}}            | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{FirstEngAirDate|¬}}} | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{ProdCode|¬}}}        | ¬ | 0 | 1
    }} + {{
      #ifeq: {{{EpisodeNumber2|¬}}}  | ¬ | 0 | 1
    }} + 3
  }}">

</td>

</tr>

` |   `

<th scope="row" id="{{
    #if: {{{Season|}}} | s{{{Season}}} |
  }}ep{{{EpisodeNumber}}}" style="text-align: center; font-weight: normal; {{#if:{{{TopColor|}}}|background:#{{{TopColor}}}|{{#if:{{{ShortSummary|}}}||background:#F2F2F2|background:#F9F9F9}} }}" rowspan="{{{NumParts|1}}}">

</th>

{{

`   #ifeq: `` | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}`

<td style="height: 2em; text-align: left">

{{\#if: }}} | 〈**}}}**〉{{\#if: }}}|{{\#if: }}}|(}|}}}}})|(}}})}}|{{\#if: }}}|  <small>}}}</small>}}}}}} }}}

</td>

{{

`   #ifeq: ``            | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``      | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``       | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``            | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``            | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}`

<td rowspan="{{{NumParts|1}}}">

{{

`   #ifeq: `` | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``        | ¬ |   | `

<td id="pc{{{ProdCode}}}" rowspan="{{{NumParts|1}}}">

</td>

` }}{{`
`   #ifeq: ``            | ¬ |   | `

<td rowspan="{{{NumParts|1}}}">

</td>

` }}`

</tr>

{{

`   #if: `` | {{`
`     #ifexpr: `` >= 2 | `

<tr style="background: #{{
        #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
          #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
            #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
          }} | {{
            #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
          }}
        }} | {{
          #if: {{{TopColor|}}} | {{{TopColor}}} | {{
            #if: {{{ShortSummary|}}} | F2F2F2
          }}
        }}
      }}">

<td class="summary" style="height: 2em; text-align: left">

{{ \#if: |〈****〉{{\#if: |{{\#if: |()|()}}|{{\#if: |  <small></small>}}}}}} 

</td>

</tr>

`   }}{{`
`     #ifexpr: `` >= 3 | `

<tr style="background: #{{
        #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
          #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
            #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
          }} | {{
            #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
          }}
        }} | {{
          #if: {{{TopColor|}}} | {{{TopColor}}} | {{
            #if: {{{ShortSummary|}}} | F2F2F2
          }}
        }}
      }}">

<td class="summary" style="height: 2em; text-align: left">

{{

`       #if: `` | 〈``〉``{{`
`         #if: `` | `
`        }}`
`     }}{{`
`       #if: `` | {{`
`         #if: `
`         | `*`"``"`*
`         | "``"`
`       }} | {{`
`         #if: `` |   | `
`       }}`
`     }}{{`
`       #if: `` |  (`<span xml:lang="ja" lang="ja"></span>`)`
`     }}`

</td>

</tr>

`   }}{{`
`     #ifexpr: `` >= 4 | `

<tr style="background: #{{
        #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
          #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
            #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
          }} | {{
            #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
          }}
        }} | {{
          #if: {{{TopColor|}}} | {{{TopColor}}} | {{
            #if: {{{ShortSummary|}}} | F2F2F2
          }}
        }}
      }}">

<td class="summary" style="height: 2em; text-align: left">

{{

`       #if: `` | 〈``〉``{{`
`         #if: `` | `
`        }}`
`     }}{{`
`       #if: `` | {{`
`         #if: `
`         | `*`"``"`*
`         | "``"`
`       }} | {{`
`         #if: `` |   | `
`       }}`
`     }}{{`
`       #if: `` |  (`<span xml:lang="ja" lang="ja"></span>`)`
`     }}`

</td>

</tr>

`   }}{{`
`     #ifexpr: `` >= 5 | `

<tr style="background: #{{
        #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
          #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
            #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
          }} | {{
            #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
          }}
        }} | {{
          #if: {{{TopColor|}}} | {{{TopColor}}} | {{
            #if: {{{ShortSummary|}}} | F2F2F2
          }}
        }}
      }}">

<td class="summary" style="height: 2em; text-align: left">

{{

`       #if: `` | 〈``〉``{{`
`         #if: `` | `
`        }}`
`     }}{{`
`       #if: `` | {{`
`         #if: `
`         | `*`"``"`*
`         | "``"`
`       }} | {{`
`         #if: `` |   | `
`       }}`
`     }}{{`
`       #if: `` |  (`<span xml:lang="ja" lang="ja"></span>`)`
`     }}`

</td>

</tr>

`   }}{{`
`     #ifexpr: `` = 6 | `

<tr style="background: #{{
        #ifeq: {{anchorencode:{{{MainList|{{{1|}}}}}}}} | {{anchorencode:{{PAGENAME}}}} | {{
          #ifeq: {{ #expr: {{{EpisodeNumber}}} mod 2 }} | 0 | {{
            #ifeq: {{{EvenRowColor|¬}}} | ¬ | E9E9E9 | {{{EvenRowColor|}}}
          }} | {{
            #ifeq: {{{OddRowColor|¬}}}  | ¬ | <!--Nothing--> | {{{OddRowColor|}}}
          }}
        }} | {{
          #if: {{{TopColor|}}} | {{{TopColor}}} | {{
            #if: {{{ShortSummary|}}} | F2F2F2
          }}
        }}
      }}">

<td class="summary" style="height: 2em; text-align: left">

{{

`       #if: `` | 〈``〉``{{`
`         #if: `` | `
`        }}`
`     }}{{`
`       #if: `` | {{`
`         #if: `
`         | `*`"``"`*
`         | "``"`
`       }} | {{`
`         #if: `` |   | `
`       }}`
`     }}{{`
`       #if: `` |  (`<span xml:lang="ja" lang="ja"></span>`)`
`     }}`

</td>

</tr>

`   }}`
` }}{{`
`   #ifeq: ``}}} | `` |   | {{`
`     #if: `` | `

<tr>

<td class="description" style="height: 2em; border-bottom: 3px solid #{{
        #if: {{{LineColor|}}} | {{{LineColor|}}} | CCF
      }}" colspan="{{
        #expr: {{
          #ifeq: {{{DirectedBy|¬}}}      | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{WrittenBy|¬}}}       | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{Aux1|¬}}}            | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{Aux2|¬}}}            | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{Aux3|¬}}}            | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{Aux4|¬}}}            | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{FirstEngAirDate|¬}}} | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{ProdCode|¬}}}        | ¬ | 0 | 1
        }} + {{
          #ifeq: {{{EpisodeNumber2|¬}}}  | ¬ | 0 | 1
        }} + 3
      }}">

</td>

</tr>

`   }}`
` }}`

}}</includeonly><noinclude>  </noinclude>