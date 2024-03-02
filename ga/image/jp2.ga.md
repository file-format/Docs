{
  "date": "2019-10-11",
  "keywords": [
"Comhad jp2",
"Formáid comhaid jp2 saor in aisce,",
"Cad is comhad jp2 ann",
"comhad",
"sampla jp2",
"Síneadh comhad jp2 saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 - Formáid Chomhaid Íomhá",
  "description": "Foghlaim faoi fhormáid comhaid JP2 agus APIs ar féidir leo comhaid JP2 a chruthú agus a oscailt.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-ga2"
}
},
  "lastmod": "2020-08-10"
}

## Cad is comhad JP2 ann? ##

Is córas códaithe íomhánna agus caighdeán comhbhrú íomhá den scoth é JPEG 2000 (**JP2**). Úsáideann sé teicneolaíocht wavelet chun ábhar gan chailliúint a chódú in aon cháilíocht ag an am céanna. Ina theannta sin, gan aon phionós suntasach maidir le héifeachtúlacht códaithe, tá an cumas ag JPEG 2000 rochtain a fháil ar an ábhar céanna agus é a dhíchódú go héifeachtach i raon rúin agus cáilíochtaí eile. Tá na sruthanna cód in JPEG 2000 inscálaithe go suntasach agus tá réigiúin spéise ann a sholáthraíonn áis do rochtain randamach spásúil.

Seasann JPEG 2000 amach mar cheann de na caighdeáin is inscálaithe. Is féidir codanna éagsúla den íomhá a stóráil trí úsáid a bhaint as cáilíochtaí éagsúla. Is féidir formhéadú feidhmíochta suntasach a bhaint amach trí shruth an chóid a ordú ar bhealaí éagsúla. Mar sin féin, éilíonn JP2 ionchódóirí/díchódóirí casta atá dúshlánach ó thaobh ríomhaireacht de, mar thoradh ar an tsolúbthacht seo. I gcomparáid le JPEG, ní tháirgeann JPEG 2000 ach déantáin imfháinne a dhéanann fáinní gar d’imeall na híomhá agus is féidir a bheith doiléir, agus úsáideann JPEG bloic 8 × 8 de dhéantúsáin amhairc ar féidir a bheith ina ndéantáin fáinneacha agus blocála araon. Ag a bhfuil Suas le 16384 comhpháirt éagsúil leis na toisí i dteiripixel, agus beachtas is féidir a bheith ard le 38 giotán/sampla.

## Stair ##

Sa bhliain 2000, dhear coiste an Chomhghrúpa Saineolaithe Grianghrafadóireachta JP2 leis an gcuspóir a gcaighdeán JPEG scoite bunaithe ar chlaochlú cosine a fheabhsú leis an modh nua seo atá bunaithe ar thonnlet. Bhí sé mar aidhm ag coiste JPEG a modhanna bunlíne a sholáthar saor ó tháillí ceadúnais. Tá JPEG 2000 dearbhaithe mar chaighdeán ISO, cé nach bhfuil an chuid is mó de na brabhsálaí gréasáin réidh chun lámh a thabhairt do JPEG 2000 ó 2017 i leith.

## Páirteanna de chóras códaithe íomhá JPEG 2000 ##

Seo a leanas na príomhchodanna a chomhdhéanann an tsraith iomlán caighdeán do JPEG 2000.


