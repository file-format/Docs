{
  "date" : "2021-02-15",
  "keywords" :[ "vp6 fájl", "vp6 fájlformátum", "mi az a vp6 fájl", "fájl", "vp6 példa", "vp6 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 – TrueMotion Video File",
  "description":"További információ a VP6 fájlformátumról és az API-król, amelyek VP6 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Mi az a VP6 fájl?

A VP6 egy veszteséges tömörítésű videóformátum, amelyet az On2 technológiák 2003 májusában vezettek be. A TrueMotion által kifejlesztett videokodekek sorozatának része, beleértve a V3-at, V4-et és V5-öt. A formátumot rövidesen a műsorszórásban használták, például a BBC-jelentésekben és a QuickLink szoftverben. A VP6-ot 2005 januárjában a VP7 Codec váltotta fel jobb tömörítési kompatibilitás mellett.

## VP6 fájlformátum

A V6-fájlok teljes specifikációi nem érhetők el nyilvánosan. Az On2 kezdetben nyilvánosságra hozta a specifikációkat, de hamarosan nem tették elérhetővé az általános felhasználók számára. A VP6 fájlformátum nem hivatalos dokumentációja a [multimédiás wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) címen érhető el, amelyre hivatkozhat a fejlesztők számára.

### Makroblokkok (MB)

Az MPEG-2, MPEG-4 2. és 10. részéhez hasonlóan a VP6 fájl minden egyes videokockája 16x16 makroblokk (MB) tömbből áll. Minden MB a következő módok egyikében lehet:

* Intra MB
* Inter MB, null MV, előző kerethivatkozás
* Inter MB, differenciál MV, korábbi keret referencia
* Inter MB, négy MV, korábbi keretreferencia
* Inter MB, MV 1, korábbi kerethivatkozás
* Inter MB, MV 2, korábbi kerethivatkozás
* Inter MB, null MV, könyvjelzővel ellátott kerethivatkozás
* Inter MB, differenciál MV, könyvjelzővel ellátott keretreferencia
* Inter MB, MV 1, könyvjelzővel ellátott keretreferencia
* Inter MB, MV 2, könyvjelzővel ellátott keretreferencia

### Keretfejléc

A VP6 keretfejléce az alábbi ábrán látható, ami követi a big endian bitcsomagolást.

|Szintaxis|Bitek száma|Típus|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 egy kereten belüli|
|qp |6 |Előjel nélküli |A kvantálási paraméter érvényes tartománya 0..63|
|jelölő| 1| Állandó| 0=VP61/62, 1=VP60|
|if (frame_mode == 0) { | 0 | |egyenlő INTRA_FRAME|
|verzió |5| Állandó| 6=VP60/61, 7=VP60(elektronikus művészet), 8=VP62|
|verzió2 |2| Állandó |0=VP60, 3=VP61/62|
|interlace |1| Logikai |true (1) azt jelenti, hogy a sorváltást használják|
|if (jelölő==1 vagy verzió2==0) {||||
|offset |16 |Aláíratlan| másodlagos puffereltolás (a puffer kezdetéhez viszonyított bájtok)|
|}||||
|dim_y |8| Aláíratlan| A videó makroblokk magassága|
|dim_x |8| Aláíratlan| A videó makroblokk szélessége|
|render_y |8 |Unsigned |Videó megjelenítési magassága|
|render_x |8 |Unsigned |Videó megjelenítési szélessége|
|}egyéb{||||
|if (jelölő==1 vagy verzió2==0) {||||
|eltolás |16 |Előjel nélküli |Másodlagos puffereltolás (a puffer kezdetéhez viszonyított bájtok)|
|}||||
|}||||

## Hivatkozások

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

