{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid HDR - Cad is comhad íomhá HDR ann?",
  "description": "Foghlaim faoi fhormáid comhaid HDR agus APIs ar féidir leo comhaid HDR a chruthú agus a oscailt.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-gar"
}
},
  "lastmod": "2022-07-21"
}

## Cad is comhad HDR ann?

Is éard atá i gcomhad HDR ná formáid comhaid íomhá raster Raon Arddhinimiciúla (HDR) chun grianghraif ceamara digiteacha a stóráil. Ligeann sé d’eagarthóirí grianghraf cur le dath agus gile na n-íomhánna digiteacha a bhfuil raon teoranta dinimiciúil acu. Is féidir leis an modhnú seo feabhas a chur ar an gile timpeall na coirnéil, rud a fhágann go bhfuil íomhá gar do nádúrtha. De ghnáth déantar comhaid HDR a shábháil mar íomhánna raster 32-giotán. Is féidir le Adobe Photoshop comhaid HDR a chruthú agus a oscailt.

Tugtar HDRI ar chomhaid HDR freisin.

## Formáid Chomhaid HDR - Tuilleadh Eolais

Tá formáid comhaid HDR bunaithe ar bhunfhormáid comhaid Radiance Picture (.pic). De ghnáth, stóráiltear sonraí picteilín comhaid HDR neamh-chomhbhrúite, ach i gcásanna áirithe déantar é a chomhbhrú le córas ionchódaithe fad reatha simplí.

### Struchtúr Comhad HDR

Tá na trí chuid seo a leanas i gcomhad íomhá HDR:

 * **Ceanntásc:** Sainaithnítear comhad HDR leis na chéad bheart sa chomhad íomhá ie #?RADIANCE.
 * ** Teaghrán Taifeach:** Tar éis an Ceanntásc tá líne aonair taifeach ar a bhfuil 4 luach; lipéad X agus Y ar gach ceann agus luach slánuimhir uimhriúil ina dhiaidh sin. Léiríonn ord an X agus Y rothlú. Clúdaíonn an meascán de X agus Y le luachanna dearfacha agus diúltacha gach treoshuíomh agus rothlú imge féideartha.
 * **Sonraí Picteilín:** Tá na sonraí picteilín de chomhad HDR neamh-chomhbhrúite nó comhbhrúite ag baint úsáide as ionchódú fad rite caighdeánach.

## API Foinse Oscailte HDR/HDRI

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Leabharlann ceanntásca singil sár-ghasta tras-ardán [C++] (/programming/cpp/) chun méid agus formáid na híomhá a fháil gan lódáil/díchódú.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Leabharlann meirge chun méid agus formáid na híomhá a fháil gan lódáil/díchódú. Tacaíonn [.avif] (/image/avif/), [.bmp] (/image/bmp/), [.cur] (/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (pictiúr), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/ png/), [psd] (/image/psd/), qoi, tga, tiff (tif), agus webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - cur i bhfeidhm Java ar HdrHistogram.

## Tagairtí

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo]( https://github.com/xiaozhuai/imageinfo)

