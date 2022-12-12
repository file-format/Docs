{
  "date" : "2021-03-10",
  "keywords" :[ "ACSM", "Adobe Content Server Message", "extension", "format", "eBook", "file", "Adobe Digital Editions" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az Adobe ACSM-fájlformátumáról és az ACSM-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"ACSM – Adobe Content Server Message File Format",
  "linktitle" : "ACSM",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Mi az ACSM fájl?

Az .acsm kiterjesztésű fájlokat Adobe Content Server Message fájloknak nevezzük. Ezeket a fájlokat az **Adobe Digital Editions** használja az Adobe DRM által védett tartalmak aktiválására és letöltésére. Valójában az ACSM-fájl nem e-könyv-fájl; nem nyitható meg és nem olvasható, mint más e-könyvek (pl. PDF); Csak az e-könyv aktiválásához és letöltéséhez szükséges adatokat tartalmazza. Ez azt jelenti, hogy egy ACSM-fájl csak az Adobe szervereivel kommunikáló információkból áll. A Digital Editions felhasználói láthatják az ACSM fájlt, ha e-könyvet fognak letölteni, de a letöltés bármilyen okból leállt volna. A felhasználók az .acsm fájlra duplán kattintva folytathatják a letöltést.

## Hogyan működik az ACSM fájl?

Mivel az Adobe Content Server feladata az e-könyvek és más digitális tartalmak védelme. A vásárlás után a tartalom automatikusan a vevő Adobe azonosítójához kapcsolódik. Az azonosító privát és nem adható át másoknak. A felhasználónak be kell állítania, mielőtt bármilyen Adobe másolásvédelemmel ellátott dokumentumot vásárolna. Az ügyfelek nem férhetnek hozzá másolásvédett dokumentumaikhoz anélkül, hogy átadnák Adobe ID-jüket a háttérben futó Adobe szerveralkalmazásnak.

Amikor az ügyfelek vásárolnak, az ACSM az egyetlen fájl, amelyet először letölthetnek. Az ACSM-fájl megnyitásához az ügyfélnek telepítenie kell az Adobe Digital Editions szoftvert a rendszerére, és össze kell kapcsolnia az Adobe azonosítójával. Az Adobe Digital Editions ellenőrzi az ACSM-fájl konvertálására vonatkozó jogosultság azonosítóját. Hitelesítés esetén a felhasználó letöltheti e-könyvét [EPUB](/hu/ebook/epub/) vagy [PDF](/hu/pdf/) formátumban. Az Adobe Digital Editions az ACSM fájlt is használja a letöltési könyvtár felismerésére.

## Hivatkozások

* [Adobe Content Server – a Wikipedia által](https://en.wikipedia.org/wiki/Adobe_Content_Server)


