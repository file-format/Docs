{
"dátum": "2023-09-27",
  "keywords": [
"cfg",
"cfg fájl",
"cfg forrásmotor konfigurációs fájl",
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
"title": "CFG fájlformátum - forrásmotor konfigurációs fájl",
  "description":"További információ a CFG Source Engine Configuration File formátumról és az API-król, amelyek CFG fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "CFG Source Engine",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Mi az a CFG fájl?

A CFG fájl a **Valve's Source Engine** kontextusában, ahogy az olyan játékokban látható, mint a Half-Life 2, konfigurációs fájlként szolgál. Ezeket a fájlokat a különböző játékbeli beállítások megváltoztatására használják egyszerű szöveges parancsok listáján keresztül. Ezek a parancsok általában soronként egyet tartalmaznak, és a játék jellemzőinek testreszabásáért felelősek.

A lejátszóknak és a szerveradminisztrátoroknak néhány lehetőségük van a `.cfg` fájlban megadott változtatások alkalmazására:

1. **Kézi végrehajtás**: A felhasználók manuálisan hajthatnak végre parancsokat a CFG fájlon belül. Ez azt jelenti, hogy minden parancsot egyenként adnak meg a játék Developer Console-jában. Ez a módszer lehetővé teszi a pontos szabályozást, hogy mely beállításokat és mikor módosítsák.
    





2. **Automatikus végrehajtás**: A játékosok választhatják az automatikus végrehajtást is. Ez magában foglalja a `.cfg` fájl megfelelő játékkönyvtárba helyezését. Egyes `.cfg` fájlok, például az `autoexec.cfg`, automatikusan végrehajtásra kerülnek a játék indításakor. Ez biztosítja, hogy a megadott beállításokat a játék minden indításakor kézi bevitel nélkül alkalmazza.

## A Valve Source Engine

A Valve Source Engine, amelyet gyakran egyszerűen **Source Engine-nek** neveznek, egy rendkívül sokoldalú és széles körben használt játékmotor, amelyet a Valve Corporation fejlesztett ki. Számos népszerű videojáték alapja volt, és számos sikeres játékot hajtott végre. Íme néhány kulcsfontosságú pont a Valve Source Engine-ről:

1. **Előzmények**: A Source Engine-t először a Valve "Counter-Strike 1.6" játékának 2004-es kiadásával mutatták be. Azóta számos frissítésen és átdolgozáson esett át, a legújabb verzió Source 2.0 néven ismert.
    





2. **Nevezetes játékok**: A Source Engine-t számos kritikailag elismert játékban használták, beleértve, de nem kizárólagosan:
    





- "Half-Life 2" és epizódjai
- "Portál" és "Portál 2"
- "Team Fortress 2"
- "Left 4 Dead" és "Left 4 Dead 2"
- "Counter-Strike: Source" és "Counter-Strike: Global Offensive"
- "DOTA 2"
3. **Jellemzők**:
    





- **Rugalmasság**: A Source Engine rugalmasságáról ismert, amely lehetővé teszi a fejlesztők számára, hogy játékműfajok széles skáláját hozzanak létre, az első személyű lövöldözős játékoktól a kirakós játékokig és így tovább.
- **Fizika**: Robusztus fizikai motort tartalmaz, amely valósághű objektum-kölcsönhatásokat és környezeti hatásokat tesz lehetővé.
- **Modding támogatás**: A motor erős modding-támogatással rendelkezik, ami számos felhasználó által generált tartalom és játékmód létrehozásához vezetett.
- **Többjátékos képességek**: A Source Engine-t egyjátékos és többjátékos játékok fejlesztésére is használták, és kiterjedt hálózati lehetőségeket kínál az online játékhoz.
    





4. **Grafika**: Az évek során a Source Engine grafikus frissítéseket kapott, hogy lépést tudjon tartani a fejlődő hardverképességekkel. Támogatja a fejlett renderelési technikákat, például a HDR (High Dynamic Range) megvilágítást és a dinamikus árnyékokat.

## CFG fájl - Mivel nyitható meg?

Lehetősége van a `.cfg` fájl megnyitására és módosítására olyan szövegszerkesztőkkel, mint a Microsoft Visual Studio Code vagy bármely más választott szövegszerkesztő. Ezek a szövegszerkesztők felhasználóbarát felületet biztosítanak a `.cfg` fájlon belüli egyszerű szöveges parancsok megtekintéséhez és szerkesztéséhez, lehetővé téve a beállítások szükség szerinti testreszabását.

A CFG fájlokat megnyitó vagy hivatkozó programok közé tartozik

- Microsoft Visual Studio kód
- Jegyzettömb
- TextEdit
- Bármilyen szövegszerkesztő

## Egyéb CFG fájlok

Íme más fájltípusok, amelyek **.cfg** kiterjesztést használnak.

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
* [Forrás (játékmotor)](https://en.wikipedia.org/wiki/Source_(game_engine))

