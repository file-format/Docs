{
  "date": "2019-10-11",
  "keywords": [
"comhad png",
"Formáid comhaid png",
"Cad is comhad png ann",
"comhad",
"sampla png",
"síneadh comhad png",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid PNG - Comhad Íomhá Raster",
  "description": "Foghlaim faoi fhormáid comhaid PNG agus APIanna ar féidir leo comhaid PNG a chruthú agus a oscailt.",
  "linktitle": "PNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pn-gag"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PNG ann?

Is formáid comhaid íomhá raster é comhad **PNG** (Grafaic Líonra Inaistrithe) a úsáideann comhbhrú gan chailliúint. Cruthaíodh an fhormáid comhaid seo in ionad Formáid Idirmhalartaithe Grafaicí ([GIF](/image/gif/)) agus níl aon teorainneacha cóipchirt ag baint leis. Mar sin féin, ní thacaíonn formáid comhaid PNG le beochan. Tacaíonn formáid comhaid PNG le comhbhrú íomhá gan chailliúint a fhágann go bhfuil tóir air i measc a chuid úsáideoirí. Le himeacht ama, tá PNG tagtha chun cinn mar cheann de na formáidí comhaid íomhá a úsáidtear go forleathan.

## Stair Achomair ar Fhormáid Chomhaid PNG

The main reason behind the creation of PNG file format was the patented compression algorithm, Lempel-Ziv-Welch, used in the GIF file format. This along with other GIF limitations created a need for replacement of [**GIF**](/image/gif/) file format. The first proposal and name for PNG file format came in January 1995. Tá príomhimeachtaí maidir le formáidí comhaid PNG liostaithe thíos:

* Deireadh Fómhair 1996: Sonraíochtaí PNG Eisíodh Leagan 1.0 agus foilsíodh é ina dhiaidh sin mar [RFC]( https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Rinneadh Moladh W3C mar an gcéanna i mí Dheireadh Fómhair 1996.

* Nollaig 1998: Eisíodh Leagan 1.1, le roinnt athruithe beaga agus trí smután nua leis.

* Lúnasa 1999: Eisíodh leagan 1.2, ag cur smután breise amháin leis.

* Samhain 2003: Rinneadh Caighdeán Idirnáisiúnta de PNG (ISO/IEC 15948:2003). Níl difríocht bheag idir an leagan seo de PNG agus leagan 1.2 agus ní chuireann sé aon smután nua leis.

* Márta 2004: ISO/IEC 15948:2004


## Comparáid Fheidhmeach GIF agus PNG

Dearadh formáid comhaid PNG le bheith simplí agus iniompartha, gan ualach go dlíthiúil, in-idirmhalartaithe, solúbtha agus láidir. Liostaíonn an tábla seo a leanas na gnéithe GIF a fhaigheann formáid comhaid PNG mar oidhreacht chomh maith le gnéithe nua.

|Gné|GIF|PNG|
---|---|---|
|Íomhánna innéacs-dath de suas le 256 dathanna|Tá|Tá|
|Tacaíocht le haghaidh sruthú|Tá|Tá|
|Trédhearcacht|Tá|Tá|
|Faisnéis choimhdeach|Tá|Tá|
|Crua-earraí agus Neamhspleáchas Ardán|Tá|Tá|
|Éifeachtach|Tá|Tá|
|Íomhánna fíordhathanna suas le 48 giotán an picteilín|Ní hea|Tá|
|Íomhánna liathscála chomh hard le 16 ghiotán in aghaidh an phicteilín|Ní hea|Tá|
|Cainéal alfa iomlán (maisc trédhearcachta ghinearálta)|Ní hea|Tá|
|Eolas gáma íomhá|Ní hea|Tá|
|Iontaofacht|Ní hea|Tá|
|Cur i láthair tosaigh níos tapúla|Ní hea|Tá|

## Struchtúr Comhad PNG

Tá tacaíocht ag beagnach gach Córas Oibriúcháin chun comhaid PNG a oscailt. Mar shampla, tá an cumas ag breathnóir Microsoft Windows comhaid PNG a oscailt mar go bhfuil an tacaíocht atá ar fáil ag an OS mar chuid den suiteáil de réir réamhshocraithe. Is éard atá i gcomhad PNG `síniú` PNG agus sraith de //chunks// ina dhiaidh sin.

### Ceanntásc Comhad PNG

Bíonn na luachanna (deachúla) seo a leanas i gcónaí sna chéad ocht mbeart de chomhad PNG:

{{{137 80 78 71 13 10 26 10 }}}

Léiríonn an síniú seo go bhfuil íomhá PNG amháin sa chuid eile den chomhad, ina bhfuil sraith smután ag tosú le smután IHDR agus ag críochnú le smután IEND.

### Smután ###

Tá ceithre chuid i ngach smután:

**Fad:** Slánuimhir 4-bheart gan síniú a thugann líon na mbeart i réimse sonraí an smutáin. Ní chomhairtear an fad ach an réimse sonraí, ní é féin, an cód cineál smután, nó an CRC. Is fad bailí é nialais. Cé gur cheart go gcaithfeadh ionchódóirí agus díchódóirí an fad mar nach bhfuil sínithe, ní ceadmhach a luach a bheith níos mó ná 231 beart.

**Chunk Type:** A 4-byte chunk type code. For convenience in description and in examining PNG files, type codes are restricted to consist of uppercase and lowercase ASCII letters (A-Z and a-z, or 65-90 and 97-122 decimal). However, encoders and decoders must treat the codes as fixed binary values, not character strings. For example, it would not be correct to represent the type code IDAT by the EBCDIC equivalents of those letters. Additional naming conventions for chunk types are discussed in the next section.

**Sonraí Snámh:** Na bearta sonraí a oireann don chineál smután, más ann dóibh. Is féidir fad nialasach a bheith sa réimse seo.

**CRC:** CRC 4-beart (Seiceáil Iomarcaíochta Timthriallach) arna ríomh ar na bearta roimhe seo sa smután, lena n-áirítear an cód cineál smután agus réimsí sonraí an smutáin, ach gan an réimse faid a áireamh. Bíonn an CRC i láthair i gcónaí, fiú i gcás smután nach bhfuil aon sonraí iontu.

Is féidir le fad na sonraí smután a bheith ar aon líon beart suas go dtí an t-uasmhéid; mar sin, ní féidir le feidhmitheoirí glacadh leis go bhfuil smután ailínithe ar aon teorainneacha níos mó ná bearta.

Is féidir smután a thaispeáint in aon ord, faoi réir na srianta a chuirtear ar gach cineál smután. (Srian suntasach amháin is ea go gcaithfidh IHDR a bheith le feiceáil ar dtús agus go gcaithfidh IEND a bheith le feiceáil ar deireadh; mar sin feidhmíonn an smután IEND mar mharcóir deireadh comhaid.) Is féidir le go leor smután den chineál céanna a bheith le feiceáil, ach amháin má cheadaítear é go sonrach don chineál sin.

#### Cineálacha smután

Déantar na Cineálacha Smután a chatagóiriú i smután **Criticiúil** agus **Coimhdeacha** bunaithe ar an luach ASCII cás-íogair 4-beart a shanntar don Chineál Smuim. Caithfidh gach cur i bhfeidhm na smután criticiúil caighdeánach a thuiscint agus a sholáthar go rathúil. Caithfidh smután IHDR, smután IDAT nó níos mó, agus smután IEND a bheith in íomhá bailí PNG.

### Comhbhrú

Sonraíonn modh comhbhrú PNG 0 (an t-aon mhodh comhbhrú atá sainithe faoi láthair do PNG) comhbhrú deflate/insínte le fuinneog sleamhnáin de 32768 beart ar a mhéad. Is díorthach LZ77 é comhbhrú Deflate a úsáidtear i zip, gzip, pkzip, agus cláir ghaolmhara. Tá taighde fairsing déanta ag tacú lena stádas saor ó phaitinn. Stóráiltear na sonraí comhbhrúite laistigh den sruth sonraí zlib mar shraith bloic, agus is féidir le gach ceann acu sonraí amh (neamh-chomhbhrúite) a léiriú, sonraí comhbhrúite LZ77 atá ionchódaithe le cóid seasta Huffman, nó sonraí comhbhrúite LZ77 atá ionchódaithe le cóid Huffman saincheaptha. Aithníonn giotán marcóra sa bhloc deiridh é mar an bloc deiridh, rud a ligeann don díchódóir deireadh an tsrutha sonraí comhbhrúite a aithint.

#### Scagadh Réamh-Chomhbhrú

Cuirtear scagairí réamh-chomhbhrú i bhfeidhm chun na sonraí íomhá a ullmhú don chomhbhrú is fearr. Sainmhíníonn modh scagaire PNG cúig chineál scagaire bunúsacha mar a leanas:

|Cineál Scagaire|Ainm|Luach Tuartha|
---|---|---|
|0|Tada|Tarchuirtear an scanlíne gan mhodhnú|
|1|Fo|Tarchuireann sé an difríocht idir gach beart agus luach bheart comhfhreagrach an phicteilín roimh ré. ||
|2|Suas|Tá an scagaire Up() díreach cosúil leis an scagaire Fo() ach amháin go n-úsáidtear an picteilín díreach os cionn an phicteilín reatha, seachas díreach ar an taobh clé, mar thuarthóir.|
|3|Meán|Úsáideann an scagaire Meán() meán an dá picteilín chomharsanachta (ar chlé agus os a chionn) chun luach picteilín a thuar.|
|4|Paeth| Ríomhann an scagaire Paeth() feidhm líneach shimplí de na trí picteilín chomharsanachta (ar chlé, thuas, ar chlé uachtarach), ansin roghnaíonn sé mar thuar an picteilín comharsanachta is gaire don luach ríofa.|

Cuirtear algartaim scagtha i bhfeidhm ar `bearta`, ní ar picteilíní, beag beann ar dhoimhneacht ghiotán nó ar chineál dath na híomhá. Oibríonn na halgartaim scagtha ar an seicheamh beart a chruthaítear le scanadhlíne. Má tá cainéal alfa san áireamh san íomhá, déantar na sonraí alfa a scagadh ar an mbealach céanna le sonraí na híomhá.

Nuair a bhíonn an íomhá interlaced, déileáiltear le gach pas den phhatrún interlace mar íomhá neamhspleách chun críocha scagtha. Oibríonn na scagairí ar na seichimh beart déanta ag na picteilíní a tharchuirtear i ndáiríre le linn pas, agus is é an scanline roimhe seo an ceann a tarchuireadh roimhe seo sa phas céanna, ní an ceann in aice leis an íomhá iomlán. Tabhair faoi deara go mbíonn an foíomhá a tharchuirtear in aon phas amháin dronuilleogach i gcónaí, ach go bhfuil leithead agus/nó airde níos lú aige ná an íomhá iomlán. Ní chuirtear an scagadh i bhfeidhm nuair a bhíonn an fhoíomhá seo folamh.

## Tagairtí ##

* [PNG - Leathanach Baile](http://www.libpng.org/pub/png/)


