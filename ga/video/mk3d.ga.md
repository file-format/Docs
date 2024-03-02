{
  "date": "2021-23-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid MK3D",
  "keywords": [
"mk3d",
"Físeán matroska",
"Formáid mkv",
"3d steirióscóp",
"SteirióMód",
"físeán",
"comhad",
"formáid"
],
  "description": "Foghlaim faoi fhormáid comhaid MK3D le haghaidh físeáin 3d stereoscópacha cruthaithe ag Matroska agus APIs ar féidir leo comhaid MK3D a chruthú agus a oscailt.",
  "linktitle": "MK3D",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk3-gad"
}
},
  "lastmod": "2021-23-02"
}

## Cad is comhad MK3D ann? ##

Baineann na comhaid MK3D leis an teaghlach formáidí físeáin Matroska. Is físeáin **steirióscópacha 3d** iad na comhaid seo a cruthaíodh le formáid Matroska 3D. Úsáideann an Coimeádán comhad MKV luach réimse StereoMode chun an cineál ábhar físe 3D steiréascópach a shainiú. Tá luach StereoMode ar fáil freisin chun na seanfhíseáin 3D steirió a thaispeáint trí dathanna cian agus dearg a scaradh (AnaGlyph)

## Sonraí Teicniúla ##
Is féidir na físeáin 3D a chomhbhrú ar an dá bhealach seo a leanas:

- Rian ar leith do gach súl.
- Comhcheangail gach rianú súl i rian amháin.

Tacaíonn an coimeádán comhaid MKV leis an dá cheann.

Maidir leis na físeáin aon-rianta atá níos éasca leis an ábhar 3D taobh istigh díobh, caithfidh tú an réimse ** StereoMode** a shocrú a chinneann an bhfuil na heitleáin le chéile sa mona nó ar chlé le chéile ar dheis. Is féidir leat ceann de na luachanna réimse StereoMode seo a leanas a úsáid:

|Luach | Cur Síos |
|---|---|
|0| mona|
|1| taobh le taobh (tá an tsúil chlé ar dtús)|
|2| barr-bun (tá an tsúil dheas ar dtús)|
|3| barr-bun (tá an tsúil chlé ar dtús)|
|4| seicchlár (ar dheis ar dtús)|
|5| seicchlár (ar chlé ar dtús)|
|6| ró idirdhuilleogach (ar dheis ar dtús)|
|7| ró idirdhuilleogach (ar chlé ar dtús)|
|8| colún idirdhuilleach (ar dheis ar dtús)|
|9| colún idirdhuilleach (ar chlé ar dtús)|
|10| anaglyph (cian/dearg)|
|11| taobh le taobh (tá an tsúil dheas ar dtús)|
|12| anaglyph (glas/maganta)|
|13| an dá shúil lactha i mBloc amháin (tá an tsúil chlé ar dtús) (modh seicheamhach réimse)|
|14| an dá shúil lactha i mBloc amháin (tá an tsúil dheas ar dtús) (modh seicheamhach réimse)|

Maidir leis na rianta iolracha, ní mór don choimeádán MKV feidhmiúlacht gach rian a chinneadh ar leithligh. Úsáidtear an **TrackOperation** le **TrackCombinePlanes** chun an jab a dhéanamh.


## Tagairtí ##

- [Matroska Specification Notes](https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

