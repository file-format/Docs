{
  "date": "2019-10-11",
  "keywords": [
"comhad bmp",
"Formáid comhaid bmp",
"Cad is comhad bmp ann",
"comhad",
"sampla bmp",
"Síneadh comhad bmp saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP - Formáid Comhad Íomhá",
  "description": "Foghlaim faoi fhormáid comhaid BMP agus APIs ar féidir leo comhaid BMP a chruthú agus a oscailt.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-gap"
}
},
  "lastmod": "2019-09-10"
}

# Cad is comhad BMP ann? #

Is ionann comhaid a bhfuil síneadh .BMP acu agus comhaid Íomhá Giotán a úsáidtear chun íomhánna digiteacha bitmap a stóráil. Tá na híomhánna seo neamhspleách ar oiriúntóir grafaice agus tugtar formáid comhaid giotánmap neamhspleách feiste (DIB) orthu freisin. Feidhmíonn an neamhspleáchas seo chun an comhad a oscailt ar ardáin iolracha ar nós Microsoft Windows agus Mac. Is féidir le formáid comhaid BMP sonraí a stóráil mar íomhánna digiteacha déthoiseacha i bhformáid mhonacrómach chomh maith le dath le doimhneachtaí dath éagsúla.

## Sonraíochtaí Formáid Chomhaid BMP ##

Feidhmíonn Giotán Neamhspleách Gléasanna mar áis chun giotáin a mhalartú idir gléasanna agus feidhmchláir. Mar gheall ar éabhlóid leanúnach na formáide comhaid seo, féadfaidh an fhaisnéis atá sna ceanntásca a bheith difriúil de réir an leagan de Bitmap. Is éard atá i gcomhad giotánmap amháin struchtúir sheasta chomh maith le struchtúir de mhéid athraitheach i seicheamh ar leith.

Socraítear struchtúir i gcomhad Giotán san ord seo a leanas:


|Struchtúr|Roghnach|Méid|Cuspóir
---|---|---|---|
|Ceanntásc an Chomhaid|Níl|14|Chun faisnéis ghinearálta a stóráil faoin gcomhad íomhá ghiotán
| Ceanntásc DIB|Níl|Méid Shocraithe|Chun faisnéis mhionsonraithe a stóráil faoin íomhá ghiotán agus an fhormáid picteilín a shainiú
|Masc Giotán Breise|Tá|12 nó 16 beart|Chun formáid na bpictiúr a shainiú
|Pailéad Dathanna|Leath-roghnach|Méid inathraithe|Chun dathanna a shainiú a úsáideann na sonraí íomhá léarscáile giotán
|Bearna1|Tá|Méid inathraithe|Ailíniú struchtúir
|Eagar Picteilín|Níl|Méid inathraithe|Sainmhínítear formáid picteilín ag an gceanntásc DIB nó maisc Giotán Breise.
|Bearna2|Tá|Méid athraitheach|Ailíniú struchtúir
|Próifíl datha ICC|Tá|Méid inathraithe|Chun an phróifíl datha a shainiú do bhainistiú datha

Nuair a luchtaítear íomhá léarscáil ghiotán isteach sa chuimhne, déantar struchtúr DIB de, a úsáideann Windows trína API GDI. Níl an ceanntásc Comhad mar chuid den struchtúr sonraí seo. Is féidir leis an dath a bheith comhdhéanta freisin d’iontrálacha 16-giotán arb ionann iad agus innéacsanna don pailéad a bhfuil tagairt déanta dó in ionad sainmhínithe dath RGB sainráite. Breathnaímis go mion ar chuid acu seo, go háirithe na ceanntásca.

### Ceanntásc Comhad Giotán ###

Tá Ceanntásc Comhad Giotán cosúil le ceanntásca comhaid eile a úsáidtear chun an comhad a shainaithint. Ós rud é go bhfuil leaganacha éagsúla le formáid comhaid BMP, is iad na chéad 2 beart den fhormáid comhaid BMP ná carachtar B agus ansin an carachtar M in ionchódú ASCII. Stóráiltear na luachanna slánuimhreacha go léir i bhformáid bheag-endian.

|Heics fhritháireamh|Fritháireamh Dec|Méid|Cuspóir
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – eagar léarscáil ghiotán struchtúr OS/2 * ** CI** – OS/2 struchtúr deilbhín datha * **CP** – pointeoir datha OS/2 const * **IC** – deilbhín struchtúr OS/2 * **PT** – pointeoir OS/2
|02|2|4 bytes|Méid an chomhaid BMP i mbearta
|06|6|2 beart|Ar cosaint; Braitheann luach iarbhír ar an iarratas a chruthaíonn an íomhá
|08|8|2 beart|Ar cosaint; Braitheann luach iarbhír ar an iarratas a chruthaíonn an íomhá
|0A|10|4 beart|Fritháireamh, ie seoladh tosaigh, an bhirt mar a bhfuil na sonraí íomhá giotánmap (eagar picteilín) le fáil.

#### ceanntásc DIB (ceanntásc faisnéise bitmap) ####

