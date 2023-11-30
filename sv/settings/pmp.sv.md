{
"datum": "2023-03-28",
  "keywords": [
"pmp-fil",
"vad är en pmp-fil",
"hur man skapar en pmp-fil",
"fil",
"pmp filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "PMP-filformat - AutoCAD Plot Model Parameter File",
  "description":"Läs mer om PMP-format och API:er som kan skapa och öppna PMP-filer.",
"linktitle": "PMP",
  "menu": {
    "docs": {
      "identifier": "settings-pmp",
      "parent": "settings"
}
},
"lastmod": "2023-03-28"
}

## Vad är en PMP fil?

Filtillägget ".pmp" används av AutoCAD för dess Plot Model Parameter File. När du ritar en ritning i AutoCAD innehåller PMP-filen (Plot Model Parameter) de skrivarspecifika inställningarna och konfigurationen som används för plottningsprocessen. Den här filen skapas automatiskt när du anpassar plottinställningarna i AutoCAD och sparar dem som en namngiven plotstil.

PMP-filen används för att lagra plotterkonfigurationen, såsom pappersstorlek, plotskala, plotarea och plotoffset, såväl som andra inställningar som linjevikter, linjetyper och penntilldelningar. Genom att spara dessa inställningar i en PMP-fil kan du enkelt tillämpa dem på framtida plottningsjobb utan att behöva konfigurera skrivarinställningarna manuellt varje gång.

Du kan redigera PMP-filen för att ändra plotterinställningarna eller skapa nya plotstilar med olika konfigurationer. PMP-filen kan delas med andra AutoCAD-användare eller datorer för att säkerställa konsekventa plottningsresultat.

## PMP-filformat – Mer information

PMP-filen är en vanlig textfil som kan öppnas och redigeras med vilken textredigerare som helst, som Anteckningar eller Wordpad. Förutom skrivarspecifika inställningar kan PMP-filen även innehålla inställningar för plottningsstil, såsom färgmappningar, raster och linjevikter. AutoCAD stöder både systemplottstilar och namngivna plotstilar. Systemplotstilar är fördefinierade plotkonfigurationer som följer med AutoCAD, medan namngivna plotstilar är användardefinierade plotkonfigurationer som sparas i en PMP-fil.

Du kan anpassa plottningsinställningarna i AutoCAD genom att komma åt Utskriftshanteraren, som låter dig ställa in plotkonfigurationer för olika typer av utdata, såsom utskrift, plottning till en PDF-fil eller publicering till en DWF-fil. När du ritar en ritning i AutoCAD kan du välja den plotstil som ska användas från en lista över tillgängliga plotstilar. Plottstilen bestämmer hur objekten i ritningen kommer att plottas baserat på deras egenskaper, såsom färg, linjetyp eller linjevikt.

## Hur skapar man en PMP-fil?

För att skapa en PMP-fil i AutoCAD kan du följa dessa steg:

1. Öppna ritningsfilen som du vill rita och gå till fliken "Layout".
2. Välj "Page Setup Manager" från gruppen "Page Setup" på fliken "Layout".
3. I dialogrutan "Sidinställningar" väljer du "Ny" för att skapa en ny sidinställningar.
4. I dialogrutan "New Page Setup" anger du inställningarna för den nya sidinställningarna, såsom skrivare, pappersstorlek, plotskala och plotarea. Du kan också välja den plotstil som ska användas för den nya siduppsättningen.
5. Klicka på "OK" för att spara den nya sidinställningarna och avsluta dialogrutan "Ny sidinställningar".
6. Tillbaka i dialogrutan "Page Setup Manager", välj den nya sidinställningarna och klicka på "Ändra" för att göra ytterligare justeringar av plottinställningarna eller plottstilen.
7. När du har gjort alla nödvändiga ändringar klickar du på "Stäng" för att avsluta dialogrutan "Sidinställningar".
8. För att spara plottinställningarna och plottstilen som en PMP-fil, välj "Plot Style Manager" från gruppen "Plot" på fliken "Output".
9. I dialogrutan "Plot Style Manager", välj den plotstil som du vill spara som en PMP-fil och klicka på "Exportera".
10. Ange filnamnet och platsen för PMP-filen i dialogrutan "Exportera plottstilstabell" och klicka på "Spara".
11. PMP-filen är nu sparad och kan användas för framtida plottningsjobb.

## Referenser
* [AutoCAD-programvara](https://en.wikipedia.org/wiki/AutoCAD)

