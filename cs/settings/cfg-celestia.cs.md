{
"datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg soubor",
"konfigurační soubor cfg celestia",
"co je soubor cfg",
"jak otevřít soubor cfg",
"soubor",
"přípona souboru cfg",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CFG – konfigurační soubor Celestia",
  "description":"Další informace o formátu konfiguračního souboru CFG Celestia a rozhraních API, která mohou vytvářet a otevírat soubory CFG.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "27.09.2023"
}

## Co je soubor CFG?

Konfigurační soubor Celestia je prostý textový soubor používaný programem Celestia, 3D vesmírným simulačním programem. Tyto soubory jsou životně důležité pro přizpůsobení toho, jak se Celestia chová, jaké nebeské objekty se zobrazují a jak program vypadá. Úprava těchto souborů však vyžaduje pečlivou pozornost, protože nesprávné změny mohou narušit proces načítání Celestie a zabránit jeho správnému fungování.

## Celestia

Celestia je bezplatný software pro simulaci 3D astronomie s otevřeným zdrojovým kódem, který uživatelům umožňuje prozkoumávat a vizualizovat vesmír vysoce realistickým a interaktivním způsobem. Byl vyvinut Chrisem Laurelem a poprvé byl vydán na počátku roku 2000. Celestia je k dispozici pro operační systémy Windows, MacOS a Linux.

Mezi klíčové vlastnosti a aspekty Celestia patří:

- **Realistická 3D vizualizace:** Celestia poskytuje podrobné a přesné znázornění naší sluneční soustavy, stejně jako hvězd, galaxií a dalších nebeských objektů. Využívá vysoce kvalitní 3D modely a textury k vytvoření vizuálně pohlcujícího zážitku.

- **Rozsáhlá nebeská databáze:** Software je dodáván s rozsáhlou vestavěnou databází známých nebeských objektů, včetně hvězd, planet, měsíců, asteroidů, komet a kosmických lodí. Uživatelé mohou tyto objekty snadno najít a prozkoumat.

- **Vědecká přesnost:** Zatímco Celestia je vizualizační nástroj, jejím cílem je co nejpřesněji reprezentovat nebeské objekty a jevy na základě dostupných vědeckých údajů.

## Formáty souborů používané Celestií

Celestia využívá různé formáty souborů pro různé aspekty své 3D astronomické simulace. Zde jsou některé z klíčových formátů souborů používaných Celestií:

1. **Konfigurační soubory (.cel)**
- *Popis*: Soubory ve formátu prostého textu, které uživatelům umožňují přizpůsobit chování, vzhled a obsah Celestie.
- *Účel*: Přizpůsobení nastavení, definování umístění a určení nebeských objektů.

2. **3D modely a sítě**
- *Formáty*: [.3ds](/cs/3d/3ds/), [.obj](/cs/3d/obj/), [.dae](/cs/3d/dae/), .ac
- *Popis*: Podporované formáty souborů 3D modelů používané pro vykreslování nebeských těles a kosmických lodí.
- *Účel*: Zobrazení 3D objektů v Celestii.

3. **Soubory textur**
- *Formáty*: [.jpg](/cs/image/jpeg/), [.png](/cs/image/png/), [.dds](/cs/image/dds/)
- *Popis*: Tyto soubory poskytují povrchové textury pro nebeská tělesa.
- *Účel*: Mapování textur na 3D modely pro realistický vzhled.

4. **Katalogy hvězd a datové soubory**
– *Formáty*: Vlastní formáty, [.csv](/cs/spreadsheet/csv/), [.tsv](/cs/spreadsheet/tsv/)
- *Popis*: Datové soubory používané k reprezentaci hvězd a jiných nebeských objektů, což zajišťuje přesnou simulaci.
- *Účel*: Přesná reprezentace nebeských objektů.

5. **Mapy texturních kostek**
- *Popis*: Krychlové mapy se používají k simulaci vzhledu vzdálených nebeských objektů, jako jsou galaxie.
- *Účel*: Vykreslování vzdálených objektů s realistickými texturami.

6. **Soubory skriptů**
- *Popis*: Tyto soubory obsahují vlastní skripty napsané ve skriptovacím jazyce Celestia.
- *Účel*: Umožnění uživatelům vytvářet dynamické události a animace ve vesmíru Celestie.

## Konfigurační soubor Celestia

Zde je základní přehled toho, co můžete dělat s konfiguračním souborem Celestia:

1. **Nastavení vaší polohy**: Svou polohu na Zemi můžete určit pomocí parametrů zeměpisné šířky, zeměpisné délky a nadmořské výšky. To umožňuje Celestii přesně zobrazit noční oblohu z vaší pozice.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Přizpůsobení možností zobrazení:** Můžete upravit různé možnosti zobrazení, jako je zorné pole, nastavení času a předvolby vykreslování.

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

3. **Načítání nebeských objektů:** Do své simulace můžete přidat nebeské objekty, jako jsou hvězdy, planety, asteroidy, kosmické lodě a další. Každý objekt je definován v konfiguračním souboru se svými vlastnostmi.

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

4. **Definování vesmírných lodí:** Můžete si vytvořit své vlastní fiktivní vesmírné lodě nebo použít ty skutečné zadáním jejich parametrů, jako je poloha, orientace a 3D modely.

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

5. **Vytváření skriptů:** Můžete psát skripty ve vlastním skriptovacím jazyce Celestia a vytvářet tak dynamické události a animace.

## Jak otevřít soubor CFG?

Programy, které otevírají nebo odkazují na soubory CFG

- Celestia (zdarma) pro (Windows, Mac, Linux)

## Jiné soubory CFG

Zde jsou další typy souborů, které používají příponu souboru **.cfg**.

**Nastavení**
- [CFG - Celestia Configuration File](/cs/settings/cfg-celestia/)
- [CFG - Soubor připojení serveru Citrix](/cs/settings/cfg-citrix/)
- [CFG - Konfigurační soubor MAME](/cs/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/cs/settings/cfg-lightwave/)

**Hra**
- [CFG - Wesnoth Markup Language File](/cs/game/cfg-wesnoth/)
- [CFG - Konfigurační soubor MUGEN](/cs/game/cfg-mugen/)
- [CFG - konfigurační soubor zdrojového enginu](/cs/game/cfg-sourceengine/)

**Systém a různé**
- [CFG - Soubor CFG](/cs/system/cfg/)
– [CFG – konfigurační soubor modelu Cal3D](/cs/misc/cfg-cal3d/)

## Reference
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

