{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om GADGET-filformat och API:er som kan skapa och öppna GADGET-filer.",
  "title" :"GADGET - Virtuell CD-fil",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## Vad är en GADGET-fil?

En GADGET-fil består av ett litet program som körs i Windows Vista eller Windows 7 sidofältet. Den komprimerar flera webbaserade filer och filerna kan bestå av filerna [.html](/sv/web/html), [.css](/sv/web/css) eller [.js](/sv/web/js/), samt andra webbfiler. GADGET-filer används för små komponenter som sökverktyg, nyhetsflöden, systemverktyg och små spel. Även om GADGET är värd för sidofältet, är de inte specifika för sidofältsområdet; dessa kan lossas och flyttas till skrivbordet efter önskemål.

## GADGET filformat

GADGET-filen är ett omdöpt [ZIP](/sv/compression/zip/)-arkiv som innehåller en samling HTML-, XML-, JScript- och CSS-filer (Cascading Style Sheets). Installationen innehåller att ladda ner .gadget-filen och aktivera nedladdningsprocessen för att installera komponenten eller att spara .gadget-filen till det lokala systemet och dubbelklicka för att starta installationsprocessen.

I grund och botten innehåller en GADGET två filer:

1. **Gadget.xml**: Manifestet, en XML-fil som består av allmän presentation och konfigurationsinformation för gadgeten.
2. **name.html**: En HTML-fil, där namnet anges i<name> taggen för det associerade gadgetmanifestet, som ger omslaget för gadgetens gränssnitt och utgör kärnfunktionaliteten för gadgeten.

Flera instanser av en GADGET-fil kan köras samtidigt. Till exempel, om någon vill veta tiden i olika tidszoner, kan de köra flera instanser av klockgadgeten genom att ställa in varje klocka till en viss tidszon.

### Avbrytande av GADGET

Eftersom Windows Sidebar-plattformen i Windows 7 har allvarliga sårbarheter är prylarna inte längre tillgängliga på Microsofts officiella webbplats. Senare drog Microsoft tillbaka den här funktionen i nyare versioner av Windows. GADGET kan utnyttjas för att komma åt en dators filer, skada en dator, avslöja stötande innehåll eller ändra deras beteende när som helst.

## Referenser

* [Windows Sidebar - av Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Utveckla en gadget för Windows Sidebar del 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

