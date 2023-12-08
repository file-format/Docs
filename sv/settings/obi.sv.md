{
"datum": "2023-05-02",
  "keywords": [
"obi fil",
"vad är en obi-fil",
"vilket är formatet på obi-filen",
"fil",
"obi filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "OBI-filformat - Outlook RSS-prenumerationsfil",
  "description":"Läs mer om OBI-format och API:er som kan skapa och öppna OBI-filer.",
  "linktitle": "OBI",
  "menu": {
    "docs": {
      "identifier": "settings-obi",
      "parent": "settings"
}
},
"lastmod": "2023-05-02"
}

## Vad är en OBI fil?

OBI-fil är en Outlook RSS-prenumerationsfil som låter användare prenumerera på ett RSS-flöde i Microsoft Outlook. RSS står för Really Simple Syndication som är ett webbflödesformat som används för att publicera ofta uppdaterat innehåll som blogginlägg, nyhetsrubriker eller poddsändningar.

För att prenumerera på RSS-flöde i Outlook kan användare klicka på länken till RSS-flöde på en webbplats eller kopiera URL:en till RSS-flödet och klistra in det i dialogrutan "Lägg till nytt RSS-flöde" i Outlook. Outlook kommer då regelbundet att kontrollera RSS-flödet för nytt innehåll och visa det i användarens RSS-flödesmapp.

Outlook RSS-prenumerationsfiler har filtillägget ".rss". Dessa filer innehåller URL-adressen till RSS-flödet och kan användas för att dela RSS-flödesprenumerationer med andra eller för att säkerhetskopiera och återställa RSS-flödesprenumerationer.

## OBI-filformat - Mer information

OBI-filer är kända som OPML-fil (Outline Processor Markup Language) och innehåller en lista över RSS-flödesadresser som har prenumererats på i Microsoft Outlook.

När en användare exporterar sina RSS-flöden till OBI-filen innehåller den en lista över alla RSS-flöden de har prenumererat på, inklusive titeln på varje flöde, webbadressen till flödet och all annan relevant information. Detta gör det möjligt för användare att enkelt överföra sina RSS-flödesprenumerationer till en annan RSS-läsare eller att säkerhetskopiera sina prenumerationer för förvaring.

OBI-filer kan också användas för att importera RSS-flödesprenumerationer till Microsoft Outlook eller en annan RSS-läsare. För att importera OBI-fil till Outlook kan användare klicka på "Arkiv" > "Öppna och exportera" > "Importera/exportera" > "Importera från ett annat program eller fil" > "Nästa" > "Importera RSS-flöden från en OPML-fil" och bläddra sedan till OBI-filens plats på datorn.

## Vilket är formatet på filen OBI?

Outlook RSS-prenumerationsfilen även känd som OBI-fil använder XML (eXtensible Markup Language) för att definiera strukturen och innehållet i filen.

OBI-filer består av serier av kapslade element var och en med sin egen uppsättning attribut och värden. Huvudelementet i OBI-filen är "outline"-elementet som innehåller information om RSS-flödet inklusive flödets titel, flödets URL och all annan relevant information.

Varje "kontur"-element kan också innehålla underordnade element som representerar undermappar eller underkategorier i RSS-flödeslistan. Strukturen för OBI-filen möjliggör enkel organisation och hantering av RSS-feedprenumerationer och den kan användas för att överföra prenumerationer mellan olika RSS-läsare eller för att säkerhetskopiera och återställa prenumerationer.

## Referenser
* [Vad är RSS-flöden?](https://support.microsoft.com/en-us/office/what-are-rss-feeds-e8aaebc3-a0a7-40cd-9e10-88f9c1e74b97)

