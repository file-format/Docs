{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-fil",
"cfg mame konfigurationsfil",
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
"title": "CFG-filformat - MAME-konfigurationsfil",
  "description":"Läs mer om CFG MAME-konfigurationsfilformat och API:er som kan skapa och öppna CFG-filer.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "2023-09-27"
}

## Vad är CFG fil?

CFG-fil är en XML-tangentbordskonfigurationsfil som används av MAME arkadspelsemulatorer. Det är en avgörande komponent för att anpassa tangentbordskontroller och snabbtangenter för att passa spelarens preferenser. Dessa filer lagrar mappningar och inställningar som bestämmer hur tangentbordet interagerar med emulatorn när du spelar spel. Genom att redigera den här filen kan användare skräddarsy sin spelupplevelse genom att tilldela specifika tangentbordstangenter till åtgärder inom spelet, såsom myntinsättning, start, rörelse och olika andra funktioner.

## MAME-konfigurationsfil

MAME, som står för **Multiple Arcade Machine Emulator**, är ett program som låter dig emulera och spela arkadspel på din dator. MAME använder konfigurationsfiler för att anpassa dess beteende och inställningar. Dessa konfigurationsfiler finns vanligtvis i mappen `cfg` i din MAME-katalog.

Här är de viktigaste konfigurationsfilerna du kan stöta på när du konfigurerar och konfigurerar MAME:

1. **mame.ini:** Detta är huvudkonfigurationsfilen för MAME. Den innehåller globala inställningar som gäller för alla spel. Du kan hitta den här filen i rotkatalogen för din MAME-installation.

1. **default.cfg:** Den här filen lagrar standardinställningar för alla spel som inte har sina egna konfigurationsfiler. Den används som reserv för spelspecifika inställningar.

1. **game-specific.cfg:** Dessa filer används för att lagra inställningar för enskilda spel. De är vanligtvis uppkallade efter ROM-fil för spel de motsvarar. Om du till exempel har ett spel som heter "pacman.zip", skulle konfigurationsfilen för det vara "pacman.cfg."

Här är några vanliga inställningar du kan hitta i MAME-konfigurationsfilen.

1. **rompath:** Anger katalogen där dina arkadspels-ROM finns.

1. **cfg_directory:** Anger katalog där spelspecifika konfigurationsfiler lagras.

1. **nvram_directory:** Anger katalog där icke-flyktiga RAM-filer (NVRAM) lagras. NVRAM lagrar höga poäng och annan spelspecifik data.

1. **artwork_directory:** Anger katalog där teckningsfiler (som ramar, markeringsramar och flygblad) lagras.

1. **samplepath:** Anger katalog där exempelljudfiler finns.

1. **cheatpath:** Specificerar katalogen där fuskfilerna finns.

Du kan också konfigurera olika andra inställningar som video- och ljudalternativ, kontroller och inmatningsenheter. För att ändra dessa inställningar kan du öppna konfigurationsfilen i textredigeraren och göra nödvändiga ändringar.

## MAME

MAME, som står för **"Multiple Arcade Machine Emulator,"** är ett program som är utformat för att efterlikna och replikera hårdvara från vintage arkadmaskiner och arkadspelkonsoler. Det tillåter användare att spela ett stort bibliotek av klassiska arkadspel på moderna datorer och andra kompatibla enheter. MAME är ett projekt med öppen källkod och har blivit en go-to-emulator för att bevara och njuta av en rik historia av arkadspel.

1. **Emulering:** MAMEs primära syfte är att noggrant emulera hårdvara i arkadmaskiner, inklusive deras centrala processorenheter (CPU), ljudchips, grafikkretsar och inmatningsenheter. Denna nivå av noggrannhet säkerställer att spelen beter sig så nära den ursprungliga arkadupplevelsen som möjligt.

1. **Kompatibilitet:** MAME stöder ett brett utbud av arkadspel-ROM, vilket gör det till en av de mest omfattande arkademulatorerna som finns tillgängliga. Den kan köra spel från olika arkadplattformar inklusive klassiska spel från 70-, 80-, 90-talet och till och med några nyare arkadtitlar.

1. **Bevarande:** Ett av MAMEs främsta uppdrag är att bevara arkadspelets historia. Genom att noggrant emulera arkadhårdvara hjälper MAME till att förhindra förlust av klassiska spel och ser till att framtida generationer kan uppleva dem som de ursprungligen var tänkta.

1. **Front-ends:** Många användare använder front-end-applikationer som tillhandahåller grafiskt gränssnitt för att hantera och starta spel via MAME. Dessa gränssnitt gör det lättare att navigera i MAMEs omfattande spelbibliotek.

## Hur öppnar man filen CFG?

Program som öppnar eller refererar till CFG-filer

- MAME (gratis) (Windows)
- ExtraMAME (provversion)
- MacMAME (MAC)

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
* [MAME](https://en.wikipedia.org/wiki/MAME)

