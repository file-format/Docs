{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg celestia konfigurationsfil",
"hvad er en cfg-fil",
"hvordan man åbner cfg fil",
"fil",
"cfg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-filformat - Celestia-konfigurationsfil",
  "description": "Lær om CFG Celestia Configuration File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia-da",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er CFG fil?

En Celestia-konfigurationsfil er en almindelig tekstfil, der bruges af Celestia, 3D-univers-simuleringsprogram. Disse filer er afgørende for at tilpasse, hvordan Celestia opfører sig, hvilke himmelobjekter der vises, og hvordan programmet vises. Redigering af disse filer kræver dog omhyggelig opmærksomhed, fordi ukorrekte ændringer kan forstyrre Celestias indlæsningsproces og forhindre den i at køre korrekt.

## Celestia

Celestia er gratis, open source 3D astronomi-simuleringssoftware, der giver brugerne mulighed for at udforske og visualisere universet på yderst realistisk og interaktiv måde. Det blev udviklet af Chris Laurel og blev først udgivet i begyndelsen af 2000'erne. Celestia er tilgængelig til Windows, macOS og Linux-operativsystemer.

Nøglefunktioner og aspekter af Celestia inkluderer:

- **Realistisk 3D-visualisering:** Celestia giver detaljeret og nøjagtig repræsentation af vores solsystem, såvel som stjerner, galakser og andre himmellegemer. Den bruger 3D-modeller og teksturer af høj kvalitet til at skabe en visuelt fordybende oplevelse.

- **Omfattende himmeldatabase:** Softwaren leveres med en stor indbygget database med kendte himmelobjekter, inklusive stjerner, planeter, måner, asteroider, kometer og rumfartøjer. Brugere kan nemt finde og udforske disse objekter.

- **Videnskabelig nøjagtighed:** Selvom Celestia er visualiseringsværktøj, sigter det mod at repræsentere himmellegemer og fænomener så nøjagtigt som muligt, baseret på tilgængelige videnskabelige data.

## Filformater brugt af Celestia

Celestia bruger forskellige filformater til forskellige aspekter af sin 3D astronomi-simulering. Her er nogle af de vigtigste filformater, der anvendes af Celestia:

1. **Konfigurationsfiler (.cel)**
- *Beskrivelse*: Almindelige tekstfiler, der tillader brugere at tilpasse Celestias adfærd, udseende og indhold.
- *Formål*: Tilpasning af indstillinger, definering af placeringer og angivelse af himmellegemer.

2. **3D-modeller og masker**
- *Formater*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
- *Beskrivelse*: Understøttede 3D-modelfilformater, der bruges til at gengive himmellegemer og rumfartøjer.
- *Formål*: Visning af 3D-objekter i Celestia.

3. **Teksturfiler**
- *Formater*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
- *Beskrivelse*: Disse filer giver overfladeteksturer til himmellegemer.
- *Formål*: Kortlægning af teksturer på 3D-modeller for et realistisk udseende.

4. **Stjernekataloger og datafiler**
- *Formater*: Tilpassede formater, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
- *Beskrivelse*: Datafiler, der bruges til at repræsentere stjerner og andre himmellegemer, hvilket sikrer nøjagtig simulering.
- *Formål*: Nøjagtig repræsentation af himmellegemer.

5. **Texture Cube Maps**
- *Beskrivelse*: Kubekort bruges til at simulere udseendet af fjerne himmellegemer som galakser.
- *Formål*: Gengivelse af fjerne objekter med realistiske teksturer.

6. **Script-filer**
- *Beskrivelse*: Disse filer indeholder brugerdefinerede scripts skrevet i Celestias scriptsprog.
- *Formål*: Gør det muligt for brugere at skabe dynamiske begivenheder og animationer i Celestias univers.

## Celestia konfigurationsfil

Her er en grundlæggende oversigt over, hvad du kan gøre med Celestia-konfigurationsfilen:

1. **Indstilling af din placering**: Du kan angive din placering på Jorden ved hjælp af bredde-, længde- og højdeparametre. Dette giver Celestia mulighed for nøjagtigt at vise nattehimlen fra din position.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Tilpasning af dine visningsindstillinger:** Du kan justere forskellige visningsindstillinger såsom synsfelt, tidsindstillinger og gengivelsespræferencer.

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

3. **Indlæsning af himmelobjekter:** Du kan tilføje himmelobjekter såsom stjerner, planeter, asteroider, rumfartøjer og mere til din simulering. Hvert objekt er defineret i konfigurationsfilen med dets egenskaber.

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

4. **Definition af rumskibe:** Du kan skabe dit eget fiktive rumfartøj eller bruge rigtige ved at angive deres parametre som position, orientering og 3D-modeller.

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

5. **Oprettelse af scripts:** Du kan skrive scripts i Celestias brugerdefinerede scriptsprog for at skabe dynamiske begivenheder og animationer.

## Hvordan åbner jeg filen CFG?

Programmer, der åbner eller refererer til CFG filer

- Celestia (gratis) til (Windows, Mac, Linux)

## Andre CFG-filer

Her er andre filtyper, der bruger filtypen **.cfg**.

**Indstillinger**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spil**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System og diverse**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Referencer
* [Celestia](https://en.wikipedia.org/wiki/Celestia)


