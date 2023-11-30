{
"datum":"2023-11-09",
   "keywords":[
"Zoo",
"zoo fil",
"zoo komprimerad fil",
"hur man öppnar en zoo-fil",
"fil",
"zoo filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"ZOO-fil - Vad är en .zoo-fil och hur öppnar man den?",
   "description":"Läs mer om ZOO-komprimerade filformat och API:er som kan skapa och öppna ZOO-filer.",
"linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Vad är ZOO fil?

En `.zoo`-fil är ett arkivformat som används för att komprimera och lagra filer och kataloger; liknar andra arkivformat som ".zip", ".tar" och ".rar". ".zoo"-formatet var populärt i början av datoranvändningen men har blivit mindre vanligt på senare år. Det utvecklades ursprungligen av **Rahul Dhesi** och användes främst på Unix- och DOS-system.

En `.zoo`-fil innehåller vanligtvis en eller flera filer och kataloger som har komprimerats och arkiverats till en enda fil. Du kan skapa och extrahera `.zoo`-filer med hjälp av olika programvaruverktyg som stöder detta format.

ZOO-arkiv har en unik funktion som tillåter dem att lagra flera versioner av samma fil förutsatt att varje version har ändrats vid olika datum. Detta innebär att ZOO-användare kan spara och komma åt tidigare iterationer av filer direkt från ZOO-arkivet. Den här funktionen gör det möjligt för användare att återgå till tidigare version av filen eller jämföra äldre version med nyare, vilket erbjuder ett bekvämt sätt att hantera filrevisioner och ändringar över tid.

## Vanliga funktioner för ZOO-filer

Här är några vanliga operationer förknippade med `.zoo`-filer:

1. **Skapa en `.zoo`-fil:** Du kan använda kommandoradsverktyg som "zoo" för att skapa en `.zoo`-fil. Till exempel kommer följande kommando att skapa `.zoo`-arkiv från katalogen:
    








`zoo a -c archive.zoo directory/`
    








I det här kommandot står "a" för "add", "-c" anger komprimering och "archive.zoo" är namnet på utdataarkivet.
    








2. **Extrahera filer från en `.zoo`-fil:** För att extrahera innehållet i `.zoo`-arkivet kan du använda kommandot så här:
    








`zoo e archive.zoo`
    








Detta kommando kommer att extrahera filer från filen `archive.zoo`.
    








3. **Lista innehållet i en `.zoo`-fil:** Du kan lista innehållet i `.zoo`-arkivet utan att extrahera dem med alternativet "l":
    








    








`zoo l archive.zoo`

## Hur öppnar man filen ZOO?

Program som öppnar ZOO-filer inkluderar

- **zoo** (gratis) för (Windows, Linux)

## Referenser
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))
