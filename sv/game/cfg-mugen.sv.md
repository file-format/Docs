{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-fil",
"cfg mugen konfigurationsfil",
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
"title": "CFG-filformat - MUGEN-konfigurationsfil",
  "description":"Läs mer om CFG MUGENs konfigurationsfilformat och API:er som kan skapa och öppna CFG-filer.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Vad är CFG fil?

CFG-fil i MUGEN-sammanhang hänvisar till "MUGEN-konfigurationsfil." **MUGEN** är anpassningsbar 2D-kampspelsmotor utvecklad av Elecbyte. Användare kan skapa sina egna karaktärer, scener och till och med ändra spelets beteende och regler genom att redigera olika konfigurationsfiler inklusive CFG-filer.

Här är en grundläggande översikt över vad du kan hitta i MUGEN `.cfg`-fil:

1. **Systemkonfiguration**: CFG-filer innehåller ofta inställningar relaterade till spelmotorns allmänna beteende. Detta inkluderar saker som skärmupplösning, ljudinställningar och ingångskonfiguration (tangentbord, joystick eller kontrollmappningar).
    








2. **Standarder för tecken och scener**: Du kan definiera standardinställningar för karaktärer och scener. Du kan till exempel ange vilka karaktärer och stadier som laddas när spelet startar.
    








3. **Spelalternativ**: MUGEN `.cfg`-filer kan också styra olika spelalternativ såsom runda tidsgränser, skadeskalning och mer.
    








4. **Felsökning och utveckling**: Avancerade användare kan använda `.cfg`-filer för felsöknings- och utvecklingssyften. Dessa inställningar kan styra hur felsökningsinformation visas på skärmen eller definiera andra utvecklingsrelaterade beteenden.
    








5. **Screenpack Configuration**: Screenpacks är visuella teman som förändrar spelets utseende och känsla. `.cfg`-filer kan specificera vilket screenpack som används och konfigurera dess olika element.
    








6. **AI-beteende**: MUGEN låter dig definiera hur datorstyrda karaktärer (AI) beter sig i strider. `.cfg`-filer kan innehålla inställningar relaterade till AI-svårigheter och beteende.

## MUGEN konfigurationsfil

En MUGEN CFG-fil (konfiguration) är en avgörande komponent för skapare i en värld av anpassade fightingspel. Det ger dem möjlighet att forma grundläggande spelregler. Detta inkluderar faktorer som hur länge varje omgång varar, utmaningsnivå från datorstyrda motståndare, spelets takt, i vilken utsträckning kombinationer påverkar skadan och mycket mer.

Dessutom tillåter CFG-fil skapare att bestämma spelets skärminställningar, såsom skärmupplösning och bestämma om MUGEN ska spela ljudeffekter och musik under spelandet. För dem som är väl insatta i MUGENs krångligheter erbjuder den här filen potential att justera en rad andra spelrelaterade inställningar för att skapa en unik spelupplevelse.

Som standard finns MUGENs primära CFG-fil, känd som `mugen.cfg`, i programmets datamapp. Även om det är möjligt att direkt redigera spelets inställningar i den här filen, är det i allmänhet att rekommendera att skapa en säkerhetskopia först. Denna försiktighetsåtgärd säkerställer att du enkelt kan återställa MUGEN till sina ursprungliga inställningar om det behövs och förhindra att oavsiktliga ändringar stör din spelupplevelse.

## MUGEN - Game Engine

MUGEN är mångsidig och mycket anpassningsbar 2D-kampspelsmotor utvecklad av Elecbyte. Namnet "MUGEN" står för "Mugen Ultimate Game Engine". Det släpptes ursprungligen 1999 och har sedan dess fått en dedikerad community av användare och skapare som använder motor för att designa och utveckla sina egna 2D-kampspel.

Här är några nyckelfunktioner och aspekter av MUGEN:

1. **Anpassningsbara karaktärer:** MUGEN låter användare skapa och importera sina egna karaktärer (kända som "fighters" eller "sprites") till spelet. Skapare kan designa unika rörelseuppsättningar, animationer och specialattacker för dessa karaktärer, vilket gör det möjligt att inkludera praktiskt taget vilken karaktär som helst från olika franchiser eller originalskapelser.
    








2. **Stapper:** Förutom karaktärer kan användare också skapa och anpassa scener där strider äger rum. Dessa stadier kan ha interaktiva element och unika bakgrunder.
      









3. **Skärmpaket:** Skärmpaket är visuella teman som förändrar spelets övergripande utseende, inklusive menyer, skärmar för val av karaktärer och livsfält. Användare kan skapa och dela sina egna skärmpaket för att ge sina spel ett unikt utseende och känsla.
    








4. **Ljud och musik:** Skapare kan lägga till ljudeffekter och bakgrundsmusik till sina spel, vilket förbättrar den övergripande spelupplevelsen.
    








5. **Skript:** Avancerade användare kan använda inbyggt skriptspråk för att skapa komplexa karaktärsbeteenden, unik spelmekanik och specialeffekter.

## Hur öppnar man filen CFG?

MUGEN CFG-filer är vanliga textdokument som gör dem tillgängliga med olika textredigerare. På Windows kan du använda Microsoft Notepad eller WordPad, medan macOS-användare kan använda Apple TextEdit för detta ändamål. Dessa redigerare tillåter användare att enkelt visa och ändra konfigurationsinställningar i CFG-filer.

Program som öppnar eller refererar till CFG-filer

- Elecbyte MUGEN
- Anteckningsblock
- Textredigering

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
* [Mugen (spelmotor)](https://en.wikipedia.org/wiki/Mugen_(game_engine))

