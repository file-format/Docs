{
"dátum": "2023-09-27",
  "keywords": [
"cfg",
"cfg fájl",
"cfg wesnoth jelölőnyelvi fájl",
"mi az a cfg fájl",
"hogyan kell megnyitni a cfg fájlt",
"fájl",
"cfg fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG fájlformátum - Wesnoth jelölőnyelvi fájl",
  "description":"További információ a CFG Wesnoth Markup Language fájlformátumról és az API-król, amelyek CFG-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Mi az a CFG fájl?

A CFG fájl **"Wesnoth Markup Language" (WML)** néven is ismert. Ez egy egyéni jelölőnyelv, amelyet elsősorban a „Battle for Wesnoth” játékban használnak, amely egy körökre osztott stratégiai játék. A WML a játék különböző aspektusainak meghatározására és testreszabására szolgál, beleértve a forgatókönyveket, kampányokat, egységeket és egyebeket. Ez egy módja annak, hogy a modderek és a fejlesztők tartalmat hozzanak létre a játékhoz.

Olyan formátumban íródott, amely hasonlít az XML és az egyszerű szkriptelés kombinációjára. Íme néhány általános elem és struktúra áttekintése, amelyeket a WML-fájlokban találhat:

1. **Címkék:** A WML címkéket használ a játék különböző elemeinek meghatározásához. A címkék szögletes zárójelben vannak. Például:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attribútumok:** A címkéken belül attribútumokat adhat meg az elemhez társított tulajdonságok vagy értékek megadásához. A fenti példában a "type" és a "hitpoints" attribútumok.
    










3. **Tömbök és tömbök:** Adattömböket, sőt tömbtömböket is létrehozhat egységek, tereptípusok vagy más játékelemek listájának meghatározásához.
    










4. **Feltételes utasítások:** A WML támogatja a feltételes utasításokat a játék menetének szabályozására. Például:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Curkok:** A hurkok segítségével ismételheti az elemek listáit, vagy hajthat végre ismételt műveleteket.
    










6. **Tartalmazza:** A fő WML-fájlba más WML-fájlokat is belefoglalhat a tartalom rendszerezéséhez és modularizálásához.
    










7. **Eseménykezelők:** Eseménykezelőket definiálhat, amelyek akciókat indítanak el, ha bizonyos események történnek a játékban.
    











Íme egy egyszerűsített példa egy WML-fájlra, amely egyéni egységet határoz meg:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## A csata Wesnothért

A "The Battle for Wesnoth" egy népszerű és nyílt forráskódú körökre osztott stratégiai játék. Több platformon is elérhető, beleértve a Mac-et, Windows-t, Linuxot és még sok mást. Az önkéntesek elkötelezett közössége által kifejlesztett játék mély és lebilincselő játékmenetéről, valamint gazdag fantáziavilágáról ismert.

A "The Battle for Wesnoth" főbb jellemzői a következők:

1. **Fantasy Setting:** A játék egy fantáziavilágban játszódik, különféle fajokkal, köztük emberekkel, elfekkel, törpökkel, orkokkal és még sok mással. A játék története és történetmesélése a játék vonzerejének szerves részét képezi.
    










2. **Körökre osztott stratégia:** A játékmenet körökre osztott, ahol a játékosok időt szakítanak arra, hogy megtervezzék és végrehajtsák lépéseiket hatszögletű rácsokon. A taktikai harcot a stratégiai döntéshozatallal ötvözi.
    










3. **Kampányok:** A játék egyjátékos kampányok széles skáláját kínálja, mindegyik saját történettel, karakterekkel és kihívásokkal. A játékosok különféle narratívákat és forgatókönyveket fedezhetnek fel.
    










4. **Multiplayer:** A "Wesnoth" támogatja az online többjátékos módot, lehetővé téve a játékosok számára, hogy stratégiai csatákban versenyezzenek egymással. A többjátékos módok közé tartozik a kooperatív játék és a kompetitív meccsek.

## CFG fájl - Mivel nyitható meg?

A „The Battle for Wesnoth” játékban használt Wesnoth Markup Language-hez (WML) általában társított CFG-fájlok bármely szabványos szövegszerkesztővel könnyen szerkeszthetők. Ezek a fájlok WML-ben írt, ember által olvasható kódot tartalmaznak, amely meghatározza a játék különböző aspektusait, beleértve a forgatókönyveket, egységeket és kampányokat.

Bár bármilyen szövegszerkesztővel módosíthatja a CFG-fájlokat, néhány fejlett szövegszerkesztő, például az Emacs és a Vi rendelkezik WML szintaxiskiemelő beépülő modulokkal. Ezek a beépülő modulok hasznos színkódolást és formázást biztosítanak, hogy megkönnyítsék a felhasználók számára a különböző elemek és struktúrák megkülönböztetését a WML-kódon belül.

A CFG fájlokat megnyitó vagy hivatkozó programok közé tartozik

- The Battle for Wesnoth (ingyenes) (Windows, MAC, Linux)
- Microsoft Jegyzettömb

## Egyéb CFG fájlok

Íme más fájltípusok, amelyek a **.cfg** fájlkiterjesztést használják.

**Beállítások**
- [CFG - Celestia konfigurációs fájl](/hu/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/hu/settings/cfg-citrix/)
- [CFG - MAME konfigurációs fájl](/hu/settings/cfg-mame/)
- [CFG - LightWave konfigurációs fájl](/hu/settings/cfg-lightwave/)

**Játszma, meccs**
- [CFG - Wesnoth Markup Language File](/hu/game/cfg-wesnoth/)
- [CFG - MUGEN konfigurációs fájl](/hu/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/hu/game/cfg-sourceengine/)

**Rendszer és egyéb**
- [CFG - CFG fájl](/hu/system/cfg/)
- [CFG - Cal3D modell konfigurációs fájl](/hu/misc/cfg-cal3d/)

## Hivatkozások
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
