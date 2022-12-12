{
  "date" : "2021-04-08",
  "keywords" :[ "pkg fájl", "pkg fájl formátum", "mi az a pkg fájl", "fájl", "pkg példa", "pkg fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG – bővíthető archív fájlformátum",
  "description":"További információ a PKG fájlformátumról és az API-król, amelyek PKG fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Mi az a PKG fájl?

A .pkg kiterjesztésű fájl egy telepítőcsomag fájl, amely szoftver telepítésére szolgál a macOS rendszeren. A Macintosh számítógépeken kívül iPhone-on is használják. A beépített Apple telepítőalkalmazással telepítheti a PKG fájl tartalmát. A PKG fájl hasonló a Windows operációs rendszeren a szoftver telepítéséhez használt MSI fájlhoz. A telepítés során ezek a csomagfájlok naplózhatnak üzeneteket, amelyek képet adnak arról, hogy milyen extra dolgokat telepít a csomag.

## PKG fájl formátum

A PKR bináris fájlok, amelyek tömörítésre kerülnek a teljes fájlméret csökkentése érdekében. Az OSX 10.5 óta az Apple egyetlen telepítőfájlt tartalmazó, sima csomagokat vezetett be. Ezek eltérnek a korábbi csomagolási formátumoktól, amelyek inkább kötegként, nem pedig különálló fájlokként érkeztek. Ezek a kötegelt csomagok strukturált könyvtárhierarchiát tartalmaztak, amely a fájlokat úgy tárolta, hogy megkönnyítse azok visszakeresését valamilyen indexfájlon keresztül. A lapos PKG fájlformátum valójában egy [XAR](/hu/compression/xar/) archívum, amely a következőket tartalmazza:

* Fejléc – Meghatározza a méretet, az ellenőrző összeget és a verzióinformációkat
* Tartalomjegyzék – UTF-8 kódolású (és kötelező) XML-dokumentum, amelyet a fájl elején tárolnak, így egyszerűvé válik az archívum átvizsgálása az egyes fájlok kibontásához
* Heap – a TOC által hivatkozott strukturálatlan adathalom

## Hivatkozások

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG – Wikipédia](https://en.wikipedia.org/wiki/.pkg)

