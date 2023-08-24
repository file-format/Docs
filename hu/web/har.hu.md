{
  "date" : "2021-07-08",
  "keywords" :["HAR", "File", "Extension", "File Format", "File Extension", "JSON", "Archive File"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - HTTP archív fájlformátum",
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az a HAR-fájl és API-k, amelyek létrehozhatnak és megnyithatnak HAR-fájlt.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Mi az a HAR fájl?

A .har fájl (HTTP archívum) egy HTTP archív fájl, amely számos böngészőn (például Chrome, Safari, IE, Firefox stb.) keresztüli munkamenetadatokat tárol [JSON] formátumban. (/hu/web/json/) fájlformátum. A szerver és a kliens (jelen esetben a felhasználó böngészője) között az interneten átvitt adatok HTTP kérés- és válaszfejléceket tartalmaznak, amelyeket HAR fájlban tárolnak. Részletes információkat tartalmaz a böngészőbe betöltött weboldalak teljesítményadatairól. A HAR-fájlok bármely szövegszerkesztőben megnyithatók, például a Notepad Microsoft Windows operációs rendszeren és a TextEdit az Apple MacOS rendszeren.

## HAR fájlformátum - További információ

A HAR-fájlok a munkamenet-információkat egyszerű szöveges fájlban tárolják a népszerű JSON formátum használatával. A HAR fájlformátum specifikációit a World Web Consortium (W3C) Web Performance Group készítette, de nem tudták közzétenni. Sikeresen definiált azonban egy archiválási formátumot a HTTP-tranzakciókhoz.

A kérések és válaszok továbbításának felügyelete mellett a fejlesztők a HAR-fájlokat használják a webböngésző teljesítményének naplózására az oldalbetöltési sebesség, a tartalombetöltés időtartama, a betöltött tartalom, a böngészőből érkező válaszok lekérdezései és sok más tekintetében. .

## Miért érdemes HAR fájlokat használni?

A HAR-fájlok segíthetnek a webhely teljesítményének javításában a hosszú betöltési idők, az oldalmegjelenítési idők és a válaszidők értékelésével. A HAR-fájlok elemezhetők, hogy megtalálják az ilyen problémákat, és megoldhatók a webhelytel kapcsolatos problémák a teljesítmény javítása érdekében.

## Hogyan lehet HAR fájlt generálni?

Szóval, hogyan lehet HAR fájlt generálni? Nos, ez attól függ, hogy milyen típusú böngészőt használ a HAR-fájl létrehozásához. Ebben az útmutatóban a Google Chrome böngésző lépéseit soroljuk fel. A HAR fájlok Safari, Firefox stb. használatával történő előállításának módszerei könnyen kereshetők és követhetők az interneten.

### Lépések a HAR-fájl létrehozásához a Google Chrome használatával

A következő lépéseket egy olyan weboldalon lehet végrehajtani, ahol problémák merültek fel.

1. Nyissa meg azt a weboldalt a Google Chrome-ban, ahol a probléma történt.
1. Nyissa meg a fejlesztői eszközt (elem ellenőrzése).
1. Menjen a panel bal oldalán a fájlrögzítés elindításához. Ebben a részben egy kis kerek piros gomb található.
1. Kattintson a „Törlés ikonra” a böngészőben tárolt naplóbejegyzések törléséhez.
1. A kívánt tartalom mentéséhez a fentiek szerint kattintson a jobb gombbal, majd kattintson a „Mentés HAR fájlként” gombra.

## Hivatkozások

* [HAR fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/HAR_(file_format))

