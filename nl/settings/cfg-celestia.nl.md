{
"datum": "27-09-2023",
  "keywords": [
"cfg",
"cfg-bestand",
"cfg celestia-configuratiebestand",
"wat is een cfg-bestand",
"hoe cfg-bestand te openen",
"bestand",
"cfg-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CFG-bestandsindeling - Celestia-configuratiebestand",
  "description":"Leer meer over het CFG Celestia-configuratiebestandsformaat en API's waarmee CFG-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent" : "settings"
}
},
"laatste mod": "27-09-2023"
}

## Wat is een CFG-bestand?

Een Celestia-configuratiebestand is een tekstbestand dat wordt gebruikt door Celestia, een 3D-universumsimulatieprogramma. Deze bestanden zijn essentieel voor het aanpassen van hoe Celestia zich gedraagt, welke hemellichamen worden weergegeven en hoe het programma verschijnt. Het bewerken van deze bestanden vereist echter zorgvuldige aandacht, omdat onjuiste wijzigingen het laadproces van Celestia kunnen verstoren, waardoor het niet correct kan worden uitgevoerd.

## Celestia

Celestia is gratis, open-source 3D-astronomiesimulatiesoftware waarmee gebruikers het universum op zeer realistische en interactieve wijze kunnen verkennen en visualiseren. Het is ontwikkeld door Chris Laurel en werd voor het eerst uitgebracht begin jaren 2000. Celestia is beschikbaar voor Windows-, macOS- en Linux-besturingssystemen.

De belangrijkste kenmerken en aspecten van Celestia zijn onder meer:

- **Realistische 3D-visualisatie:** Celestia biedt een gedetailleerde en nauwkeurige weergave van ons zonnestelsel, evenals van sterren, sterrenstelsels en andere hemellichamen. Het maakt gebruik van hoogwaardige 3D-modellen en texturen om een visueel meeslepende ervaring te creëren.

- **Uitgebreide hemelse database:** De software wordt geleverd met een enorme ingebouwde database van bekende hemellichamen, waaronder sterren, planeten, manen, asteroïden, kometen en ruimtevaartuigen. Gebruikers kunnen deze objecten gemakkelijk lokaliseren en verkennen.

- **Wetenschappelijke nauwkeurigheid:** Hoewel Celestia een visualisatietool is, heeft het tot doel hemellichamen en verschijnselen zo nauwkeurig mogelijk weer te geven, op basis van beschikbare wetenschappelijke gegevens.

## Bestandsformaten gebruikt door Celestia

Celestia gebruikt verschillende bestandsformaten voor verschillende aspecten van zijn 3D-astronomiesimulatie. Hier zijn enkele van de belangrijkste bestandsformaten die door Celestia worden gebruikt:

1. **Configuratiebestanden (.cel)**
- *Beschrijving*: platte tekstbestanden waarmee gebruikers het gedrag, het uiterlijk en de inhoud van Celestia kunnen aanpassen.
- *Doel*: instellingen aanpassen, locaties definiëren en hemellichamen specificeren.

2. **3D-modellen en meshes**
- *Formaten*: [.3ds](/nl/3d/3ds/), [.obj](/nl/3d/obj/), [.dae](/nl/3d/dae/), .ac
- *Beschrijving*: Ondersteunde 3D-modelbestandsindelingen die worden gebruikt voor het weergeven van hemellichamen en ruimtevaartuigen.
- *Doel*: 3D-objecten weergeven binnen Celestia.

3. **Textuurbestanden**
- *Formaten*: [.jpg](/nl/image/jpeg/), [.png](/nl/image/png/), [.dds](/nl/image/dds/)
- *Beschrijving*: deze bestanden bieden oppervlaktestructuren voor hemellichamen.
- *Doel*: texturen in kaart brengen op 3D-modellen voor een realistisch uiterlijk.

4. **Stercatalogi en gegevensbestanden**
- *Formaten*: aangepaste formaten, [.csv](/nl/spreadsheet/csv/), [.tsv](/nl/spreadsheet/tsv/)
- *Beschrijving*: gegevensbestanden die worden gebruikt om sterren en andere hemellichamen weer te geven, waardoor een nauwkeurige simulatie wordt gegarandeerd.
- *Doel*: Nauwkeurige weergave van hemellichamen.

5. **Textuurkubuskaarten**
- *Beschrijving*: Kubuskaarten worden gebruikt om het uiterlijk van verre hemellichamen zoals sterrenstelsels te simuleren.
- *Doel*: Objecten op afstand weergeven met realistische texturen.

6. **Scriptbestanden**
- *Beschrijving*: deze bestanden bevatten aangepaste scripts geschreven in de scripttaal van Celestia.
- *Doel*: gebruikers in staat stellen dynamische gebeurtenissen en animaties te creëren binnen het universum van Celestia.

## Celestia-configuratiebestand

Hier is een basisoverzicht van wat u kunt doen met het Celestia-configuratiebestand:

1. **Uw locatie instellen**: u kunt uw locatie op aarde opgeven met behulp van parameters voor de breedtegraad, lengtegraad en hoogte. Hierdoor kan Celestia de nachtelijke hemel nauwkeurig weergeven vanuit uw positie.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Uw weergaveopties aanpassen:** U kunt verschillende weergaveopties aanpassen, zoals gezichtsveld, tijdinstellingen en weergavevoorkeuren.

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

3. **Hemellichamen laden:** U kunt hemellichamen zoals sterren, planeten, asteroïden, ruimtevaartuigen en meer aan uw simulatie toevoegen. Elk object wordt gedefinieerd in het configuratiebestand met zijn eigenschappen.

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

4. **Ruimteschepen definiëren:** U kunt uw eigen fictieve ruimtevaartuigen maken of echte ruimtevaartuigen gebruiken door hun parameters zoals positie, oriëntatie en 3D-modellen op te geven.

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

5. **Scripts maken:** U kunt scripts schrijven in de aangepaste scripttaal van Celestia om dynamische gebeurtenissen en animaties te maken.

## Hoe open je een CFG-bestand?

Programma's die CFG-bestanden openen of ernaar verwijzen

- Celestia (gratis) voor (Windows, Mac, Linux)

## Andere CFG-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cfg** gebruiken.

**Instellingen**
- [CFG - Celestia-configuratiebestand] (/nl/settings/cfg-celestia/)
- [CFG - Citrix-serververbindingsbestand](/nl/settings/cfg-citrix/)
- [CFG - MAME-configuratiebestand] (/nl/settings/cfg-mame/)
- [CFG - LightWave-configuratiebestand] (/nl/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language-bestand] (/nl/game/cfg-wesnoth/)
- [CFG - MUGEN-configuratiebestand] (/nl/game/cfg-mugen/)
- [CFG - Bronengineconfiguratiebestand](/nl/game/cfg-sourceengine/)

**Systeem en Diversen**
- [CFG - CFG-bestand](/nl/system/cfg/)
- [CFG - Cal3D-modelconfiguratiebestand] (/nl/misc/cfg-cal3d/)

## Referenties
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

