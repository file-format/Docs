{
  "date": "2019-10-11",
  "keywords": [
"JAR",
".jar",
"cad is comhad jar ann",
"conas a oscailt comhad jar",
"síneadh",
"comhad",
"comhad jar",
"formáid comhaid jar",
"síneadh .jar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR - Formáid Chomhaid Cartlainne Java",
  "description": "Foghlaim faoi fhormáid comhaid JAR agus APIanna ar féidir leo comhad JAR a chruthú agus a oscailt.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-gar"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad JAR ann?

Is comhad Cartlainne Java é comhad le síneadh .jar ina bhfuil go leor comhaid éagsúla a bhaineann le feidhmchláir mar chomhad amháin. Cruthaíodh an fhormáid comhaid seo chun luas luchtaithe Feidhmchláirín Java íoslódáilte sa bhrabhsálaí trí idirbheart HTTP a laghdú, trí naisc iomadúla HTTP a sheachaint. Féadfaidh comhaid ranga Java ([.class](/programming/class/)), [images](/image/), agus [sounds](/audio/) a bheith i gcomhad JAR amháin. Is féidir le forbróir an fheidhmchláir míreanna aonair laistigh de chomhad JAR a shíniú go digiteach chun a mbunús a fhíordheimhniú. Úsáidtear comhaid JAR go rialta chun APIanna feidhmiúla a chruthú ina bhfuil feidhmiúlacht shonrach a bhaineann leis an API sin.

## Formáid Comhaid JAR

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### An Comhad Manifest

Nuair a chruthaítear comhad JAR, cruthaítear comhad follasach go huathoibríoch taobh istigh de ina bhfuil an fhaisnéis meiteashonraí maidir le hábhar an chomhaid JAR. Taispeánann an comhad seo an t-inneachar atá pacáistithe laistigh den chomhad JAR. Féachtar ar ghnáthchomhad Manifest mar seo a leanas a thaispeánann na fillteáin agus na ranganna atá sa chomhad JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Sonraíochtaí Manifest

Sainmhíníonn Oracle sonraíochtaí follasacha mar seo a leanas.

`comhad follasach`: nualíne na príomhrannóige \*rannán aonair

`príomh-rannán`: leagan-eolas nualíne \*príomh-tréith

`leagan-info`: Manifest-Leagan : leagan-uimhir

`leagan-uimhir' : digit+{.digit+}*

`príomh-tréith`: (aon phríomh-tréith dhlisteanach) nualíne

`rannán-aonair`: Ainm : luach na nualíne \*perentry-attribute

`perentry-attribute`: (aon tréith dlisteanach perentry) nualíne

`nualíne` : CR LF | LF | CR (gan LF ina dhiaidh)

`digit`: {0-9}

### JAR inrite

Is féidir feidhmchlár a bheith i gcomhaid JAR freisin ar féidir le Java Virtual Machine (JVM) é a dhéanamh cosúil le feidhmchlár ar bith eile ar Chóras Oibriúcháin Microsoft Windows. Sa chás seo, ní mór go mbeadh a fhios ag an JVM faoi phointe iontrála an iarratais, is é sin aon aicme le príomh-mhodh poiblí folús statach. Aithníonn an comhad follasach rang dá leithéid le ceanntásc `Príomhranga` san fhormáid seo a leanas:

```
Main-Class: com.example.MyClassName
```



## Tagairtí

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [Formáid Comhaid JAR]( https://en.wikipedia.org/wiki/JAR_(file_format))

