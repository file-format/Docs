{
"date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-fil",
"cfg wesnoth markup language file",
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
"title": "CFG-filformat - Wesnoth Markup Language File",
  "description":"Läs mer om CFG Wesnoth Markup Language File-format och API:er som kan skapa och öppna CFG-filer.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "2023-09-27"
}

## Vad är CFG fil?

CFG-filen är också känd som **"Wesnoth Markup Language" (WML)**. Det är ett anpassat märkningsspråk som främst används i spelet "Battle for Wesnoth", som är ett turbaserat strategispel. WML används för att definiera och anpassa olika aspekter av spelet, inklusive scenarier, kampanjer, enheter och mer. Det är ett sätt för moddare och utvecklare att skapa innehåll för spelet.

Det är skrivet i ett format som liknar en kombination av XML och enkel scripting. Här är en översikt över några vanliga element och strukturer du kan hitta i en WML-fil:

1. **Taggar:** WML använder taggar för att definiera olika element i spelet. Taggar är inneslutna i vinkelparenteser. Till exempel:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attribut:** Inom taggar kan du definiera attribut för att ange egenskaper eller värden som är associerade med elementet. I exemplet ovan är "typ" och "träffpunkter" attribut.
    










3. **Arrayer och arrayer av arrayer:** Du kan skapa arrayer av data och till och med arrayer av arrayer för att definiera listor över enheter, terrängtyper eller andra spelelement.
    










4. **Villkorliga uttalanden:** WML stöder villkorliga uttalanden för att kontrollera flödet av spelet. Till exempel:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Slingor:** Du kan använda loopar för att iterera genom listor med objekt eller utföra åtgärder upprepade gånger.
    










6. **Innehåller:** Du kan inkludera andra WML-filer i en WML-huvudfil för att organisera och modularisera ditt innehåll.
    










7. **Händelsehanterare:** Du kan definiera händelsehanterare för att utlösa åtgärder när specifika händelser inträffar i spelet.
    











Här är ett förenklat exempel på en WML-fil som definierar en anpassad enhet:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Slaget om Wesnoth

"The Battle for Wesnoth" är ett populärt turbaserat strategispel med öppen källkod. Den är tillgänglig för flera plattformar, inklusive Mac, Windows, Linux och mer. Spelet har utvecklats av en dedikerad gemenskap av frivilliga och är känt för sitt djupa och engagerande spel, såväl som sin rika fantasivärld.

Viktiga funktioner i "The Battle for Wesnoth" inkluderar:

1. **Fantasimiljö:** Spelet utspelar sig i en fantasivärld med olika raser, inklusive människor, alver, dvärgar, orcher och mer. Spelets lore och berättande är en integrerad del av dess överklagande.
    










2. **Turn-Based Strategy:** Spelet är turbaserat, där spelare tar sig tid att planera och utföra sina drag på sexkantiga rutnät. Den kombinerar taktisk strid med strategiskt beslutsfattande.
    










3. **Kampanjer:** Spelet erbjuder ett brett utbud av enspelarkampanjer, alla med sin egen story, karaktärer och utmaningar. Spelare kan utforska olika berättelser och scenarier.
    










4. **Multiplayer:** "Wesnoth" stöder online multiplayer, vilket gör att spelare kan tävla mot varandra i strategiska strider. Flerspelarlägen inkluderar samarbetsspel och tävlingsmatcher.

## Hur öppnar man filen CFG?

CFG-filer, som vanligtvis förknippas med Wesnoth Markup Language (WML) som används i "The Battle for Wesnoth"-spelet, kan enkelt redigeras med vilken standardtextredigerare som helst. Dessa filer innehåller läsbar kod skriven i WML, som definierar olika aspekter av spelet, inklusive scenarier, enheter och kampanjer.

Även om du kan använda vilken textredigerare som helst för att ändra CFG-filer, har vissa avancerade textredigerare som Emacs och Vi WML-syntaxmarkeringsplugins tillgängliga. Dessa plugins ger användbar färgkodning och formatering för att göra det lättare för användare att särskilja olika element och strukturer inom WML-koden.

Program som öppnar eller refererar till CFG-filer inkluderar

- Slaget om Wesnoth (gratis) för (Windows, MAC, Linux)
- Microsoft Notepad

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
