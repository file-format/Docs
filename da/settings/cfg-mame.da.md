{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg mame konfigurationsfil",
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
  "title": "CFG-filformat - MAME-konfigurationsfil",
  "description": "Lær om CFG MAME Configuration File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-da",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er CFG fil?

CFG-fil er en XML-tastaturkonfigurationsfil, der bruges af MAME arkade-videospilsemulatorer. Det er en afgørende komponent til at tilpasse tastaturkontroller og genvejstaster, så de passer til spillerens præferencer. Disse filer gemmer kortlægninger og indstillinger, der bestemmer, hvordan tastaturet interagerer med emulatoren, mens du spiller spil. Ved at redigere denne fil kan brugere skræddersy deres spiloplevelse ved at tildele specifikke tastaturtaster til handlinger i spillet, såsom møntindsættelse, start, bevægelse og forskellige andre funktioner.

## MAME-konfigurationsfil

MAME, som står for **Multiple Arcade Machine Emulator**, er et softwareprogram, der giver dig mulighed for at efterligne og spille arkadespil på din computer. MAME bruger konfigurationsfiler til at tilpasse dens adfærd og indstillinger. Disse konfigurationsfiler er typisk placeret i mappen `cfg` i din MAME-mappe.

Her er de vigtigste konfigurationsfiler, du kan støde på, når du opsætter og konfigurerer MAME:

1. **mame.ini:** Dette er hovedkonfigurationsfilen til MAME. Den indeholder globale indstillinger, der gælder for alle spil. Du kan finde denne fil i rodmappen på din MAME-installation.

1. **default.cfg:** Denne fil gemmer standardindstillinger for alle spil, der ikke har deres egne konfigurationsfiler. Det bruges som reserve til spilspecifikke indstillinger.

1. **game-specific.cfg:** Disse filer bruges til at gemme indstillinger for individuelle spil. De er typisk opkaldt efter ROM-fil for spil, de svarer til. For eksempel hvis du har et spil kaldet pacman.zip, ville konfigurationsfilen for det være pacman.cfg.

Her er nogle almindelige indstillinger, du kan finde i MAME-konfigurationsfilen.

1. **rompath:** Specificerer mappen, hvor dine arkadespil-ROM'er er placeret.

1. **cfg_directory:** Specificerer den mappe, hvor spilspecifikke konfigurationsfiler er gemt.

1. **nvram_directory:** Specificerer mappe, hvor ikke-flygtige RAM-filer (NVRAM) er gemt. NVRAM gemmer høje scores og andre spilspecifikke data.

1. **artwork_directory:** Specificerer det bibliotek, hvor illustrationsfiler (såsom rammer, markiser og flyers) er gemt.

1. **samplepath:** Specificerer det bibliotek, hvor prøvelydfiler er placeret.

1. **cheatpath:** Specificerer mappen, hvor snydefiler er placeret.

Du kan også konfigurere forskellige andre indstillinger såsom video- og lydindstillinger, kontroller og inputenheder. For at ændre disse indstillinger kan du åbne konfigurationsfilen i teksteditoren og foretage de nødvendige ændringer.

## MAME

MAME, som står for **Multiple Arcade Machine Emulator,** er softwareapplikation designet til at efterligne og replikere hardware fra vintage arkademaskiner og arkadespilkonsoller. Det giver brugerne mulighed for at spille et stort bibliotek af klassiske arkadespil på moderne computere og andre kompatible enheder. MAME er et open source-projekt og er blevet en go-to-emulator for at bevare og nyde en rig historie med arkadespil.

1. **Emulering:** MAME's primære formål er nøjagtigt at efterligne hardware i arkademaskiner, inklusive deres centrale behandlingsenheder (CPU'er), lydchips, grafikchips og inputenheder. Dette niveau af nøjagtighed sikrer, at spil opfører sig så tæt på den originale arkadeoplevelse som muligt.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Bevarelse:** En af MAMEs primære missioner er at bevare historien om arkadespil. Ved nøjagtigt at emulere arkadehardware hjælper MAME med at forhindre tab af klassiske spil og sikrer, at fremtidige generationer kan opleve dem, som de oprindeligt var tiltænkt.

1. **Front-ends:** Mange brugere bruger front-end-applikationer, der giver grafisk grænseflade til at administrere og starte spil gennem MAME. Disse front-ends gør det lettere at navigere i MAMEs omfattende bibliotek af spil.

## Hvordan åbner jeg filen CFG?

Programmer, der åbner eller refererer til CFG filer

- MAME (gratis) (Windows)
- ExtraMAME (prøveversion)
- MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)


