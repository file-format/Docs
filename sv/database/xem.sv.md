{
"datum": "2023-04-27",
  "keywords": [
"xem fil",
"vad är en xem-fil",
"vilket är formatet på xem-filen",
"vad innehåller xem-filen",
"fil",
"xem filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "XEM-filformat - PowerDesigner-modelldefinitionsfil",
  "description":"Läs mer om XEM-format och API:er som kan skapa och öppna XEM-filer.",
"linktitle": "XEM",
  "menu": {
    "docs": {
      "identifier": "database-xem",
      "parent": "database"
}
},
"lastmod": "2023-04-27"
}

## Vad är en XEM fil?

XEM-fil är XML-metadatautbytesfil som kan användas för att exportera metadatainformation om PowerDesigner-modellen till extern fil. XEM-filen innehåller information om modellen inklusive enheter, relationer, nycklar, diagram och annan relevant metadata. Filen kan användas för att överföra eller dela modell med andra användare eller system eller för att skapa en säkerhetskopia av modellen för förvaring.

För att exportera PowerDesigner-modellen till .xem-fil kan du gå till Arkiv-menyn och välja "Exportera" och sedan "XML Metadata Interchange". Du kan sedan välja specifika element av modellen som du vill exportera och spara den resulterande .xem-filen på önskad plats.

På samma sätt kan du importera .xem-fil till PowerDesigner-modellen genom att välja "Importera" från Arkiv-menyn och sedan välja alternativet "XML Metadata Interchange". Du kan sedan välja .xem-fil att importera och välja specifika element att importera till din modell.

.xem-filformatet är en användbar funktion i PowerDesigner som gör det möjligt för användare att dela och överföra metadatainformation mellan olika system eller användare.

## Vilket är formatet på filen XEM?

Formatet på XEM-filen är textbaserat vilket innebär att den kan öppnas eller redigeras med valfri textredigerare t.ex. Notepad, Notepad++ etc. Formatet följer XML-standarden som är en allmänt använd standard för att lagra och utbyta data mellan olika system.

## XEM-filformat - Mer information

När du exporterar PowerDesigner-modellen till .xem-filen kan du välja vilken specifik metadatainformation som ska inkluderas i exporten. Detta kan vara användbart om du bara vill överföra vissa delar av modellen eller om du vill minska filstorleken på den exporterade .xem-filen.

När du importerar .xem-fil till PowerDesigner-modellen har du möjlighet att välja vilka specifika element i modellen som ska importeras. Detta kan vara användbart om du bara vill importera vissa element i modellen eller om du vill slå samman importerade element med befintliga element i modellen.

## Vad innehåller XEM-filen?

XEM-filen i PowerDesigner innehåller metadatainformation om PowerDesigner-modellen. Denna metadatainformation inkluderar:

- **Entiteter:** .xem-filen innehåller information om enheter i modellen inklusive deras namn, beskrivningar och attribut.
- **Attribut:** .xem-filen innehåller information om attribut för varje entitet, inklusive deras namn, datatyper och begränsningar.
- **Relationer:** .xem-filen innehåller information om relationer mellan enheter, inklusive deras typer, kardinaliteter och främmande nycklar.
- **Nycklar:** .xem-filen innehåller information om nycklar som används i modellen, inklusive primärnycklar och unika nycklar.
- **Diagram:** .xem-filen innehåller information om diagram i modellen, inklusive deras namn, beskrivningar och layout.
- **Anpassningar:** .xem-filen kan också innehålla information om eventuella anpassningar eller modifieringar av modellen, inklusive användardefinierade datatyper, domäner och mallar.

De specifika elementen och detaljerna som ingår i .xem-filen kan variera beroende på de inställningar och alternativ som valts under exportprocessen. När du importerar en .xem-fil till en ny modell kan du välja vilka specifika element som ska inkluderas, vilket gör att du kan slå samman de importerade elementen med den befintliga modellen på ett flexibelt sätt.

## Referenser
* [PowerDesigner](https://en.wikipedia.org/wiki/PowerDesigner)

