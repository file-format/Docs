{
  "date": "2019-10-11",
  "keywords": [
"comhad mf",
"mf",
"síneadh",
"formáid",
"Formáid comhaid mf"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF - Formáid Chomhaid Manifest Java",
  "description": "Foghlaim faoi fhormáid comhaid MF agus APIanna ar féidir leo comhaid MF a chruthú agus a oscailt.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-gaf"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad MF ann?

Is comhad Java Manifest é comhad a bhfuil iarmhír .mf air ina bhfuil faisnéis faoi na hiontrálacha comhaid aonair [JAR](/programming/jar/). Tá an comhad MF féin laistigh den chomhad JAR agus soláthraíonn sé an síneadh agus an sainmhíniú ar fad a bhaineann le pacáiste. Is féidir comhaid JAR a tháirgeadh le húsáid mar chomhad inrite. I gcás den sórt sin, sonraíonn an comhad mainfest príomhaicme an fheidhmchláir ina bhfuil ráiteas **`poiblí ar neamhní statach príomh`**. Ainmnítear comhaid fhollasacha mar MANIFEST.MF agus is féidir iad a oscailt le haon eagarthóir téacs ar Chórais Oibriúcháin Windows, MacOS agus Linux.

## Sonraíochtaí Formáid Comhad Manifest

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Príomhranna

Príomhchuid:

* ina bhfuil faisnéis maidir le slándáil agus cumraíocht faoin gcomhad JAR

* ina bhfuil faisnéis faoin bhfeidhmchlár nó faoin síneadh a bhfuil an comhad JAR mar chuid de

* sainmhíníonn sé na príomh-tréithe do gach mír follasach aonair


**Nóta**: Ní féidir Ainm a thabhairt ar aon tréith sa chuid seo.

### Rannóga Aonair

Sainmhíníonn rannóg aonair tréithe éagsúla do phacáistí nó do chomhaid comhaid JAR. Caithfidh gach rannóg tosú le tréith darb ainm Ainm a gcaithfidh a luach a bheith ina chonair choibhneasta leis an gcomhad, nó ina URL iomlán a dhéanann tagairt do shonraí lasmuigh den chartlann.

### Sonraíochtaí Manifest

|Tréithe|Cur síos|
---|---|
|comhad follasach|nualíne na príomhrannóige *rannán aonair|
|príomhroinn|leagan-faisnéis nualíne *príomh-thréith|
|leagan-info|Leagan-Manifest : uimhir an leagain|
|uimhir leagain|digit+{.digit+}*|
|príomh-tréith|(príomh-tréith dhlisteanach ar bith) nualíne|
|rannán-aonair|Ainm : luach na nualíne *perentry-attribute|
|tréithe-peanais|(aon aitreabúid buana dlisteanach) nualíne|
|nualíne|CR LF | LF | CR (gan LF ina dhiaidh)|
|digit|{0-9}|

## Tagairtí

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [Formáid Comhaid JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

