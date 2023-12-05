{
"dátum": "2023-09-27",
  "keywords": [
"cfg",
"cfg fájl",
"cfg celestia konfigurációs fájl",
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
"title": "CFG fájlformátum - Celestia konfigurációs fájl",
  "description":"További információ a CFG Celestia konfigurációs fájl formátumáról és az API-król, amelyek CFG fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Mi az a CFG fájl?

A Celestia konfigurációs fájl egy egyszerű szöveges fájl, amelyet a Celestia, a 3D univerzum szimulációs program használ. Ezek a fájlok létfontosságúak a Celestia viselkedésének, az égi objektumok megjelenítésének és a program megjelenésének testreszabásához. A fájlok szerkesztése azonban gondos odafigyelést igényel, mert a helytelen változtatások megzavarhatják a Celestia betöltési folyamatát, és megakadályozhatják a megfelelő működést.

## Celestia

A Celestia egy ingyenes, nyílt forráskódú 3D csillagászati szimulációs szoftver, amely lehetővé teszi a felhasználók számára, hogy rendkívül valósághű és interaktív módon fedezzék fel és vizualizálják az univerzumot. Chris Laurel fejlesztette ki, és először a 2000-es évek elején adták ki. A Celestia elérhető Windows, macOS és Linux operációs rendszerekhez.

A Celestia főbb jellemzői és jellemzői a következők:

- **Valósághű 3D-s megjelenítés:** A Celestia részletes és pontos ábrázolást nyújt Naprendszerünkről, valamint csillagokról, galaxisokról és más égi objektumokról. Kiváló minőségű 3D modelleket és textúrákat használ a vizuálisan magával ragadó élmény létrehozásához.

- **Kiterjedt égi adatbázis:** A szoftver hatalmas beépített adatbázissal rendelkezik ismert égi objektumokról, beleértve a csillagokat, bolygókat, holdakat, aszteroidákat, üstökösöket és űrhajókat. A felhasználók könnyen megtalálhatják és felfedezhetik ezeket az objektumokat.

- **Tudományos pontosság:** Míg a Celestia vizualizációs eszköz, célja az égi objektumok és jelenségek lehető legpontosabb ábrázolása a rendelkezésre álló tudományos adatok alapján.

## A Celestia által használt fájlformátumok

A Celestia különféle fájlformátumokat használ a 3D csillagászati szimuláció különböző aspektusaihoz. Íme néhány a Celestia által használt kulcsfontosságú fájlformátumok:

1. **Konfigurációs fájlok (.cel)**
- *Leírás*: Egyszerű szöveges fájlok, amelyek lehetővé teszik a felhasználók számára a Celestia viselkedésének, megjelenésének és tartalmának testreszabását.
- *Cél*: Beállítások testreszabása, helyek meghatározása és égi objektumok megadása.

2. **3D modellek és hálók**
- *Formátumok*: [.3ds](/hu/3d/3ds/), [.obj](/hu/3d/obj/), [.dae](/hu/3d/dae/), .ac
- *Leírás*: Támogatott 3D-s modellfájlformátumok, amelyek égitestek és űrhajók megjelenítéséhez használatosak.
- *Cél*: 3D objektumok megjelenítése a Celestián belül.

3. **Texture Files**
- *Formátumok*: [.jpg](/hu/image/jpeg/), [.png](/hu/image/png/), [.dds](/hu/image/dds/)
- *Leírás*: Ezek a fájlok felületi textúrákat biztosítanak az égitestek számára.
- *Cél*: Textúrák hozzárendelése 3D modellekre a valósághű megjelenés érdekében.

4. **Csillag katalógusok és adatfájlok**
- *Formátumok*: Egyéni formátumok, [.csv](/hu/spreadsheet/csv/), [.tsv](/hu/spreadsheet/tsv/)
- *Leírás*: A csillagok és más égi objektumok ábrázolására használt adatfájlok, amelyek pontos szimulációt biztosítanak.
- *Cél*: Az égi objektumok pontos ábrázolása.

5. **Texture Cube Maps**
- *Leírás*: A kockatérképek távoli égi objektumok, például galaxisok megjelenésének szimulálására szolgálnak.
- *Cél*: Távoli objektumok renderelése valósághű textúrákkal.

6. **Szkriptfájlok**
- *Leírás*: Ezek a fájlok a Celestia szkriptnyelvén írt egyedi szkripteket tartalmaznak.
- *Cél*: Lehetővé teszi a felhasználók számára, hogy dinamikus eseményeket és animációkat hozzanak létre a Celestia univerzumában.

## Celestia konfigurációs fájl

Íme az alapvető áttekintés arról, hogy mit tehet a Celestia konfigurációs fájljával:

1. **A hely beállítása**: Megadhatja tartózkodási helyét a Földön a szélességi, hosszúsági és magassági paraméterek segítségével. Ez lehetővé teszi a Celestia számára, hogy pontosan jelenítse meg az éjszakai égboltot az Ön pozíciójából.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **A megtekintési beállítások testreszabása:** Különféle megtekintési beállításokat állíthat be, például a látómezőt, az időbeállításokat és a megjelenítési beállításokat.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Égi objektumok betöltése:** A szimulációhoz hozzáadhat égi objektumokat, például csillagokat, bolygókat, aszteroidákat, űrhajókat és sok mást. Minden objektum konfigurációs fájlban van definiálva a tulajdonságaival együtt.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Űrhajók meghatározása:** Létrehozhat saját kitalált űrhajókat, vagy valódi űrhajókat is használhat paramétereik, például pozíció, tájolás és 3D modellek megadásával.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Szkriptek létrehozása:** A Celestia egyéni szkriptnyelvén írhat szkripteket dinamikus események és animációk létrehozásához.

## CFG fájl - Mivel nyitható meg?

Olyan programok, amelyek megnyitják a CFG fájlokat vagy hivatkoznak rájuk

- Celestia (ingyenes) (Windows, Mac, Linux)

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
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

