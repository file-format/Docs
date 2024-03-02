{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad AGI - Formáid Chomhéadain Chomhéadain Tairseach Réiltín",
  "description":"Foghlaim faoi cad is formáid comhaid AGI ann le sampla agus APIanna ar féidir leo comhaid AGI a chruthú agus a oscailt.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi-ga",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Cad is comhad AGI ann?

Is comhad scripte é comhad AGI a úsáideann an córas teileafónaíochta foinse oscailte, Asterisk. Tá faisnéis ann ar féidir a úsáid chun próisis agus diaphlean Réiltín a uathoibriú. Trí chomhaid scripte AGI a úsáid, is féidir naisc a bhunú le bunachair shonraí choibhneasta ar nós PostgreSQL nó MySQL. Ina theannta sin, is féidir scripteanna AGI a úsáid chun teacht ar acmhainní seachtracha eile freisin. Is féidir le scripteanna AGI smacht an diailphlean a thiontú go script sheachtrach AGI, rud a chuireann ar chumas Réiltín tascanna casta a dhéanamh.

## Formáid Chomhaid AGI - Tuilleadh Eolais

Sábháltar comhaid scripte AGI mar chomhaid téacs agus is féidir iad a oscailt in aon eagarthóir téacs chun athruithe a dhéanamh.

### Patrún Caighdeánach Cumarsáide AGI

Lódálann an script AGI na hathróga agus na luachanna a sheolann Réiltín chuige. Tá cuma choitianta ar na hathróga seo mar seo a leanas.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Leanann na hathróga seo líne bhán a sheol Réiltín, a thaispeánann gur féidir leis an script AGI smacht a ghlacadh ar an dialphlean anois.

### Teanga ríomhchlárúcháin le haghaidh Comhaid Script AGI

Is féidir scripteanna AGI a scríobh go hiondúil i Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal, nó Bourne Shell.

## Tagairtí

 * [Script AGI réiltín]( https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

