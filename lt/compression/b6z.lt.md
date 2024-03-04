{
  "date": "2019-10-11",
  "keywords": [
"b6z failą",
"b6z failo formatas",
"kas yra b6z failas",
"failą",
"b6z pavyzdys",
"b6z failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "B6Z - B6ZIP archyvo failo formatas",
  "description": "Sužinokite apie B6Z failo formatą ir API, kurios gali kurti ir atidaryti B6Z failus.",
  "linktitle": "B6Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-b6-ltz"
}
},
  "lastmod": "2021-04-05"
}

## Kas yra B6Z failas?

Failas su plėtiniu .b6z yra suspaustas archyvo failas, sukurtas macOS programinės įrangos programa [B6Zip](http://b6zip.com), kuri naudojama failams suspausti ir išskleisti. Tai palyginti naujas archyvo formatas, leidžiantis didesnį suspaudimo koeficientą. B6Z turi atvirą architektūrą ir palaiko failų dydžius iki 900 000 PB. Jis palaiko duomenų glaudinimą, klaidų atkūrimą ir failų apimtį. B6Zip paslaugų programinė įranga yra nemokama MacOS, kad būtų galima atidaryti įvairių tipų suspaustus failus, įskaitant B6Z.

## B6Z failo formatas

B6Z failo formatas yra pagrįstas atvira architektūra ir užtikrina tvirtą glaudinimą naudojant AES-256 šifravimo algoritmą. Jis naudoja LZMA2 kaip numatytąjį glaudinimo metodą, bet taip pat palaiko kitus glaudinimo metodus, kaip nurodyta toliau.

|Metodas|Aprašymas|
---|---|
|LZMA |Optimizuota LZ77 algoritmo versija|
|LZMA2| Patobulinta LZMA versija|
|Išleisti| Įprastas LZ77 algoritmas|
|BZip2| Standartinis BWT algoritmas|
|PPMD| Dmitrijaus Škarino PPMdH|

B6Zip programa palaiko visus šiuos glaudinimo standartus ir yra labai optimizuota, todėl užtikrina didelį greitį. Jis palaiko darbą su [ZIP](/compression/zip/), [TAR](/compression/tar/) ir [RAR](/compression/rar/) failų formatais. B6Z failai yra suglaudinti MIME tipo programa / x-b6z.

## Nuorodos

* [B6Zip](http://b6zip.com)