|Cuid|Teideal|Cur Síos|Uimhir
---|---|---|---|
|Cuid 1|Croíchóras códaithe| Sainmhíníonn comhréir sruth cód. Céimeanna éagsúla i gceist le díchódú JPEG 2000 íomhánna. Mínítear bunfhormáid comhaid JP2, meiteashonraí, agus cearta IP atá le soláthar.|ISO/IEC 15444-1
|Cuid 2|Eisínteachtaí|Sainmhíníonn sí síntí do shruth cód formáid comhaid agus ceadaíonn sé taispeántais samplacha HDR, sonraíocht spáis datha, bearradh, claochlú geoiméadrach; beochan éagsúil, meiteashonraí, agus sruth ilchód.|ISO/IEC 15444-2
|Cuid 3|Tairiscint JPEG 2000 (MJ2 nó MJP2)|Cuir isteach formáid comhaid le haghaidh seichimh ghluaisne, ag ionchódú íomhánna i sruth cód neamhspleách.|ISO/IEC 15444-3
|Cuid 4|Comhlíonadh|Sonraítear teicníochtaí tástála maidir le hionchódú agus díchódú agus seiceálann sé comhaid le haghaidh sruthanna cód lom agus comhaid JP2 araon.|ISO/IEC 15444-4
|Cuid 5|Bogearraí tagartha|Cuimsíonn dhá phacáiste cód foinse (Java, C) a chuireann an Croíchóras códaithe i bhfeidhm agus atá ar fáil faoi cheadúnais foinse oscailte.|ISO/IEC 15444-5
|Cuid 6|Formáid chomhchodach comhaid íomhá|Sainmhíníonn sé formáid comhaid JPM agus ceadaíonn sé íomháú doiciméad illeathanaigh d'fheidhmchláir cosúil le facs. Tacaíonn sé le húsáid JBIG2 agus JPEG.|ISO/IEC 15444-6
|Cuid 8|Slánaithe JPEG 2000 (JPSEC)| Cinntíonn sé slándáil idirbheart, inneachar agus teicneolaíochtaí, agus ceadaíonn sé sruthanna giotán JPEG 2000 daingnithe.|ISO/IEC 15444-8
|Cuid 9|JPIP|Sainmhínítear uirlisí i dtimpeallacht líonraithe chun rochtain a fháil ar mheiteashonraí agus ar íomhánna, agus sonraítear Prótacail idirghníomhacha agus éifeachtúla | ISO/IEC 15444-9
|Cuid 10|JP3D|Síneadh toirtmhéadrach ar Chuid 1 agus tugtar isteach toise Z. Síneann sé le coincheap na dtíleanna, na gcódbhloic, na maighne, agus na gnéithe inrochtaineachta 3D réigiún spéise.|ISO/IEC 15444-10
|Cuid 11|JPWL|Déileálann le tarchur dea-eagraithe thar líonra gan sreang atá seans maith go earráidí. Tá an breiseán seo comhoiriúnach le díchódóirí | ISO/IEC 15444-11
|Cuid 13|Ionchódóir leibhéal iontrála|Sainmhínítear cur chun feidhme ionchódóra leibhéal iontrála an Chórais Chódaithe Lárnaigh.|ISO/IEC 15444-13
|Cuid 14|JPXML|Léiriú in XML agus mínítear míreanna marcála agus modhanna chun rochtain a fháil ar shonraí inmheánacha na híomhánna.|ISO/IEC 15444-14
|Cuid 15|HTJ2K (Tearfhorbairt)|Sonraíonn sé algartam códaithe blocála malartach. Tairgeann algartam tréchur méadaithe faoi dheich agus códú/díchódú gan chailliúint.|

## Formáid Chomhaid JP2 ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Cé go ndéanann JPEG 2000 cur síos ar shamplaí íomhá go heisiach, ach cuimsíonn JPEG-1 faisnéis bhreise eile faoin spás datha agus an taifeach atá riachtanach chun an íomhá a ionchódú. Má tá íomhá stóráilte mar chomhad JPEG 2000, úsáidtear an **.jp2** mar shíneadh. Feabhsaítear an fhormáid comhaid seo tuilleadh le síneadh JPEG 2000 cuid-2, a shainíonn meicníochtaí beochana agus cumraíocht sruthanna cód iomadúla in aon íomhá amháin. Úsáidtear an breiseán **.jpx** nuair a shábhálann íomhánna leis an bhformáid chomhaid leathnaithe seo. Toisc nach meastar sonraí sruthchód a shábháil i gcomhaid go príomha, mar sin ní shainítear aon síneadh caighdeánach chun na críche seo. Cé gur chun críocha tástála, is minic a fhaigheann sé an síneadh **.jpc** nó **.j2k**. I gcodarsnacht le JPEG-1, roghnaíonn JPEG 2000 bealach difriúil chun meiteashonraí a ionchódú i bhformáid XML. Úsáidtear an caighdeán 12234-1.4 (ag an gcoiste ISO TC42) mar thagairt idir na clibeanna Exif agus na comhpháirteanna XML. Is féidir le caighdeán ISO, XMP laistigh de JPEG 2000.

