{
  "date" : "2021-02-10",
  "keywords" :[ "jpf fájl", "jpf fájlformátum", "mi az a jpf fájl", "fájl", "jpf példa", "jpf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPF - képfájl formátum",
  "description":"További információ a JPF fájlformátumról és az API-król, amelyek JPF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Mi az a JPF fájl? ##

A .jpf kiterjesztésű fájl a JPEG 2000 képkódoló rendszer ISO/IEC 15444 kiterjesztése, és az ISO/IEC 15444-2 2. részeként hivatkozik rá. Veszteségmentes (bitmegőrző) és veszteséges tömörítési módszerek készletét határozza meg és adja meg folyamatos tónusú, kétszintű, szürkeárnyalatos, színes digitális állóképek vagy többkomponensű képek kódolásához. Az ISO/IEC 15444-1 első része a [JP2](/hu/image/jp2/)-re vonatkozik, amely a wavelet technológiát használja a veszteségmentes tartalom kódolására, és a JPEG 2000 képfájlformátumok alapja. A JPF fájlformátum nem kapott meleg fogadtatást a JPEG formátum kiterjedt használata miatt. A JPF fájlok megnyithatók olyan népszerű képalkalmazásokkal, mint az Adobe Photoshop 2020, az Adobe Illustrator 2020 és a CorelDraw Graphics Suite 2020.

## Rövid története

2000-ben a Joint Photographic Experts Group bizottság megtervezte a JP2-t azzal a céllal, hogy ezzel az új, wavelet-alapú módszerrel javítsák saját diszkrét koszinusz transzformáció alapú JPEG szabványukat. A JPEG bizottság célja az volt, hogy alapmódszereiket licencdíjak nélkül biztosítsák. A JP2 licensz versenyében 20 cég között pokolian nyertek. A JPEG 2000-et ISO szabványnak nyilvánították, bár a legtöbb webböngésző 2017 óta nem áll készen a JPEG 2000-re. 2004-ben az ISO/IEC 15444-2 formátumot nyilvánosan elfogadták a JP2 fájlformátum kiterjesztéseként.

## JPF fájl formátum

A JPF fájlformátum kiterjesztett dekódolási folyamatokat határoz meg a tömörített képadatok rekonstrukcióhoz való konvertálásához. Ez egy kiterjesztett fájlformátum, amely kiterjesztett kódfolyam szintaxist ad meg, amely információkat tartalmaz a tömörített képadatok értelmezéséhez. Ez a kiterjesztett szabvány meghatároz egy tárolót a kép metaadatainak tárolására, és útmutatást ad a kibővített kódolási folyamatokhoz a forrásképadatok tömörített képadatokká konvertálásához.

### Fájlszervezés

A JPF a formális tárolási fájlformátum, amikor a JPX fájlokat számítógépes fájlrendszerben tárolják. Ezenkívül más ajánlások/nemzetközi szabványok más dobozokat is meghatározhatnak a JPX fájlokon belüli használatra. A JPX-fájlban található összes információnak azonban dobozos formátumban kell lennie; a nem doboz formátumú bájtfolyamok nem találhatók meg a fájlban. A JPX fájlban lévő doboz bináris szerkezete megegyezik a [JP2](/hu/image/jp2/) fájlformátumban meghatározottal.

## Referenciák ##

* [A JPEG 2000 áttekintése](https://jpeg.org/jpeg2000/)
* [ISO/IEC 15444-2:2004](https://www.iso.org/standard/33160.html)

