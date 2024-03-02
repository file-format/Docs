{
  "date": "2019-10-11",
  "keywords": [
"ico comhad",
"Formáid comhaid ico",
"cad is comhad ico",
"comhad",
"sampla ico",
"Síneadh comhad ico saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO - Formáid Comhad Íomhá",
  "description": "Foghlaim faoi fhormáid comhaid ICO agus APIanna ar féidir leo comhaid ICO a chruthú agus a oscailt.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-gao"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad ICO ann?

Is cineálacha comhaid íomhá iad comhaid a bhfuil síneadh ICO orthu a úsáidtear mar dheilbhín chun feidhmchlár a léiriú ar [Microsoft Windows](https://www.microsoft.com/en-us/windows). Tagann siad seo i méideanna éagsúla, tacaíocht dath agus réiteach chun freastal ar riachtanais an taispeántais. Formáid chomhaid íomhá eile ar Microsoft Windows is ea [CUR](/image/cur/) le haghaidh ionadaíochta cúrsóra agus sainmhíníonn sé hotspot sa cheanntásc íomhá. Ar MacOS, feidhmíonn formáidí comhaid ICNS an cuspóir céanna le comhaid ICO. Soláthraíonn go leor suíomhanna gréasáin ar líne chomh maith le feidhmchláir an ghné de chomhaid den sórt sin a chruthú agus formáidí íomhánna eile ar nós [BMP](/image/bmp/), [PNG](/image/png/), etc. a thiontú go formáid deilbhíní. Is é image/vnd.microsoft.icon an cineál meán Idirlín oifigiúil atá cláraithe le IANA do chomhaid ICO.

## Stair Ghearr ##

Icons were introduced with the launch of Microsoft Windows 1.0. Bhí siad seo 32x32 i méid agus monacrómach. Le teacht ar win32, tugadh isteach tacaíocht d'íomhánna deilbhíní i ndath fíor le suas le 256x256 picteilín i toise. Ba é Windows XP an chéad cheann a chuir tacaíocht ar fáil d’íomhánna deilbhín datha 32-giotán, rud a cheadaigh limistéir leath-thrédhearcacha cosúil le scáthanna, éifeachtaí frith-ailiasacha agus gloine a chur leis an deilbhín. Níor mhol Microsoft ach méideanna deilbhín suas le 48 × 48 picteilín do Windows XP. Chuir Windows Vista deilbhín 256×256-picteilín le Windows Explorer, chomh maith le tacaíocht don fhormáid chomhbhrúite [PNG](/image/png/). Agus úsáideoirí ag baint úsáide as réitigh níos airde agus modhanna arda DPI, moltar formáidí deilbhíní níos mó (amhail 256×256).

## Formáid Chomhaid ICO ##

Is éard atá i gcomhad ICO amháin ná íomhá bheag amháin nó níos mó d'ilmhéideanna agus doimhneacht dathanna. Tá láithreacht íomhánna de mhéideanna iolracha le haghaidh scálaithe cuí ag taifeach scáileáin éagsúla. Léirítear gach luach i gcomhaid ICO/CUR in ord beart [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Tá an comhad ICO comhdhéanta de cheanntásc Deilbhín, Eolaire Deilbhíní,

| Réimse | Cur síos
---|---|
|Ceanntásc Icon|Stórálann sé faisnéis ghinearálta faoin gcomhad ICO.
|Comhadlann[1..n]|Stórálann sé faisnéis ghinearálta faoi gach íomhá sa chomhad.
|Deilbhín #1|Na sonraí iarbhír don chéad íomhá sa seanfhormáid AND/XOR DIB nó PNG níos nuaí
|...|
| Deilbhín #n|Sonraí don íomhá dheilbhín dheireanach

### Ceanntásc ###

|Fritháireamh|Méid (i mbeart)|Cuspóir
---|---|---|
|0|2|Ar cosaint. Caithfidh sé a bheith i gcónaí 0.
|2|2|Sonraíonn an cineál íomhá: 1 le haghaidh íomhá deilbhín (.ICO), 2 le haghaidh íomhá cúrsóra (.CUR). Tá luachanna eile neamhbhailí.
|4|2|Sonraíonn sé líon na n-íomhánna sa chomhad.

### Eolaire ###

San eolaire atá i gcomhad ICO, arna léiriú mar struchtúr ICONDIR, tá struchtúr COMHSHEOLAITHE do gach íomhá sa chomhad. Ina dhiaidh sin tá bloc tadhlach de shonraí léarscáile uile na híomhá. Tá sé seo mar a thaispeántar thíos.

|Fritháireamh|Méid|Cur Síos
---|---|---|
|0 (0)|1|Leithead, ba cheart go mbeadh 0 má 256 picteilín
|1(1)|1|Airde, ba cheart go mbeadh sé 0 má 256 picteilín
|2(2)|1|Comhaireamh datha, ba cheart go mbeadh 0 ann má tá níos mó ná 256 dathanna ann
|3(3)|1|Forchoimeád, ba cheart go mbeadh 0 ann
|4(4)|2|Ba cheart go mbeadh eitleáin dhaite nuair atá siad i bhformáid .ICO, 0 nó 1, nó ba cheart go mbeadh an hotspot X san fhormáid .CUR
|6(6)|2|Giotán in aghaidh na picteilín nuair atá sé i bhformáid .ICO, nó an hotspot Y nuair atá sé i bhformáid .CUR
|8(8)|4|Méid na sonraí giotáin i mbearta.
|12(C)|4|Fritháireamh sa chomhad.

## Tagairtí ##

* [ICO - Le Vicipéid]( https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


