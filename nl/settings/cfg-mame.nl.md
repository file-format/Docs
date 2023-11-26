{
"datum": "27-09-2023",
  "keywords": [
"cfg",
"cfg-bestand",
"cfg mame-configuratiebestand",
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
"title":"CFG-bestandsindeling - MAME-configuratiebestand",
  "description":"Leer meer over het CFG MAME-configuratiebestandsformaat en API's waarmee CFG-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"parent":"instellingen"
}
},
"laatste mod": "27-09-2023"
}

## Wat is een CFG-bestand?

CFG-bestand is een XML-toetsenbordconfiguratiebestand dat wordt gebruikt door MAME arcade-videogame-emulators. Het is een cruciaal onderdeel voor het aanpassen van toetsenbordbedieningen en sneltoetsen aan de voorkeuren van de speler. Deze bestanden slaan toewijzingen en instellingen op die bepalen hoe het toetsenbord samenwerkt met de emulator tijdens het spelen van een game. Door dit bestand te bewerken, kunnen gebruikers hun game-ervaring aanpassen door specifieke toetsenbordtoetsen toe te wijzen aan acties binnen het spel, zoals het inwerpen van munten, starten, bewegen en diverse andere functies.

## MAME-configuratiebestand

MAME, wat staat voor **Multiple Arcade Machine Emulator**, is een softwaretoepassing waarmee u arcadespellen op uw computer kunt emuleren en spelen. MAME gebruikt configuratiebestanden om het gedrag en de instellingen aan te passen. Deze configuratiebestanden bevinden zich doorgaans in de map `cfg` in uw MAME-map.

Hier volgen de belangrijkste configuratiebestanden die u kunt tegenkomen bij het instellen en configureren van MAME:

1. **mame.ini:** Dit is het hoofdconfiguratiebestand voor MAME. Het bevat algemene instellingen die van toepassing zijn op alle games. Je kunt dit bestand vinden in de hoofdmap van je MAME-installatie.

1. **default.cfg:** In dit bestand worden standaardinstellingen opgeslagen voor alle games die geen eigen configuratiebestanden hebben. Het wordt gebruikt als fallback voor gamespecifieke instellingen.

1. **game-specific.cfg:** Deze bestanden worden gebruikt om instellingen voor individuele games op te slaan. Ze zijn meestal vernoemd naar het ROM-bestand van het spel waarmee ze overeenkomen. Als je bijvoorbeeld een spel hebt met de naam "pacman.zip", zou het configuratiebestand daarvoor "pacman.cfg" zijn.

Hier zijn enkele veelvoorkomende instellingen die u mogelijk in het MAME-configuratiebestand aantreft.

1. **rompath:** Specificeert de map waar uw arcadespel-ROM's zich bevinden.

1. **cfg_directory:** Specificeert de map waar spelspecifieke configuratiebestanden worden opgeslagen.

1. **nvram_directory:** Specificeert de map waarin niet-vluchtige RAM-bestanden (NVRAM) worden opgeslagen. NVRAM slaat hoge scores en andere spelspecifieke gegevens op.

1. **artwork_directory:** Specificeert de map waarin illustratiebestanden (zoals randen, selectiekaders en flyers) worden opgeslagen.

1. **samplepath:** Specificeert de map waar de voorbeeldgeluidsbestanden zich bevinden.

1. **cheatpath:** Specificeert de map waar cheatbestanden zich bevinden.

U kunt ook diverse andere instellingen configureren, zoals video- en audio-opties, bedieningselementen en invoerapparaten. Om deze instellingen te wijzigen, kunt u het configuratiebestand in de teksteditor openen en de nodige wijzigingen aanbrengen.

## MAME

MAME, wat staat voor **"Multiple Arcade Machine Emulator,"** is een softwareapplicatie die is ontworpen om de hardware van vintage arcade-machines en arcade-gameconsoles te emuleren en te repliceren. Hiermee kunnen gebruikers een enorme bibliotheek met klassieke arcadespellen spelen op moderne computers en andere compatibele apparaten. MAME is een open-sourceproject en is een go-to-emulator geworden voor het behouden en genieten van de rijke geschiedenis van arcade-gaming.

1. **Emulatie:** Het primaire doel van MAME is het nauwkeurig emuleren van de hardware van speelautomaten, inclusief hun centrale verwerkingseenheden (CPU's), geluidschips, grafische chips en invoerapparaten. Dit nauwkeurigheidsniveau zorgt ervoor dat games zich zo dicht mogelijk bij de originele arcade-ervaring gedragen.

1. **Compatibiliteit:** MAME ondersteunt een breed scala aan arcadespel-ROM's, waardoor het een van de meest uitgebreide arcade-emulators is die er zijn. Het kan games van verschillende arcadeplatforms uitvoeren, waaronder klassieke games uit de jaren '70, '80, '90 en zelfs enkele recentere arcadetitels.

1. **Behoud:** Een van de belangrijkste missies van MAME is het bewaren van de geschiedenis van arcade-gaming. Door arcade-hardware nauwkeurig te emuleren, helpt MAME het verlies van klassieke games te voorkomen en ervoor te zorgen dat toekomstige generaties deze kunnen ervaren zoals ze oorspronkelijk bedoeld waren.

1. **Front-ends:** Veel gebruikers gebruiken front-end-applicaties die een grafische interface bieden om games via MAME te beheren en te starten. Deze front-ends maken het gemakkelijker om door de uitgebreide gamebibliotheek van MAME te navigeren.

## Hoe open je een CFG-bestand?

Programma's die CFG-bestanden openen of ernaar verwijzen

- MAME (gratis) (Windows)
- ExtraMAME (proefversie)
-MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)

