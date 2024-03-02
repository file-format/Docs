{
  "date": "2021-02-15",
  "keywords": [
"comhad vp6",
"formáid comhaid vp6",
"Cad é an comhad vp6",
"comhad",
"vp6 shampla",
"vp6 síneadh comhad",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VP6 - Comhad Físe TrueMotion",
  "description": "Foghlaim faoi fhormáid comhaid VP6 agus APIs ar féidir leo comhaid VP6 a chruthú agus a oscailt.",
  "linktitle": "VP6",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-ga6"
}
},
  "lastmod": "2021-02-16"
}

## Cad is comhad VP6 ann?

VP6 is a lossy compression video format that was introduced by On2 technologies in May 2003. Is cuid de shraith codecs físe atá forbartha ag TrueMotion lena n-áirítear V3, V4 agus V5. Baineadh úsáid as an bhformáid go luath sa réimse craolacháin ar nós tuarascálacha BBC agus bogearraí QuickLink. Tháinig VP7 Codec i gcomharbacht ar VP6 i mí Eanáir 2005 le comhoiriúnacht comhbhrú níos fearr.

## Formáid Chomhaid VP6

Complete specifications for V6 files are not available publicly. On2 made the specifications public initially but soon these were made non-available for general users. An unofficial documentation of the VP6 file format is available at [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) that can be referred for developer's reference.

### Macroblocks (MB)

Cosúil le MPEG-2, MPEG-4 páirteanna 2 agus 10, tá gach fráma físe de chomhad VP6 comhdhéanta de raon de mhacrblocks 16 × 16 (MB). Is féidir le gach MB a bheith i gceann de na modhanna seo a leanas:

 * laistigh de MB
 * Inter MB, MV null, fráma tagartha roimhe seo
 * Idir MB, MV difreálach, fráma tagartha roimhe seo
 * Idir MB, ceithre MV, fráma tagartha roimhe seo
 * Idir MB, MV 1, fráma tagartha roimhe seo
 * Idir MB, MV 2, fráma tagartha roimhe seo
 * Inter MB, MV null, fráma tagartha leabharmharcáilte
 * Idir MB, MV difreálach, fráma tagartha leabharmharcáilte
 * Idir MB, MV 1, fráma tagartha leabharmharcáilte
 * Idir MB, MV 2, fráma tagartha leabharmharcáilte

### Ceanntásc an Fhráma

Tá ceanntásc fráma VP6 mar a thaispeántar thíos a leanann an pacáil giotán mór-endian.

|Comhréir|Líon giotán|Cineál|Siomhanais|
---|---|---|---|
| fráma_mód|1|Uimhríocht|Ciallaíonn 0x0 fráma laistigh|
|qp |6 |Gan síniú |Paraiméadar cainníochtaithe raon bailí 0..63|
|marcóir| 1| tairiseach| 0=VP61/62, 1=VP60|
| má (frame_mode == 0) { | 0 | |ar aon dul le INTRA_FRAME|
|leagan |5| tairiseach| 6=VP60/61, 7=VP60(Ealaíona Leictreonacha), 8=VP62|
|leagan2 |2| Tairiseach |0=VP60, 3=VP61/62|
| idirláimh |1| Boole |fíor (1) a úsáidfear idirlás |
|má tá (marcóir==1 nó leagan2==0) {||||
|fritháireamh |16 |Gan síniú | fritháireamh maolánach tánaisteach (bearta a bhaineann le tús an mhaoláin)|
|}||||
| dim_y |8| Gan síniú| Airde macroblock an fhíseáin |
| dim_x |8| Gan síniú| Leithead macrabhloic an fhíseáin |
|render_y |8 |Gan síniú |Taispeáin airde an fhíseáin|
|render_x |8 |Gan síniú |Taispeáin leithead an fhíseáin|
|}eile{||||
|má tá (marcóir==1 nó leagan2==0) {||||
|fritháireamh |16 |Gan síniú |Fritháireamh maolánach tánaisteach (bearta a bhaineann le tús an mhaoláin) |
|}||||
|}||||

## Tagairtí

* [VP6 Vicipéid]( https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)


