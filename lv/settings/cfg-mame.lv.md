{
  "date": "2023-09-27",
  "keywords": [
"sk",
"cfg failu",
"cfg mame konfigurācijas fails",
"kas ir cfg fails",
"kā atvērt cfg failu",
"failu",
"cfg faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG faila formāts — MAME konfigurācijas fails",
  "description": "Uzziniet par CFG MAME konfigurācijas faila formātu un API, kas var izveidot un atvērt CFG failus.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Kas ir CFG fails?

CFG fails ir XML tastatūras konfigurācijas fails, ko izmanto MAME arkādes videospēļu emulatori. Tas ir būtisks komponents, lai pielāgotu tastatūras vadīklas un karstos taustiņus, lai tie atbilstu spēlētāja vēlmēm. Šajos failos tiek saglabāti kartējumi un iestatījumi, kas nosaka, kā tastatūra mijiedarbojas ar emulatoru spēles laikā. Rediģējot šo failu, lietotāji var pielāgot savu spēļu pieredzi, piešķirot konkrētus tastatūras taustiņus darbībām spēlē, piemēram, monētu ievietošanai, sākumam, kustībai un dažādām citām funkcijām.

## MAME konfigurācijas fails

MAME, kas apzīmē **Multiple Arcade Machine Emulator**, ir lietojumprogramma, kas ļauj atdarināt un spēlēt arkādes spēles datorā. MAME izmanto konfigurācijas failus, lai pielāgotu savu darbību un iestatījumus. Šie konfigurācijas faili parasti atrodas mapē cfg jūsu MAME direktorijā.

Šeit ir norādīti galvenie konfigurācijas faili, ar kuriem var saskarties, iestatot un konfigurējot MAME:

1. **mame.ini:** Šis ir MAME galvenais konfigurācijas fails. Tajā ir globāli iestatījumi, kas attiecas uz visām spēlēm. Šo failu varat atrast MAME instalācijas saknes direktorijā.

1. **default.cfg:** šajā failā tiek saglabāti noklusējuma iestatījumi visām spēlēm, kurām nav savu konfigurācijas failu. Tas tiek izmantots kā atkāpšanās spēlei specifiskiem iestatījumiem.

1. **game-specific.cfg:** šie faili tiek izmantoti atsevišķu spēļu iestatījumu saglabāšanai. Tie parasti tiek nosaukti pēc ROM faila spēlei, kurai tie atbilst. Piemēram, ja jums ir spēle ar nosaukumu pacman.zip, tās konfigurācijas fails būtu pacman.cfg.

Šeit ir daži izplatīti iestatījumi, kurus varat atrast MAME konfigurācijas failā.

1. **rompath:** norāda direktoriju, kurā atrodas jūsu arkādes spēļu ROM.

1. **cfg_directory:** norāda direktoriju, kurā tiek glabāti spēlei specifiski konfigurācijas faili.

1. **nvram_directory:** norāda direktoriju, kurā tiek glabāti nepastāvīgie RAM (NVRAM) faili. NVRAM saglabā labākos rezultātus un citus ar spēli saistītus datus.

1. **artwork_directory:** norāda direktoriju, kurā tiek glabāti mākslas darbu faili (piemēram, rāmji, telts un skrejlapas).

1. **samplepath:** norāda direktoriju, kurā atrodas skaņas failu paraugi.

1. **cheatpath:** norāda direktoriju, kurā atrodas apkrāptu faili.

Varat arī konfigurēt dažādus citus iestatījumus, piemēram, video un audio opcijas, vadīklas un ievades ierīces. Lai mainītu šos iestatījumus, teksta redaktorā varat atvērt konfigurācijas failu un veikt nepieciešamās izmaiņas.

## MAME

MAME, kas apzīmē **Multiple Arcade Machine Emulator** ir programmatūras lietojumprogramma, kas izstrādāta, lai atdarinātu un replicētu seno spēļu automātu un arkādes spēļu konsoļu aparatūru. Tas ļauj lietotājiem spēlēt plašu klasisko arkādes spēļu bibliotēku mūsdienu datoros un citās saderīgās ierīcēs. MAME ir atvērtā pirmkoda projekts, un tas ir kļuvis par emulatoru bagātīgas arkādes spēļu vēstures saglabāšanai un baudīšanai.

1. **Emulācija:** MAME galvenais mērķis ir precīzi atdarināt arkādes iekārtu aparatūru, tostarp to centrālos procesorus (CPU), skaņas mikroshēmas, grafikas mikroshēmas un ievades ierīces. Šis precizitātes līmenis nodrošina, ka spēles darbojas pēc iespējas tuvāk oriģinālajai arkādes pieredzei.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Saglabāšana:** viena no MAME galvenajām misijām ir saglabāt arkādes spēļu vēsturi. Precīzi emulējot arkādes aparatūru, MAME palīdz novērst klasisko spēļu zaudēšanu un nodrošina, ka nākamās paaudzes var tās izjust tā, kā tās sākotnēji bija paredzētas.

1. **Frond Ends:** daudzi lietotāji izmanto priekšgala lietojumprogrammas, kas nodrošina grafisku saskarni, lai pārvaldītu un palaistu spēles, izmantojot MAME. Šīs priekšējās daļas atvieglo navigāciju MAME plašajā spēļu bibliotēkā.

## Kā atvērt CFG failu?

Programmas, kas atver CFG failus vai atsaucas uz tiem

- MAME (bezmaksas) (Windows)
- ExtraMAME (izmēģinājuma versija)
- MacMAME (MAC)

## Citi CFG faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.cfg**.

**Iestatījumi**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spēle**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistēma un citi**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Atsauces
* [MAME](https://en.wikipedia.org/wiki/MAME)


