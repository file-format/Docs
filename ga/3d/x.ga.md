{
  "date": "2020-01-11",
  "keywords": [
"x comhad",
"x formáid comhaid",
"cad is comhad x ann",
"comhad",
"x sampla",
"x síneadh comhad",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X - Formáid Chomhaid DirectX 2.0",
  "description": "Foghlaim faoi fhormáid comhaid DirectX X agus APIanna ar féidir comhaid DirectX X a oscailt agus a chruthú.",
  "linktitle": "X",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d--gax"
}
},
  "lastmod": "2020-01-11"
}

## Cad is comhad X ann?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. Úsáideadh é le haghaidh rindreáil grafaicí 3D i gcluichí agus sonraíonn sé na struchtúir le haghaidh mogaill, uigeachtaí, beochan, agus réada atá sainithe ag an úsáideoir. Tá sé i léig ó 2014 mar feidhmíonn formáid comhaid Autodesk FBX níos fearr mar fhormáid níos nua-aimseartha. Tá X bunaithe ar theimpléad agus tá sé saor ó aon eolas úsáide.

Is féidir leat comhaid DirectX X a oscailt ag baint úsáide as Microsoft DirectX agus eagarthóirí téacs coitianta.

## Formáid X Comhaid

Tá faisnéis thagartha san [X file reference](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) maidir leis na heilimintí API a úsáidtear chun oibriú le comhaid DirectX .x. Soláthraíonn an fhormáid primitives sonraí ar leibhéal íseal a úsáideann feidhmchláir eile chun primitives ardleibhéil a shainiú trí theimpléid sonraí. Thug DirectX 6.0 comhéadain agus modhanna isteach a chumasaíonn léamh ó chomhaid .x agus scríobh chucu. Thug DirectX 3.0 leagan dénártha den fhormáid comhaid seo isteach.

San {{ HYPERLINK1}} atá sainmhínithe ag DirectX 9 tá faisnéis tagartha do chomhaid .x i nDénártha chomh maith le hIonchóduithe Téacs.

### Ionchódú Dénártha

Sainmhíníonn [binary format](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) an fhormáid DirectX X mar léiriú comharthaithe ar fhormáid an téacs. Is féidir leis na comharthaí seo a bheith ina n-aonar chun struchtúr gramadaí a thabhairt nó is féidir iad a bheith ina n-acmhainní taifid a sholáthraíonn na sonraí riachtanacha.

#### Ceanntásc

Is féidir an ceanntásc dénártha a léamh agus a scríobh ag baint úsáide as na sainmhínithe seo a leanas.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Ionchódú Téacs

Ní bhraitheann comhaid DirectX .x ar an mbealach a úsáidtear an comhad agus ní bhaineann siad go sonrach le feidhmchlár ar bith. Ligeann an cur chuige seo atá bunaithe ar theimpléad gur féidir formáid comhaid .x a úsáid ag aon fheidhmchlár ó chliaint.


#### Ceanntásc

Tá an ceannteideal fad athraitheach éigeantach agus caithfidh sé a bheith ag tús an tsrutha sonraí. Tá na sonraí seo a leanas sa cheanntásc.

|Cineál |Fo-Chineál |Méid |Ábhair |Ciall an Ábhair|
---|---|---|---|---|
|Uimhir Dhraíochta (riachtanach)| | 4 beart |xof |
|Leagan Uimhir (riachtanach) |Móruimhir |2 beart |03 |Mórleagan 3|
| |Mionuimhir |2 beart |02 |Mionleagan 2|
|Cineál formáide (riachtanach)| |4 beart | txt  | Téacschomhad|
| | | |bin | Comhad Dénártha|
| | | | tzip | Comhad Téacs Comhbhrúite MSZip|
| | | |bzip | Comhad Dénártha Comhbhrúite MSZip|
|Méid snámhphointe (riachtanach) | |4 beart| 0064| Snámháin 64-giotán |
| | | |0032 | Snámháin 32-giotán |


## Tagairtí

 * [Oidhreacht X Comhad](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [Tagairt Formáid Comhaid DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

