{
  "date": "2021-06-29",
  "keywords": [
"comhad com",
"cad is comhad com ann",
"comhad",
"com shampla",
"síneadh comhad com",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid COM agus APIs ar féidir leo comhaid COM a chruthú agus a oscailt.",
  "title": "COM - Formáid Comhaid Ordú DOS",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-gam"
}
},
  "lastmod": "2021-06-29"
}

## Cad is comhad COM ann?
Úsáidtear na comhaid COM go simplí chun sraith orduithe nó treoracha a fhorghníomhú. Is éard atá i gcomhad COM ná clár inrite is féidir a rith ó Windows nó MS-DOS. Mar an gcéanna comhad EXE, sábháiltear an comhad COM i bhformáid dhénártha freisin ach tá sé difriúil ó chomhad EXE toisc nach bhfuil aon cheanntásc nó meiteashonraí aige agus freisin go bhfuil an t-uasmhéid thart ar 64KB aige. Nuair a ritheann an comhad COM den chéad uair ar chóras 32-giotán, spreagann sé an chomhpháirt NT Virtual DOS Machine (NTVDM) a shuiteáil. Is féidir an comhad COM a reáchtáil ar an leagan 64-giotán de Microsoft Windows le meaisín fíorúil a thacaíonn le timpeallacht MS-DOS.

## Formáid comhaid COM
Is formáid dhénártha inrite í formáid comhaid COM a úsáidtear i Microsoft Windows nó MS-DOS. Níl sa struchtúr ach sraith treoracha; níl aon cheanntásc ann agus níl aon mheiteashonraí caighdeánacha ann. Stórálann sé a chuid sonraí agus cód go léir in aon mhír amháin agus tá uasmhéid 64KB ag a dhénártha. Ní athlonnaítear formáid an chomhaid seo nuair a dhéantar iarracht é a rith arís. Mar sin lódálann an córas oibriúcháin é ag seoladh réamhshocraithe. Ina theannta sin, is féidir comhad COM a dhéanamh le forghníomhú faoin dá chóras oibriúcháin i bhfoirm **dénártha saille**. Níl aon chomhoiriúnacht iarbhír ag an leibhéal teagaisc. Roghnaítear na treoracha ag an bpointe iontrála le bheith comhionann i bhfeidhmiúlacht ach difriúil sa dá chóras oibriúcháin, agus chun an clár a rith, léim go dtí an chuid den chóras oibriúcháin atá in úsáid. Go bunúsach is dhá chlár dhifriúla é a bhfuil an nós imeachta céanna acu in aon chomhad amháin, agus roghnaíonn an cód an ceann atá le húsáid roimhe sin.
### sampla comhad COM
Nuair a bhíonn comhad COM á fhorghníomhú, léitear na treoracha ón gcéad bheart agus leantar iad i ndiaidh a chéile go dtí go bhfaightear na treoracha deiridh. Seo sampla de chód ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Tagairtí 

* [comhad COM - le Wikipewdia](https://en.wikipedia.org/wiki/COM_file)


