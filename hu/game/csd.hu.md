{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a CSD Steam Game Data Backup fájlformátumról és az API-król.",
  "title" :"CSD fájlformátum - Steam játék adatmentési fájl",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Mi az a CSD fájl?

A CSD-fájl a **Steam** játékszolgáltatás által generált játékmentési fájl, amely lehetővé teszi a felhasználók számára a **Valve** játékok letöltését és kezelését. Tartalmazza a játékokhoz kapcsolódó biztonsági mentési adatokat, amelyek segítségével visszaállíthatja a törölt játékokat. A Steam csak akkor tudja visszaállítani a játékot CSD-fájlból, ha a játék letöltése, telepítése és javítása a Steamen keresztül történt. A játék CSD-fájlból történő visszaállításához használja a Steam → Biztonsági mentés és visszaállítás Gamesteam lehetőséget, és válassza ki a fájlt.

## CSD fájlformátum - További információ

A CSD fájlformátum belső szerkezete nem elérhető nyilvánosan, és a fájlformátum specifikációi nem állnak rendelkezésre a fejlesztők számára. A CSD-fájlokat CSM- és ISS-fájlok kísérik, amelyek szintén Steam-játékfájlformátumok.

### Hol találhatók a Steam biztonsági mentési fájlok?

A teljes Steam biztonsági mentési fájl a következő helyeken található:

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Egyéni konfigurációk és konfigurációs szkriptek
* \downloads\ - Egyéni tartalom többjátékos játékokhoz
* \maps\ - Egyéni térképek, amelyeket többjátékos játékok során telepítettek vagy töltöttek le
* \anyagok\ - Egyedi textúrák és felületek
* \SAVE\ - Egyjátékos mentett játékok

A harmadik fél által készített játékok helye azonban eltérő lehet, és azt a játék fejlesztője határozza meg.

### Visszaállítás CSD biztonsági mentési fájlból

Telepítse a Steam-et, és jelentkezzen be a megfelelő Steam fiókba (további utasításokért lásd: Steam telepítése)
* Indítsa el a Steam programot
* Kattintson a "Steam" gombra a Steam alkalmazás bal felső sarkában
* Válassza a "Játékok biztonsági mentése és visszaállítása..." lehetőséget.
* Válassza az "Előző biztonsági mentés visszaállítása" lehetőséget
* Keresse meg a játék biztonsági mentési fájljainak helyét
* Folytassa a Steam ablakon keresztül a szükséges játékok telepítéséhez.

## Hivatkozások

* [A Steam biztonsági mentési funkció használata](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

