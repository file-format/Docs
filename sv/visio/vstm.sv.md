{
  "date" : "2019-10-11",
  "keywords" :[ "vstm-fil", "vstm-filformat", "vad är en vstm-fil", "fil", "vstm-exempel", "vstm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTM - Microsoft Visio Template File Format",
  "description":"Läs mer om VSTM-filformat och API:er som kan skapa och öppna VSTM-filer.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VSTM fil?

Filer med VSTM-tillägg är mallfiler skapade med Microsoft Visio som stöder makron. Till skillnad från VSDX-filer kan filer skapade från VSTM-mallar köra makron som är utvecklade i Visual Basic for Applications (VBA)-kod. En mallfil kan skapas för att tillhandahålla grundläggande inställningar för dokumentet som kan användas för att generera ytterligare dokument med dessa inställningar. Visio-filer används för att skapa ritningar som innehåller visuella objekt, flödesscheman, UML-diagram, informationsflöde, organisationsdiagram, programvarudiagram, nätverkslayout, databasmodeller, objektkartläggning och annan liknande information. Filer som genereras med Visio kan också exporteras till olika filformat som PNG, BMP, PDF och andra.

## Filformat ##

VSTM-filer är baserade på Open Packaging Conventions och XML och utvecklare kan dra nytta av detta format genom att lära sig hur man arbetar med dessa filer programmatiskt. Formatet ärver många av samma XML-strukturer som dess delar från filformatet Visio XML Drawing (.vdx). Interoperabiliteten med Visio-filer ökar avsevärt eftersom programvara från tredje part kan manipulera Visio-filer på filformatsnivå.

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations"-delar.

### Dokument ###

Dokumentdelarna innehåller det faktiska innehållet och metadata för Visio-filen, som namnet på filen, den första sidan och alla former som den innehåller, och till och med dataanslutningarna för formerna. Bilder och textfiler i paketet betraktas som dokumentdelar.

### Relationer ###

Relationsdelarna i en Visio-fil lagras i mappen "_rels" och beskriver hur delarna i paketet är relaterade till var och en. Det ger också filens struktur. Ett fristående XML-dokument använder elementets överordnade/underordnade relation för att bestämma förhållandet mellan enheter och varandra. Ett giltigt Visio 2013-filformat innehåller rätt uppsättning delar och paketet innehåller relationerna mellan delarna.

Relationsdelar är XML-dokument som beskriver relationerna mellan olika dokumentdelar inom paketet. De definierar en koppling mellan två objekt: en specificerad källa (definierad av namnet och platsen för relationsfilen) och en specificerad måldokumentdel. Till exempel används relationsdelar för att beskriva vilka formmaster som är associerade med filen, hur sidor relaterar till filen och till varandra, eller hur bilder och objekt relaterar till en specifik sida.

## Referenser ##

* [Introduktion till Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

