{
  "date": "2019-10-11",
  "keywords": [
"comhad exif",
"Formáid comhaid exif",
"Cad is comhad exif ann",
"comhad",
"sampla exif",
"síneadh comhad exif",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "Foghlaim faoi fhormáid comhaid EXIF agus APIanna ar féidir leo comhaid EXIF a chruthú agus a oscailt.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-gaf"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad EXIF ann?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. Tá an caighdeán á bhainistiú ag an tSeapáin Leictreonaic agus Teicneolaíocht Faisnéise Tionscail Association (JEITA) mar atá inniu ann. Is caighdeán é EXIF maidir le sonraíochtaí formáidí íomhá agus fuaime a úsáideann ceamaraí digiteacha agus scanóirí go príomha.

Cuimsíonn caighdeán EXIF an fhaisnéis chlibeála agus meiteashonraí leis an gcomhad íomhá. Is féidir faisnéis a bheith sna meiteashonraí amhail samhail ceamara, luas comhla, Dáta agus am, Cró, monaróir, am nochta, taifeach X, taifeach Y etc. De ghnáth bíonn sonraí EXIF i bhfolach de réir réamhshocraithe. Chun na sonraí EXIF a fheiceáil, caithfidh duine na hairíonna radhairc a roghnú laistigh den fheidhmchlár féachana íomhá. Féadfaidh meiteashonraí Exif mionsamhlacha chomh maith le sonraí íomhá teicniúla agus príomhúla a áireamh in aon chomhad íomhá amháin.

## Stair agus Leaganacha ##

* I mí Dheireadh Fómhair 1995, bhunaigh JEIDA Leagan 1. Sa leagan seo shainigh JEIDA an struchtúr, atá comhdhéanta de fhormáid sonraí íomhá agus faisnéis aitreabúide, agus clibeanna bunúsacha.

* Samhain 1997, tugadh isteach leagan 1.1 leis an gcuid is mó de na clibeanna ó leagan 1 ach cuireadh forálacha leis freisin maidir le faisnéis faoi tréith roghnach agus oibriú formáide.

* Meitheamh 1998, Leagan 2 le spás datha sRGB, mionsamhlacha comhbhrúite agus comhaid fuaime.

* Nollaig 1998, Leagan 2.1 le faisnéis feabhsaithe stórála agus tréithe.

* Feabhra 2002, Leagan 2.2, leagan feabhsaithe 2.1 agus críochnú priontála curtha leis.

* Meán Fómhair 2003, Leagan 2.21 le spás datha roghnach ar a dtugtar adobe RGB.


## Formáid Chomhaid EXIF

Úsáideann EXIF na formáidí comhaid seo a leanas agus cuirtear meiteashonraí sonracha leis.

1. [JPEG](/image/jpeg/) - trasfhoirmiú scoite cosine (DCT) le haghaidh comhaid íomhá comhbhrúite.
1. {{ HYPERLINK1}} Rev. 6.0 (RGB nó YCbCr) le haghaidh comhaid íomhá neamh-chomhbhrúite.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) le haghaidh comhaid fuaime (Líneach [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) nó ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM le haghaidh sonraí fuaime neamh-chomhbhrúite, agus [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) le haghaidh sonraí fuaime comhbhrúite).

### Marcóir in úsáid ag EXIF ###

Is é an marcóir 0xFFE0~~0xFFEF ná Marcóir Feidhmchláir, a úsáideann feidhmchlár úsáideora. Mar shampla, úsáideann ceamaraí digi níos sine JFIF (Formáid Idirmhalartaithe Comhad JPEG) chun íomhánna a stóráil. Úsáideann JFIF Marcóir APP0 (0xFFE0) chun sonraí cumraíochta ceamara digi agus íomhá mionsamhlacha a chur isteach. Ina theannta sin, úsáideann EXIF Marcálaí Feidhmchláir chun sonraí a chur isteach, ach úsáideann EXIF Marcálaí APP1 (0xFFE1) chun coinbhleacht le formáid JFIF a sheachaint. Tosaíonn gach formáid comhaid EXIF ón bhformáid seo.


|Marcóir SOI|Marcóir APP1|Sonraí APP1|Marcóir Eile
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Tosaíonn sé ó SOI (0xFFD8) Marker, mar sin is comhad JPEG é. Ansin leanann APP1 Marcóir láithreach. Stóráiltear sonraí uile EXIF sa réimse sonraí APP1 seo. Ciallaíonn an chuid de SSSS ar an tábla uachtarach méid limistéar sonraí APP1 (limistéar sonraí EXIF). Tabhair faoi deara go n-áirítear sa mhéid SSSS méid an tuairisceora féin freisin. Tar éis an SSSS, tosaíonn sonraí APP1. Is sonraí speisialta é an chéad chuid lena sainaithint cibé acu an úsáidtear EXIF nó nach n-úsáidtear, carachtar ASCII EXIF agus 2 beart 0x00. Tar éis limistéar Marcála APP1, leanann na Marcóirí JPEG eile.

### Struchtúr Sonraí Exif ###

Taispeántar struchtúr garbh de shonraí EXIF (APP1) mar atá thíos. Mar a pléadh thuas, tosaíonn sonraí EXIF ón gcarachtar ASCII EXIF agus 2 beart de 0x00, agus ansin leanann sonraí EXIF. Úsáideann EXIF formáid TIFF chun sonraí a stóráil.


|FFE1|Marcóir APP1
---|---|
|SSSS|Sonraí APP1|Méid Sonraí APP1
|45786966 0000|Ceanntásc Exif
|49492A00 08000000|Ceanntásc TIFF
|XXXX. . . .|IFD0 (príomhíomhá)|Comhadlann
|LLLLLLLL|Nasc le IFD1
|XXXX. . . .|Réimse sonraí IFD0
|XXXX. . . .|Exif SubIFD|Comhadlann
|00000000|Deireadh an Nasc
|XXXX. . . .|Limistéar sonraí de chuid Exif SubIFD
|XXXX. . . .|IFD1(íomhá mionsamhla)|Comhadlann
|00000000|Deireadh an Nasc
|XXXX. . . .|Réimse sonraí IFD1
|FFD8XXXX. . . XXXXFFD9|Íomhá mionsamhla

#### Ceanntásc TIFF ####

tá an fhaisnéis seo a leanas i gceanntásc comhaid 8-beart [TIFF](/image/tiff/):

`Beirt 0-1:` An t-ordú beart a úsáidtear laistigh den chomhad. Is iad na luachanna dlíthiúla:II”(4949.H)MM” (4D4D.H).

San fhormáid II”, bíonn an t-ordú beart i gcónaí ón mbeart is lú suntasaí go dtí an beart is suntasaí, le haghaidh slánuimhreacha 16-giotán agus 32-giotán araon. San fhormáid MM”, bíonn ord beart i gcónaí ón gceann is suntasaí go dtí an ceann is lú suntasaí, do shlánuimhreacha 16-giotán agus 32-giotán. Tugtar ordú beart mór-endian air seo.

`Beirt 2-3:` Uimhir threallach ach roghnaithe go cúramach (42) a shainaithníonn tuilleadh an comhad mar chomhad TIFF. Braitheann an t-ordú beart ar luach Beart 0-1.

`bearta 4-7:` Fritháireamh (i mbeart) an chéad IFD. Féadfaidh an t-eolaire a bheith ag suíomh ar bith sa chomhad i ndiaidh an cheanntásca ach ní mór tosú ar theorainn focal. Go háirithe, féadfaidh Eolaire Comhad Íomhá na sonraí íomhá a chuireann sé síos a leanúint. Ní mór do léitheoirí na leideanna a leanúint cibé áit ar féidir leo a threorú. Úsáidtear an téarma fritháireamh beart sa doiciméad seo i gcónaí chun tagairt a dhéanamh do shuíomh maidir le tús an chomhaid TIFF. Tá fritháireamh 0 ag an gcéad bheart den chomhad.

#### Eolaire Comhad Íomhá ####

Cuimsíonn IFD faisnéis faoin íomhá chomh maith le leideanna do na sonraí íomhá iarbhír. Is éard atá ann comhaireamh 2 bheart de líon na n-iontrálacha eolaire (.i. líon na réimsí), agus seicheamh iontrálacha réimse 12 beart ina dhiaidh , agus fritháireamh 4-bheart ina dhiaidh sin ar an gcéad IFD eile (nó 0 mura bhfuil aon cheann). Ní mór 1 IFD ar a laghad a bheith i gcomhad TIFF agus ní mór iontráil amháin ar a laghad a bheith ag gach IFD.

##### Iontráil IFD #####

Tá gach Iontráil IFD 12 beart san fhormáid seo a leanas.


| Beart | Cur síos
---|---|
|0-1|An Chlib a shainaithníonn an réimse
|2-3|An cineál páirce
|4-7|Comhaireamh den chineál a shonraítear
|8-11|An Fritháireamh Luacha, an comhad a fhritháireamh (i mbeart) den Luach don réimse. Táthar ag súil go dtosóidh an Luach ar theorainn focal; mar sin beidh an Fritháireamh Luacha comhfhreagrach mar uimhir chothrom. Fritháireamh an comhad seo maypoint áit ar bith sa chomhad, fiú tar éis na sonraí íomhá

Is aonán loighciúil é réimse TIFF comhdhéanta de chlib TIFF agus a luach. Cuirtear an coincheap loighciúil seo i bhfeidhm mar Iontráil IFD, móide an luach iarbhír mura n-oireann sé don chuid luach/fritháirimh, na 4 beart deiridh den Iontráil IFD. Tá na téarmaí réimse TIFF agus iontráil IFD idirmhalartaithe i bhformhór na gcomhthéacsanna.

#### Íomhá Mionsamhla ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Tá 3 fhormáid le haghaidh mionsamhlacha; Formáid JPEG (Úsáideann JPEG YCbCr), formáid RGB TIFF, formáid YCbCr TIFF.

##### Mionsamhail Formáid JPEG #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Dealraíonn sé go bhfuil formáid JPEG agus 160x120 picteilín méid molta formáid mionsamhlacha do Exif2.1 nó níos déanaí.

##### Mionsamhail Formáid TIFF #####

Más é '1' luach na Clib Comhbhrú(0x0103) in IFD1, níl aon chomhbhrú i bhformáid íomhá mionsamhail (ar a dtugtar íomhá TIFF). Is é pointe tosaigh sonraí mionsamhlacha Clib StripOffset(0x0111), is é méid na mionsamhlacha suim Clib StripByteCounts(0x0117).

## Tagairtí ##

* [EXIF - Le Vicipéid]( https://ga.wikipedia.org/wiki/Exif)

* [Formáid Comhaid EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)


