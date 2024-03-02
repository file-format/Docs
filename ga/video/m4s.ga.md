{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad M4S - Cad is comhad M4S ann?",
  "description": "Foghlaim faoi fhormáid comhaid M4S agus APIs ar féidir leo comhaid M4S a chruthú agus a oscailt.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-gas"
}
},
  "lastmod": "2022-07-18"
}

## Cad is comhad M4S ann?

Is éard is comhad M4S ann ná mír bheag d’fhíseán a shruthaítear thar an idirlíon ag baint úsáide as an teicníc sruthú **MPEG-DASH**. Tá deighleog físe ann i bhfoirm sonraí dénártha. Imríonn an t-iarratas glactha (brabhsálaí gréasáin nó seinnteoirí meán de ghnáth) na míreanna seo san ord ina bhfaightear iad. Sainaithnítear an chéad mhír M4S leis na sonraí tosaigh atá ann. In **achoimre**, is codanna beaga meán aonair iad comhaid M4S de chomhad iomlán.

## Formáid Chomhaid M4S

Tá comhaid M4S bunaithe ar an [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Is féidir na codanna beaga seo de chomhad mór a íoslódáil go neamhspleách trí HTTP. Mar sin, má tá comhad mór scannáin {{ HYPERLINK2}} agat, is féidir é a shruthú ag baint úsáide as an teicníc MPEG-DASH (Sruthú Oiriúnaitheach Dinimiciúla thar HTTP) trína dheighilt mar chomhaid mhíre M4S. Má dhéantar an comhad mór scannáin seo a íoslódáil chuig diosca mar M4S, íoslódáiltear go leor comhaid M4S. Má chomhtháthaítear na codanna .m4 seo go léir, cuirfear comhad iomlán inimeartha ar fáil. Ní féidir leis na meáin chumarsáide an comhad a sheinm mura bhfuil an chéad mhír tosaigh ar fáil leis an gcomhad freisin.

## Maidir le Sruthú MPEG-DASH

Úsáideann MPEG-DASH teicníocht sruthaithe giotán oiriúnaitheach a fhágann gur féidir ábhar meán ardchaighdeáin a shruthú ar an idirlíon. Déantar é seo tríd an ábhar a bhriseadh ina sheicheamh de mhíreanna beaga a sruthaítear thar HTTP. Is féidir comhaid mhóra meán ar nós scannáin, podchraoltaí, nó craoladh beo ar imeacht spóirt a shruthú ar an mbealach seo. Tá na codanna seo ionchódaithe ag rátaí giotán éagsúla. Roghnaíonn na himreoirí meán cumasaithe MPEG-DASH an deighleog leis an ráta giotán is airde go huathoibríoch ag baint úsáide as algartam oiriúnaithe ráta giotán. Seachnaíonn sé seo imeachtaí stad nó ath-mhaolánú san athsheinm.

### API Foinse Oscailte do chomhaid M4S

Tá API foinse oscailte ar fáil ar féidir iad a úsáid chun comhaid M4S a léamh agus a thiontú.

 * [libdash](https://github.com/bitmovin/libdash) - .NET API le haghaidh comhaid M4S
 * [dash.js]( https://github.com/Dash-Industry-Forum/dash.js ) - Cliant javascript le haghaidh comhad M4S
 * [Téigh chuig an Leabharlann chun Comhaid Dash a chruthú] (https://github.com/zencoder/go-dash)

### Foinse Oscailte API chun M4S a thiontú go MP4

 * [MFourStoMp4]( https://github.com/muri11o/mfourstomp4)

## Tagairtí ###

* [Formáid Bhunchomhad Meán ISO (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [Sruthú Oiriúnaitheach Dinimiciúla thar HTTP - MPEG-DASH]( https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