### Smután ###
Cuimsíonn comhaid JPEG 2000 smután as a chéile. Tá ceanntásc beart 8 ag gach smután: smután 4-beart (mór-endian, beart ard ar dtús) agus cineál smután 4-beart - ceann amháin de na sínithe réamhshainithe:  jP  nó  jP2 .

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000 sainmhínithe ag fo-chineál a chaithfidh a bheith mar cheann de na luachanna: jp2 (cineál comhaid \*.JP2), jp20 (cineál comhaid \*.JPA),  jpm  (cineál comhaid \*.JPM),  jpx  (cineál comhaid \*.JPX).

Smutáin a atriallta, go dtí go n-aimsítear cineál anaithnid, cruthaímid comhad íomhá/físe JPEG 2000.

### Claochlú datha ###

Ar dtús, tá gá le híomhánna a chlaochlú ó spás dath RGB go spás dath eile. Chun na críche sin, tá dhá bhealach ann: Trasfhoirmiú Datha do-aisiompaithe (TFC) agus Trasfhoirmiú Datha Inchúlaithe (RCT). Úsáideann iar-YC,,B,,C,,R,, spás datha agus ní mór é a chur i bhfeidhm i bpointe deisiúcháin/snámh agus níos déanaí ina spás datha YUV modhnaithe agus inchúlaithe sa nádúr.// // Gan a bheith teoranta do mhúnla RGB, JPEG Úsáideann 2000 teanga claochlú comhpháirteanna iolracha.

### Tíleáil ###

Nuair a dhéantar an claochlú datha, athraíonn an íomhá i réigiúin dronuilleogacha ar a dtugtar tíleanna ar féidir iad a chlaochlú agus a ionchódú ar leithligh. Beidh an méid céanna ag gach tíleanna nó is féidir an íomhá ar fad a mheas mar aon tíl amháin. Baineann díchódóir leas as tíliú agus ídíonn sé níos lú cuimhne nó féadann sé roinnt tíleanna a ionchódú go páirteach. Cé go bhfuil míbhuntáiste ag baint leis an teicníc seo maidir le díghrádú cáilíochta an phictiúir.

### Claochlú Wavelet ###

Déantar íomhá tar éis tíleála a chlaochlú ar thonnlet ar féidir a bheith do-aisiompaithe nó inchúlaithe agus a chur i bhfeidhm trí úsáid a bhaint as an scéim convolution nó ardaithe.

### Cóimheas Comhbhrú ###

Ag brath ar shaintréithe fisiceacha íomhá, faightear gnóthachan comhbhrú de 20% Tá ról ríthábhachtach ag tuar iomarcaíochta spáis JPEG 2000 sa phróiseas comhbhrú agus is gnách go mbainfidh íomhánna ardtaifeach an buntáiste is mó.

## Feidhmchláir a bhfreastalaíonn an caighdeán ## orthu

* Taifeadadh, eagarthóireacht agus stóráil físeáin HD fráma-bhunaithe

* Íomháineachas leighis & bithmhéadracht

* íomhánna satailíte, cianbhraiteacht agus braite gluaisne

* Cumarsáid cliant/freastalaí, dáileadh líonra agus stóráil.

* Pictiúrlann dhigiteach, ranníocaíocht beathaithe HDTV beo, ábhar digitithe closamhairc


## Tagairtí ##

* [Forbhreathnú ar JPEG 2000](https://jpeg.org/jpeg2000/)

* [Córas códaithe íomhá JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


