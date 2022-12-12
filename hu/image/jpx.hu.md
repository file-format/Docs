{
  "date" : "2021-02-10",
  "keywords" :[ "jpx fájl", "jpx fájlformátum", "mi az a jpx fájl", "fájl", "jpx példa", "jpx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Képfájl formátum",
  "description":"További információ a JPX fájlformátumról és az API-król, amelyek JPX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Mi az a JPX fájl? ##

A .jpx kiterjesztésű fájl a JPEG 2000 fájlformátum kiterjesztése. Elsősorban a JPEG 2000 tömörítést használja, és olyan fejlett funkciókat is biztosít, mint például több réteg egy képhez, különböző színterek, átlátszatlanság és töredezett kódfolyamok. A JPX a JPEG 2000 tömörítésen kívül más tömörítéseket is lehetővé tesz, például JBIG, CCITT Group3, CCITT Group4 stb. A JPX fájlformátumot [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) szabványként hagyták jóvá, de a [JPEG széleskörű használata miatt nem kapott meleg fogadtatást. ](/hu/image/jpeg/) fájlformátum. A JPX fájlokat megnyitni képes alkalmazások közé tartozik a Corel PaintShop Pro, az Adobe Photoshop 2020, az Adobe Illustrator 2020 és a CorelDraw Graphics Suite 2020.

## Rövid története

2000-ben a Joint Photographic Experts Group bizottság megtervezte a JP2-t azzal a céllal, hogy ezzel az új, wavelet-alapú módszerrel javítsák saját diszkrét koszinusz transzformáció alapú JPEG szabványukat. A JPEG bizottság célja az volt, hogy alapmódszereiket licenszdíjmentesen biztosítsák. A JP2 licencben 20 cég közötti versenyben ők nyertek. A JPEG 2000-et ISO szabványnak nyilvánították, bár a legtöbb webböngésző 2017 óta nem áll készen a JPEG 2000-re. 2004-ben az ISO/IEC 15444-2 formátumot nyilvánosan elfogadták a JP2 fájlformátum kiterjesztéseként.

## JPX fájlformátum

A JPX fájlformátumot úgy alakították ki, hogy megfeleljen azon alkalmazások követelményeinek, amelyeknek a [JP2](/hu/image/jp2/) fájlformátum által meghatározott funkcionalitáson túlmutató adatstruktúrákra volt szükségük. A nem kompatibilis kiterjesztésű JP2 fájlok zavart okozhatnak a piacon, ahol egyes olvasók képesek értelmezni egyes JP2 fájlokat, míg másokat nem. A JPX a válasz az ilyen jellegű problémák elkerülésére az alkalmazásokban.

### Fájlazonosító

A JPX fájlok [JPF](/hu/image/jpf/) formátumban tárolódnak, ha hagyományos számítógépes fájlrendszerben tárolják őket. Éppen ezért a JPX kifejezést a JPF-hez képest legkevésbé használják. A JPX fájl a következő bájtokkal kezdődik:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Fájlszervezés

A JP2-hez hasonlóan a JPX fájl olyan dobozok gyűjteménye, amelyek bináris felépítésűek, és a dobozok összefüggő sorrendben vannak elrendezve. Az első doboz a fájl kezdetét adja az első bájtjával, az utolsó doboz utolsó bájtja pedig a fájl utolsó bájtját.
A JPX fájlban lévő doboz bináris szerkezete megegyezik a [JP2](/hu/image/jp2/) fájlformátumban meghatározottal.

### A CodeStream tárolása JPX-ben

A JPX fájlformátum lehetővé teszi a kép kódfolyamának töredékekre való felosztását. Ez lehetővé teszi a kép egyetlen csempéjének módosítását, és a módosított csempének a fájl végére írását anélkül, hogy a teljes fájlt át kellene írni. Az eredeti [JP2](/hu/image/jp2/) fájlformátum korlátozza a teljes kódfolyam tárolását a fájl egy összefüggő részében, ami problémát jelenthet a képszerkesztő alkalmazások számára, amelyek a kép egyetlen csempéjét kívánják módosítani a fenti JPX fájlformátum támogatását. A képkódfolyam töredezettsége a JPX fájlformátumot felülmúlja a JP2 fájlformátumot. Ezenkívül a JPX fájlformátum lehetővé teszi több kódfolyam kombinálását és renderelt eredmény létrehozását. A kódfolyamok összeállításként és animációként kombinálhatók.

## Hivatkozások ##

* [A JPEG 2000 áttekintése](https://jpeg.org/jpeg2000)

