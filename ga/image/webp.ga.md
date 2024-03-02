{
  "date": "2019-10-11",
  "keywords": [
"comhad webp",
"Formáid comhaid webp",
"Cad is comhad webp ann",
"comhad",
"webp shampla",
"síneadh comhad webp",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP - Formáid Chomhaid Íomhá Google Raster",
  "description": "Foghlaim faoi fhormáid comhaid WEBP agus APInna ar féidir leo comhaid WEBP a chruthú agus a oscailt.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad WEBP ann?

Is formáid comhaid íomhá gréasáin raster nua-aimseartha é WebP, a thug Google isteach, atá bunaithe ar chomhbhrú gan chaillteanas agus gan chailliúint. Soláthraíonn sé cáilíocht íomhá céanna agus laghdaítear méid na híomhá go mór. Ós rud é go n-úsáideann an chuid is mó de na leathanaigh ghréasáin íomhánna mar léiriú éifeachtach ar shonraí, is é an toradh a bhíonn ar úsáid íomhánna WebP ar leathanaigh ghréasáin ná lódáil níos tapúla ar leathanaigh ghréasáin. De réir Google, tá íomhánna gan chailliúint WebP 26% níos lú i méid i gcomparáid le [PNGs](/image/png/), agus tá íomhánna caillte WebP 25-34% níos lú ná íomhánna inchomparáide [JPEG](/image/jpeg/). Déantar comparáid idir íomhánna bunaithe ar an innéacs Cosúlachta Struchtúrtha (SSIM) idir WebP agus formáidí comhaid íomhá eile. Is comhthionscadal é WebP de [WebM](https://en.wikipedia.org/wiki/WebM) formáid coimeádán ilmheán.

## Forbhreathnú ar Ghnéithe WebP ##

Úsáideann íomhánna WebP an próiseas comhbhrú bunaithe ar thuar picteilíní óna mbloic máguaird, agus mar thoradh air sin is féidir picteilíní a úsáid go minic i gcomhad amháin. Tacaíonn sé le híomhánna beoite agus táthar ag súil go dtacóidh sé le gnéithe níos mó sa todhchaí. Chuir Google an cód foinse [online](https://developers.google.com/speed/webp/download) ar fáil dá ionchódóir agus dá dhíchódóir ionas gur féidir é a úsáid nuair is gá. Soláthraíonn íomhá WebP tacaíocht do:

* ** Comhbhrú caillteach:** Tá an comhbhrú caillteach bunaithe ar ionchódú fráma eochrach [VP8](https://en.wikipedia.org/wiki/VP8). Is formáid comhbhrú físeáin é VP8 a chruthaigh On2 Technologies mar chomharba ar na formáidí VP6 agus VP7.

* ** Comhbhrú gan chailliúint:** Is í foireann WebP a fhorbraíonn an fhormáid chomhbhrú gan chailliúint.

* **Trédhearcacht:** Tá cainéal alfa 8-giotán úsáideach le haghaidh íomhánna grafacha. Is féidir an cainéal Alfa a úsáid mar aon le RGB caillte, gné nach bhfuil ar fáil faoi láthair in aon fhormáid eile.

* ** Beochan:** Tacaíonn sé le fíor-dathanna íomhánna beoite.

* ** Meiteashonraí:** D’fhéadfadh meiteashonraí EXIF agus XMP a bheith aige (a úsáideann ceamaraí, mar shampla).

* **Próifíl Datha:** D’fhéadfadh próifíl leabaithe ICC a bheith aige.


Úsáideann comhbhrú Lossy WebP códú tuarthach chun íomhá a ionchódú, an modh céanna a úsáideann an CODEC físeáin VP8 chun eochairfhrámaí a chomhbhrú i bhfíseáin. Úsáideann códú tuarthach na luachanna i mbloic picteilín in aice láimhe chun na luachanna i mbloc a thuar, agus ansin ní ionchódaíonn sé ach an difríocht.

Úsáideann comhbhrú WebP gan chailliúint blúirí íomhá atá feicthe cheana féin chun picteilíní nua a athchruthú go beacht. Is féidir leis pailéad áitiúil a úsáid freisin mura bhfaightear meaitseáil suimiúil.

## Formáid Chomhaid ##

Tá formáid comhaid WebP bunaithe ar fhormáid an doiciméid RIFF (formáid comhaid idirmhalartaithe acmhainní). Soláthraíonn an coimeádán WebP tacaíocht do ghnéithe sa bhreis agus níos mó ná nach bhfuil ann ach íomhá amháin atá ionchódaithe mar eochairfhráma VP8. Is é an bunghné de chomhad RIFF ná smután atá comhdhéanta de:


| Réimse | Cur síos
---|---|
|Chunk FourCC: 32 giotán|Cód ceithre charachtar ASCII a úsáidtear chun smután a shainaithint
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-gang
|Ualach Páirteanna: Beart Méid an Chunk|An pálasta sonraí. Má tá Méid an Chunk corr, cuirtear beart stuála amháin ~-~- ar cheart dó a bheith 0 ~-~- leis
|ChunkHeader ('ABCD')|Úsáidte chun cur síos a dhéanamh ar an gceanntásc FourCC agus Chunk Size de smután aonair, áit arb é 'ABCD' an FourCC don smután. Is é méid an eilimint seo ná 8 bytes.

### Ceanntásc WebP ###

Tá ceanntásc comhaid WebP mar seo a leanas:

* Ceanntásc RIFF - 32 giotán a sheasann do na carachtair ASCII 'R' 'I' 'F' 'F'

* Méid an Chomhaid - 32 giotán (uint32) a léiríonn méid an chomhaid i mbeart ag tosú ar fhritháireamh 8. Is é uasluach an réimse seo ná 2^32 lúide 10 beart agus mar sin is é méid an chomhaid iomláin ar a mhéad ná 4GiB lúide 2 beart .

* 'WEBP' - 32 giotán a sheasann do na carachtair ASCII 'W' 'E' 'B' 'P'


### Formáid Chomhaid Lossy ###

Úsáideann íomhánna WebP formáid an chomhaid chaillte má tá an íomhá bunaithe ar ionchódú caillte agus nach dteastaíonn aon ardghnéithe/gnéithe sínte ar nós trédhearcachta, beochana, alfa, etc. Tá íomhánna caillte níos lú agus tacaítear leo ó na feidhmchláir níos sine freisin.

Sa chomhad WebP, sa chás seo, tá:

* Ceanntásc comhaid WebP 12 bytes

* Smután VP8


Léiríonn an [VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) sonraíochtaí formáide srutha giotán VP8.

### Formáid Chomhaid Gan chailleadh ###

Úsáidtear an leagan amach seo nuair a bhíonn an íomhá bunaithe ar ionchódú gan chailleadh agus níl aon ghá leis na hardghnéithe a sholáthraíonn an fhormáid sheachtrach. Seans nach mbeidh feidhmchláir níos sine in ann comhaid dá leithéid a léamh áfach.

Sa chomhad WebP, sa chás seo, tá:

* Ceanntásc comhaid WebP 12 bytes

* Smután VP8L


## Tagairtí ##

* [Tagairt Fhorbróra WebP - Le Google](https://developers.google.com/speed/webp/)

* [Formáid Chomhaid WebP - Le Vicipéid](https://en.wikipedia.org/wiki/WebP)


