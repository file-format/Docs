{
"datum":"2023-09-21",
   "keywords":[
"bps",
"bps-fil",
"vad är en bps-fil",
"hur man öppnar bps-fil",
"bps filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"BPS-filformat - BPS-patchfil",
   "description":"Läs mer om BPS-format och API:er som kan skapa och öppna BPS-filer.",
   "linktitle":"BPS",
   "menu":{
      "docs":{
         "identifier":"game-bps",
         "parent":"game"
}
},
"lastmod":"2023-09-21"
}

## Vad är en BPS fil?

En ".bps" filtillägg hänvisar vanligtvis till en binär patchfil. Dessa filer används för att applicera patchar eller uppdateringar till befintliga filer eller programvara. Här är lite mer information om BPS-filer:

1. **Patchfiler:** BPS-filer innehåller binära data som representerar de ändringar som behövs för att uppdatera eller modifiera en befintlig fil eller ett befintligt program. Istället för att ersätta hela filen innehåller korrigeringsfilerna bara skillnaderna mellan originalfilen och den uppdaterade versionen.

2. **ROM-hackning:** BPS-filer används ofta i samband med ROM-hackning. ROM-hackare använder BPS-filer för att distribuera patchar som modifierar spelkoden eller innehållet i klassiska videospel-ROM. Spelare kan applicera dessa patchar på sina spel-ROM för att uppleva modifieringar och översättningar av fans.

3. **Läggningsapplikation:** För att applicera en BPS-lapp behöver du ett lappverktyg. Populära patchverktyg som "Floating IPS" eller "Beat" låter dig applicera BPS-patchar på motsvarande ROM-fil och skapa en modifierad version av spelet eller programvaran.

I följande avsnitt kommer vi att utforska programvaruapplikationerna som är associerade med BPS-filer.

## Flytande IPS

Floating IPS (Flips) är ett populärt och användarvänligt verktyg för att applicera patchar på ROM-filer i samband med ROM-hackning. Det används ofta i emulerings- och fanöversättningsgemenskaperna. Lite mer information relaterad till det ges nedan.

- **Patchapplikation:** Flytande IPS är utformad för att applicera patchfiler, vanligtvis i BPS-format, på ROM-filer. Dessa patchar innehåller binär data som representerar ändringar av den ursprungliga ROM-skivan, såsom översättningar, buggfixar eller modifieringar av spelet.

- **Automatisk patchning:** Flytande IPS upptäcker automatiskt mål-ROM:s header och applicerar patchen därefter, vilket förenklar patchningsprocessen.

- **Checksum Verification:** Verktyget innehåller ofta en checksumverifieringsfunktion för att säkerställa integriteten hos det korrigerade ROM-minnet, vilket minskar risken för fel eller korruption.

- **Skapa patch:** Även om Floating IPS främst används för att applicera patchar, kan den också användas för att skapa patchfiler (BPS-format) från skillnaderna mellan två ROM, vilket gör det användbart för ROM-hacknings- och översättningsprojekt.

## MultiPatch

MultiPatch är ett annat verktyg som ofta används i ROM-hackargemenskapen, speciellt för att applicera patchar på ROM-filer. Den liknar sin funktion till Floating IPS men kommer med sina egna funktioner och gränssnitt. Lite mer information relaterad till det ges nedan.

- **Patchapplikation:** MultiPatch är utformad för att applicera patchar på ROM-filer, vanligtvis i format som IPS, UPS eller BPS. Dessa patchar innehåller binär data som modifierar den ursprungliga ROM-skivan, ofta för ändamål som översättningar, buggfixar eller anpassningar.

- **Stöd för olika patchformat:** Den stöder en rad patchfilformat, inklusive IPS (International Patching System), UPS (Universal Patch Format) och BPS (Binary Patch System), vilket gör den mångsidig för olika typer av plåster.

- **Batch-patch:** MultiPatch kan användas för att applicera flera patchar på en enda ROM-fil eller på flera ROM-filer samtidigt, vilket är användbart för komplexa ROM-hack eller projekt som involverar flera patchar.

- **Skapa patch:** På samma sätt som flytande IPS kan MultiPatch också användas för att skapa patchfiler från skillnaderna mellan två ROM, vilket är användbart för ROM-hacknings- och översättningsprojekt.

## Hur öppnar man filen BPS?

Program som öppnar BPS-filer inkluderar

- Flytande IPS (gratis) för (MAC, Windows och Linux)
- MultiPatch (gratis) för (MAC)

## Andra BPS-filer

Här är andra filtyper som använder filtillägget **.bps**.

- [BPS - BPS Malware-fil från SpywareCops](/sv/misc/bps-malware/)
- [BPS - Microsoft Works Document Backup](/sv/misc/bps-works/)

## Referenser
* [Flytande IPS](https://www.gamebrew.org/wiki/Floating_IPS)

