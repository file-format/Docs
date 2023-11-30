{
"datum":"2023-01-04",
   "keywords":[
"Posten",
"ups-fil",
"ups patch-fil",
"hur man öppnar en ups-fil",
"fil",
"ups filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"UPS-filformat - UPS-patchfil",
   "description":"Läs mer om UPS Patch File-format och API:er som kan skapa och öppna UPS-filer.",
"linktitle":"UPS",
   "menu":{
      "docs":{
         "identifier":"game-ups",
         "parent":"game"
}
},
"lastmod":"2023-01-04"
}

## Vad är en UPS fil?

En UPS-fil, som står för **Universal Patching System**, är en typ av patchfil som används för att modifiera eller tillämpa ändringar på data i ett videospel eller annan programvara. UPS-filer används vanligtvis i emuleringsgemenskapen för att applicera patchar eller modifieringar på ROM (Read-Only Memory) av gamla videospel.

## UPS patchfil

Så här fungerar en UPS-patchfil:

1. **Originaldata:** Du börjar med den ursprungliga ROM-filen för ett videospel eller programvara som du vill modifiera. Denna ROM innehåller spelets kod och data.
    






2. **Patchfil:** En UPS-patchfil skapas med hjälp av specialiserad patchprogramvara. Denna korrigeringsfil innehåller ändringar som du vill tillämpa på originaldata. Dessa ändringar kan inkludera buggfixar, översättningskorrigeringar eller andra modifieringar.
    






3. **Lättningsprocess:** För att tillämpa ändringar använder du ett UPS korrigeringsverktyg som tar original ROM och UPS korrigeringsfil som indata. Patchverktyget tillämpar sedan ändringar som anges i UPS-patchfilen på original-ROM och skapar en modifierad version av spelet eller programvaran.
    






4. **Resultat:** Utdata är ett korrigerat eller modifierat ROM som innehåller ändringar från UPS-patchfilen. Detta patchade ROM kan sedan spelas på en emulator eller användas på andra sätt beroende på ändringar som görs.
    







UPS-patchfiler är populära i emuleringsgemenskapen eftersom de tillåter användare att göra förbättringar eller modifieringar av gamla spel utan att distribuera hela spelets ROM som kan vara föremål för upphovsrätt. Istället kan användare bara dela UPS patchfil som innehåller ändringar och användare kan tillämpa den på sitt lagligt ägda original-ROM.

UPS-patchar erbjuder flera fördelar jämfört med [IPS](/sv/game/ips/):

1. **Ingen storleksbegränsning:** Till skillnad från IPS-patchar som är begränsade till 16 MB kan UPS-patchar användas med filer av alla storlekar. Denna flexibilitet gör UPS särskilt användbar för större spel och mjukvara.
    






2. **Dubbelriktad patchning:** UPS stöder dubbelriktad patchning vilket innebär att en enda UPS-patch både kan tillämpa och ta bort ändringar i ett spel eller programvara. Denna funktion förenklar processen att ändra eller återställa ändringar, vilket förbättrar användarens upplevelse.
    






3. **CRC32-kontrollsummor:** UPS använder CRC32-kontrollsummor som en inbyggd mekanism för att säkerställa att patchar appliceras på korrekt spel eller programvara. Denna kontrollsumma-verifiering hjälper till att upprätthålla integriteten för korrigerade filer och förhindrar oavsiktlig eller felaktig applicering av korrigeringar.

## Hur applicerar man en UPS-patch?

För att applicera en UPS-patch behöver du ett UPS-patchverktyg, som Lunar IPS (för Windows), NUPS (för Windows) eller MultiPatch (för flera plattformar) och original-ROM för spel eller programvara som du vill patcha.

## Hur öppnar man filen UPS?

Program som öppnar UPS-filer inkluderar

- **Lunar IPS** (för Windows)
- **NUPS** (för Windows)
- **MultiPatch** (för flera plattformar)

## Referenser
* [Lunar IPS](https://www.romhacking.net/utilities/240/)

