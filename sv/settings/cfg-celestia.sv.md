{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-fil",
"cfg celestia konfigurationsfil",
"vad är en cfg-fil",
"hur man öppnar cfg-fil",
"fil",
"cfg filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG-filformat - Celestia-konfigurationsfil",
  "description":"Läs mer om CFG Celestia-konfigurationsfilformat och API:er som kan skapa och öppna CFG-filer.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Vad är CFG fil?

En Celestia-konfigurationsfil är en vanlig textfil som används av Celestia, simuleringsprogram för 3D-universum. Dessa filer är viktiga för att anpassa hur Celestia beter sig, vilka himmelska objekt som visas och hur programmet ser ut. Men att redigera dessa filer kräver noggrann uppmärksamhet eftersom felaktiga ändringar kan störa Celestias laddningsprocess och förhindra att den körs korrekt.

## Celestia

Celestia är gratis, öppen källkod för 3D astronomisimuleringsprogram som låter användare utforska och visualisera universum på ett mycket realistiskt och interaktivt sätt. Den utvecklades av Chris Laurel och släpptes först i början av 2000-talet. Celestia är tillgängligt för Windows, macOS och Linux operativsystem.

Nyckelfunktioner och aspekter av Celestia inkluderar:

- **Realistisk 3D-visualisering:** Celestia ger en detaljerad och korrekt representation av vårt solsystem, såväl som stjärnor, galaxer och andra himmelska objekt. Den använder högkvalitativa 3D-modeller och texturer för att skapa en visuellt uppslukande upplevelse.

- **Omfattande himmeldatabas:** Programvaran kommer med en stor inbyggd databas med kända himmelska objekt, inklusive stjärnor, planeter, månar, asteroider, kometer och rymdfarkoster. Användare kan enkelt hitta och utforska dessa objekt.

- **Vetenskaplig noggrannhet:** Celestia är ett visualiseringsverktyg, men det syftar till att representera himmelska objekt och fenomen så exakt som möjligt, baserat på tillgängliga vetenskapliga data.

## Filformat som används av Celestia

Celestia använder olika filformat för olika aspekter av sin 3D-astronomisimulering. Här är några av de viktigaste filformaten som används av Celestia:

1. **Konfigurationsfiler (.cel)**
- *Beskrivning*: Enkla textfiler som tillåter användare att anpassa Celestias beteende, utseende och innehåll.
- *Syfte*: Anpassa inställningar, definiera platser och ange himmelska objekt.

2. **3D-modeller och maskor**
- *Format*: [.3ds](/sv/3d/3ds/), [.obj](/sv/3d/obj/), [.dae](/sv/3d/dae/), .ac
- *Beskrivning*: Stödda 3D-modellfilformat som används för att rendera himlakroppar och rymdskepp.
- *Syfte*: Visa 3D-objekt i Celestia.

3. **Texturfiler**
- *Format*: [.jpg](/sv/image/jpeg/), [.png](/sv/image/png/), [.dds](/sv/image/dds/)
- *Beskrivning*: Dessa filer ger ytstrukturer för himlakroppar.
- *Syfte*: Kartlägga texturer på 3D-modeller för ett realistiskt utseende.

4. **Stjärnkataloger och datafiler**
- *Format*: Anpassade format, [.csv](/sv/spreadsheet/csv/), [.tsv](/sv/spreadsheet/tsv/)
- *Beskrivning*: Datafiler som används för att representera stjärnor och andra himmelska objekt, vilket säkerställer korrekt simulering.
- *Syfte*: Exakt representation av himmelska föremål.

5. **Kartor för texturkub**
- *Beskrivning*: Kubkartor används för att simulera uppkomsten av avlägsna himmelska objekt som galaxer.
- *Syfte*: Återge avlägsna objekt med realistiska texturer.

6. **Skriptfiler**
- *Beskrivning*: Dessa filer innehåller anpassade skript skrivna på Celestias skriptspråk.
- *Syfte*: Gör det möjligt för användare att skapa dynamiska händelser och animationer inom Celestias universum.

## Celestia konfigurationsfil

Här är en grundläggande översikt över vad du kan göra med Celestia-konfigurationsfilen:

1. **Ställa in din plats**: Du kan ange din plats på jorden med hjälp av parametrar för latitud, longitud och höjd. Detta tillåter Celestia att exakt visa natthimlen från din position.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Anpassa dina visningsalternativ:** Du kan justera olika visningsalternativ som synfält, tidsinställningar och renderingsinställningar.

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

3. **Ladda in himmelska objekt:** Du kan lägga till himmelska objekt som stjärnor, planeter, asteroider, rymdfarkoster och mer till din simulering. Varje objekt definieras i konfigurationsfilen med dess egenskaper.

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

4. **Definiera rymdskepp:** Du kan skapa dina egna fiktiva rymdskepp eller använda riktiga genom att ange deras parametrar som position, orientering och 3D-modeller.

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

5. **Skapa skript:** Du kan skriva skript i Celestias anpassade skriptspråk för att skapa dynamiska händelser och animationer.

## Hur öppnar man filen CFG?

Program som öppnar eller refererar till CFG-filer

- Celestia (gratis) för (Windows, Mac, Linux)

## Andra CFG-filer

Här är andra filtyper som använder filtillägget **.cfg**.

**Inställningar**
- [CFG - Celestia-konfigurationsfil](/sv/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/sv/settings/cfg-citrix/)
- [CFG - MAME-konfigurationsfil](/sv/settings/cfg-mame/)
- [CFG - LightWave-konfigurationsfil](/sv/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language File](/sv/game/cfg-wesnoth/)
- [CFG - MUGEN-konfigurationsfil](/sv/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/sv/game/cfg-sourceengine/)

**System & Övrigt**
- [CFG - CFG-fil](/sv/system/cfg/)
- [CFG - Cal3D Model Configuration File](/sv/misc/cfg-cal3d/)

## Referenser
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

