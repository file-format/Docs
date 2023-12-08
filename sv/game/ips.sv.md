{
"datum":"2023-09-21",
   "keywords":[
"ips",
"ips-fil",
"ips intern korrigeringsfil för patchsystem",
"vad är en ips-fil",
"hur man öppnar ips-fil",
"ips filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"IPS-filformat - intern patchfil för systempatch",
   "description":"Läs mer om IPS-format och API:er som kan skapa och öppna IPS-filer.",
   "linktitle":"IPS",
   "menu":{
      "docs":{
         "identifier":"game-ips",
         "parent":"game"
}
},
"lastmod":"2023-09-21"
}

## Vad är en IPS fil?

En "IPS-fil" hänvisar vanligtvis till en "Internal Patching System Patch File." IPS är en förkortning för "International Patching System", och det är ett filformat som används för att skapa och applicera patchar på ROM-filer (Read-Only Memory), ofta i samband med videospelsemulering och ROM-hackning.

Så här fungerar det:

- **Original ROM:** Du börjar med en original ROM-fil, som i huvudsak är en kopia av ett videospel eller programvara lagrad i ett ROM-format. Den här filen är vanligtvis skrivskyddad, vilket innebär att du inte kan ändra den direkt.

- **IPS-patchfil:** En IPS-patchfil innehåller de ändringar du vill tillämpa på det ursprungliga ROM-minnet. Dessa ändringar kan vara buggfixar, översättningar eller andra ändringar.

- **Patchapplikation:** För att tillämpa ändringarna behöver du ett verktyg eller program som kan läsa IPS-patchfilen och tillämpa den på original-ROM. Denna process "lappar" i huvudsak den ursprungliga ROM-filen med de ändringar som anges i IPS-filen, vilket skapar en modifierad ROM-fil.

- **Modifierad ROM:** Resultatet är ett modifierat ROM som innehåller ändringarna från IPS-patchfilen. Denna modifierade ROM kan sedan användas i en emulator eller på kompatibel hårdvara för att spela spelet med önskade modifieringar.

Dessa patchar används vanligtvis för att göra ändringar eller förbättringar av spel, och de kan omfatta olika ändringar, inklusive modifieringar av grafik, modeller och annan speldata. IPS-filer är särskilt lämpliga för relativt små patchar, vanligtvis mindre än 16 megabyte i storlek.

I följande avsnitt kommer vi att utforska de program som är associerade med IPS-filer.

## Lunar IPS

Lunar IPS är ett populärt och användarvänligt verktyg som används för att skapa och applicera IPS (Internal Patching System) patchar på ROM-filer. Här är några viktiga funktioner och information om Lunar IPS:

- **Lättarskapande:** Lunar IPS tillåter användare att skapa IPS-korrigeringar genom att ange de ändringar de vill göra i en original ROM-fil. Du kan välja original-ROM och den modifierade versionen, och Lunar IPS kommer att generera en IPS-patchfil baserat på skillnaderna mellan de två filerna.

- **Patchapplikation:** När du väl har en IPS-patchfil låter Lunar IPS dig applicera den på ett original-ROM. Denna process "lappar" i huvudsak ROM-minnet med de ändringar som anges i IPS-filen, vilket skapar ett modifierat ROM.

- **Lättvikt:** Lunar IPS är ett litet och lätt program, vilket innebär att det inte förbrukar mycket systemresurser och går snabbt att ladda ner och köra.

## IPSWin

IPSWin är ett verktyg som främst är utformat för Windows-användare som underlättar skapandet och tillämpningen av IPS (Internal Patching System) patchar till ROM-filer. Det är ett enkelt och användarvänligt verktyg, lämpligt för dem som vill patcha ROM enkelt. Här är lite information om IPSWin:

- **Skapa korrigeringar:** IPSWin tillåter användare att skapa IPS-korrigeringar genom att jämföra två ROM-filer: den ursprungliga ROM och den modifierade ROM. Den identifierar skillnaderna mellan de två filerna och genererar en IPS-patchfil som innehåller dessa ändringar.

- **Patchapplikation:** Detta verktyg gör det också möjligt för användare att applicera befintliga IPS-patchfiler på original-ROM. Genom att välja lämplig IPS-patch och original-ROM kommer IPSWin att slå samman ändringarna till en ny ROM-fil och skapa en patchad version.

## Hur öppnar man filen IPS?

Program som öppnar IPS-filer inkluderar

- Lunar IPS
- IPSWin
- MultiPatch

## Andra IPS-filer

Här är andra filtyper som använder filtillägget **.ips**.

- [IPS - PlayStation 2 In-Game Video](/sv/game/ips-ps2/)
- [IPS - iOS Analytics Data](/sv/misc/ips/)

## Referenser
* [Lunar IPS](https://www.romhacking.net/utilities/240/)
