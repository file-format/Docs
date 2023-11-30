{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO File - DISCO Dynamic Discovery Document File Format",
  "description":"Lär dig mer om vad en VDISCO-fil är?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Vad är en VDISCO fil?

En VDISCO-fil är en upptäcktsfil som används av Microsoft Visual Studio i dess webbtjänster. Den tillhandahåller information om tillgängliga webbtjänster som deras URL:er, namnområden och metoder. VDISCO-filen liknar filformatet [DISCO](/sv/web/disco/) men genereras vid körning. Den lagras i webbtjänstapplikationen och används av Visual Studio för att dynamiskt upptäcka och använda webbtjänster i ett projekt. VDISCO-filer används i kombination med filen [.asmx](/sv/web/asmx/) som innehåller den faktiska webbtjänstkoden.

Du kan öppna VDISCO-filen i vilken textredigerare som helst som Microsoft Notepad, Github Atom och Apple TextEdit. Det kan också öppnas med Microsoft Visual Studio 2012 och senare för att arbeta med det.

## VDISCO filformat

En VDISCO-fil sparas och lagras i [XML](/sv/web/xml/) filformat som är ett universellt format för sammansättning och publicering av data. Den innehåller tjänstens URL, namnområden och metoder i vanliga XML-taggar där varje tagg innehåller respektive värde av dess information.

## Referenser

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Web Services Discovery](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# Exempel på DiscoveryClient Class](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

