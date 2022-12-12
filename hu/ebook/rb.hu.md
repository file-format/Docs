{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Nuvo Media's Rocket eBook eszköz", "file", "extension", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tudjon meg többet a Nuvo Media Rocket eBook eszközének RB fájlformátumáról és az RB-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"RB - Rocket eBook File",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Mi az RB fájl?

Az .rb kiterjesztésű fájl tartalmazza a Rocket eBook tartalmát. A Rocket eBook valójában a Nuvo Media által gyártott eszköz; 1998-ban adták ki ezt a készüléket. A Rocket eBook ugyan képes képeket megjeleníteni, de csak fekete-fehérben. 106 dpi-s vagy 480 x 320 pixeles képernyővel rendelkezik, 4,5 x 3 hüvelykes érintőképernyőn. A Rocket eBook soros porton keresztül csatlakozik a számítógéphez az e-könyvek RB fájlformátumban történő letöltéséhez. Az RB fájlok képesek DRM használatára, de ezt a technológiát nem használják a modern e-könyvekben. Az RB-fájl hagyományosan tartalmaz egy HTML-fájlt a képeket és egy pszeudo-OPF-fájlt az összes metaadattal (.info).

## Az RB fájlformátum műszaki specifikációja ##

A fájl első 4 bájtjában egy mágikus szám jelenik meg (hexadecimális formában): B0 0C B0 0C.

Úgy tűnik, hogy a következő két bájt egy verziószám, például "02 00", ami a 2-es főverziót és a 0-s mellékverziót jelenti.

A következő négy bájt a "NUVO" szöveget tartalmazza, amelyet 4 bájt 00h követ.

A következő 4 bájt a könyv létrehozásának dátuma, int16-ként kódolva. Ezzel 0Eh eltolást kapunk. Az OrocketLibrary régi verziója az év teljes értékét kódolta (azaz 1999 "CF 07", 2000 "D0 07" volt). A legújabb verzióban a tm_year szó szerint van tárolva, azaz 100 a 2000. évhez ("64 00"). Az év után jön egy int8, amely az 1 relatív hónap számát, és egy int8 a hónap napját.

A következő 6 bájt 00h. Az idő beállításához ezek lefoglalhatók.

A "Tartalomjegyzék" abszolút eltolása egy int32-ben található a 18h eltolásnál.

Ezt követően egy int32, amely az .rb fájl hosszát tartalmazza. Ez annak meghatározására szolgál, hogy a fájlok teljesek-e vagy sem.

Úgy tűnik, ez az egész bájtdarab (20-128 óra) csak egy titkosított címhez szükséges. A nem titkosított címeknél ezek mindig nullák.

A legtöbb esetben a tartalomjegyzék következik (128-as eltolásnál). Az int32 számlálóval kezdődik, amely az „oldal” bejegyzések (.rb-fájl szakaszok) számát tartalmazza a tartalomjegyzékben. Minden bejegyzés egy névből áll (32 bájtig nullázva), majd ezt követi 3 int32: az adatszegmens hossza, az .rb fájl pozíciója és a bejegyzés jelzője. A mai állás szerint az ismert értékek: 1 (titkosított), 2 (információs oldal) és 8 (leeresztett). A nevek szükség szerint személyre szabottak, hogy egyediek legyenek.

## Hivatkozások

* [E-Reader – a MobileRead által](https://en.wikipedia.org/wiki/E-reader)