Tá an fhaisnéis mhionsonraithe faoin íomhá léirithe ag an gceannteideal seo. Bunaithe ar an eolas seo, cinnfear feidhmchlár a úsáidfear chun an íomhá a thaispeáint ar an scáileán. Tá réimse DWORD (32-giotán) ag gach ceanntásc den sórt sin, ag sonrú a mhéide, ionas gur féidir le feidhmchlár an ceanntásc a úsáidtear san íomhá a chinneadh go héasca. Tá sé seo go bunúsach mar gheall ar an bhfíric go ndearnadh roinnt síntí ar fhormáid DIB. Seo a leanas Ceanntásc DIB le réimsí liostaithe.

#### Pailéad Dathanna ####

Is sraith struchtúr é pailéad dathanna BMP a shonraíonn luachanna déine RGB gach datha i bpailéad dathanna gléas taispeána. Stórálann gach picteilín sna sonraí bitmap luach amháin a úsáidtear mar innéacs isteach sa pailéad dathanna. Sonraíonn an fhaisnéis datha atá stóráilte san eilimint ag an innéacs sin dath an phicteilín sin. Athraíonn infhaighteacht datha i gcomhad mapa giotán mar seo a leanas:

* Giotán amháin, 4 agus 8 - táthar ag súil go mbeidh pailéad dathanna ann i gcónaí

* Sé cinn déag, 24 agus 32-giotán - nach bhfuil pailéid dathanna riamh

* Comhaid BMP sé bliana déag agus 32-giotán - go bhfuil luachanna masc bitfields in ionad an pailéad dathanna


#### Stóráil picteilíní ####

Stóráiltear picteilíní Giotán mar ghiotán pacáilte i sraitheanna ina ndéantar méid gach ró a shlánú suas go dtí iolraí de 4 beart (DWORD 32-giotán) trí stuáil. Ní féidir méid iomlán na mbeart a theastaíonn chun picteilíní íomhá a stóráil a ríomh go díreach trí na giotán a chomhaireamh. Ós rud é go bhfuil stuáil i gceist, is gá an éifeacht a bhaineann le méid gach ró a shlánú suas go iolraí de 4 beart. Ní mór bearta stuála (ní gá 0) a chur i gceangal le deireadh na sraitheanna chun fad na sraitheanna a thabhairt suas go hiolra de cheithre beart. Nuair a luchtaítear an t-eagar picteilín sa chuimhne, ní mór do gach ró tosú ag seoladh cuimhne ar iolraí de 4 é.

Déantar cur síos iarbhír ar an íomhá ag an léiriú DWORDs 32-giotán den eagar picteilín. De ghnáth, stóráiltear picteilíní bun aníos, ag tosú sa chúinne íochtarach ar chlé, ag dul ó chlé go deas, agus ansin as a chéile ó bhun go barr na híomhá. Tá formáidí picteilíní agus a n-impleachtaí mar atá liostaithe thíos:

* Tacaíonn an fhormáid 1-giotán in aghaidh an picteilín (1bpp) le 2 dhath ar leith, (mar shampla: dubh agus bán).

* Tacaíonn an fhormáid 2-ghiotán in aghaidh an phicteilín (2bpp) le 4 dhath ar leith agus stórálann sí 4 phicteilín in aghaidh 1 bheart, agus an picteilín is mó ar chlé sa dá ghiotán is suntasaí. Is innéacs 2-ghiotán é gach luach picteilín i dtábla suas le 4 dhath.

* Tacaíonn an fhormáid 4-ghiotán in aghaidh an picteilín (4bpp) le 16 dhath ar leith agus stórálann sé 2 phicteilín in aghaidh 1 bheart, agus an picteilín is mó ar chlé sa nibble is suntasaí. Is innéacs 4-ghiotán é gach luach picteilín i dtábla suas le 16 dhath.

* Tacaíonn an fhormáid 8-giotán in aghaidh an picteilín (8bpp) le 256 dathanna ar leith agus stórálann sé 1 picteilín in aghaidh 1 beart. Is innéacs é gach beart i dtábla suas le 256 dath.

* Tacaíonn an fhormáid 16-giotán in aghaidh an picteilín (16bpp) le 65536 dathanna ar leith agus stórálann sé 1 picteilín in aghaidh an WORD 2-bheart. Is féidir le gach WORD samplaí alfa, dearg, glas agus gorm de na picteilíní a shainiú.

* Tacaíonn an fhormáid 24-giotán picteilín (24bpp) 16,777,216 dathanna ar leith agus stórálann 1 luach picteilín in aghaidh 3 beart. Sainmhíníonn gach luach picteilín na samplaí dearg, glas agus gorm den picteilín (8.8.8.0.0 i nodaireacht RGBAX). Go sonrach, san ord: gorm, glas agus dearg (8 giotán in aghaidh gach sampla).

* Tacaíonn an fhormáid 32-giotán in aghaidh an picteilín (32bpp) le 4,294,967,296 dathanna ar leith agus stórálann sé 1 picteilín in aghaidh an DWORD 4-beart. Is féidir le gach DWORD samplaí alfa, dearg, glas agus gorm de na picteilíní a shainiú.


## Tagairtí ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Formáid Chomhaid BMP](https://en.wikipedia.org/wiki/BMP_file_format )


