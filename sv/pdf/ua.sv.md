{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA filformat",
  "description":"Läs mer om PDF/UA-filformat och API:er som kan skapa och öppna PDF/UA-filer.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Vad är PDF/UA-fil? #

PDF/UA publicerades som [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) i augusti 2012 och är den överlägset första fullständiga definitionen av en uppsättning krav för universellt tillgängliga PDF-dokument. Termen "allmänt tillgänglig" syftar på förståelsen att informationen i ett [PDF](/sv/pdf/) dokument ska vara lika och oberoende tillgänglig för alla i allmänhet och för personer med funktionsnedsättning i synnerhet. Införandet av PDF/UA-standarden kan betraktas som ett stort steg för att skapa verktyg och applikationer för att skapa och läsa PDF-innehåll.

## Filformatskrav ##

PDF/UA har några bestämda krav i sin bas som fungerar som kärnan i denna standard. I huvudsak är dessa baserade på taggning av PDF-filer, vilket innebär att alla PDF/UA-dokument måste vara korrekt taggade. Det kräver också att taggarna är semantiskt lämpliga och i logisk ordning. Detta säkerställer att slutdokumentet som skapats med PDF/UA-specifikationer är mer tillförlitligt och tillgängligt. Detta kan få PDF-författare att fråga sig om de behöver veta allt om alla sådana krav? Lyckligtvis är det inte så här eftersom PDF/UA-överensstämmelseverktygen tar ansvaret för att lägga till och bevara PDF:ens tillgänglighet.

Filformatkraven för PDF/UA är följande.

* Innehåll kategoriseras på ett av två sätt: meningsfullt innehåll och artefakter som dekorativa sidelement. Allt meningsfullt innehåll måste taggas och integreras i strukturträdet för alla taggar i ett dokument. Artefakter, å andra sidan, behöver bara märkas som sådana.
* Meningsfullt innehåll ska markeras med taggar och tillsammans med övriga taggar i dokumentet skapa ett komplett strukturträd.
* Meningsfullt innehåll måste markeras med lämpliga semantiska taggar.
* Strukturträdet som skapas av dokumenttaggarna måste återspegla dokumentets logiska läsordning.
* Endast standardtaggar som definieras i PDF 1.7 får användas; om några andra taggar används måste en rolltilldelningspost registrera vilken standardtagg var och en representerar.
* Information får inte förmedlas med enbart visuella medel (t.ex. kontrast, färg eller position på sidan).
* Inget flimrande, blinkande eller blinkande innehåll är tillåtet, varken som effekter kontrollerade av JavaScript eller som en del av videor som är inbäddade i PDF-filen.
* En dokumenttitel måste anges, och dokumentet måste ställas in så att titeln (istället för filnamnet) visas i fönstrets titel.
* Språket för allt innehåll måste noteras, och språkändringar måste uttryckligen markeras som sådana.

## PDF/UA-överensstämmelse ##

PDF/UA-standarden definierar specifikationer för innehåll, läsare och hjälpmedel. Dessa tre aspekter är kopplade till varandra utifrån innehållet i dokumentet. Överensstämmelsekraven för var och en av dessa är enligt nedan.

## Överensstämmande filer ##

Filer som överensstämmer med PDF/UA-standarden bör innehålla funktioner som är giltiga enligt [PDF 1.7-specifikationerna](http://www.adobe.com/go/pdfreference). Funktioner som är förbjudna av PDF/UA specifikt bör dock uteslutas.

## Konforma läsare ##

En överensstämmande läsare måste följa reglerna i PDF 1.7-specifikationerna. Specifikt bör den stödja:

* alla taggar, attribut och nyckelvärden som anges för tillgänglighet. Den bör också ha förmågan att bearbeta och representera digitala signaturer, anteckningar och valfritt innehåll.
* bearbeta och representera digitala signaturer, anteckningar och valfritt innehåll
* navigera i dokumentet på olika sätt

## Överensstämmande hjälpmedelsteknik ##

En överensstämmande hjälpmedelsteknik är bunden för att stödja PDF/UA-funktionerna. Dessa inkluderar till exempel funktioner i innehållet och läsaren, och bör tillåta navigering efter sidetiketter, dokumentstruktur eller kontur. Det bör också låta användaren åsidosätta standardnavigeringszoom.

## Referenser ##

* [PDF/UA - Av Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA i ett nötskal](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

