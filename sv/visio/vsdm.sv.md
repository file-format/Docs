{
  "date" : "2019-10-11",
  "keywords" :[ "vsdm-fil", "vsdm-filformat", "vad är en vsdm-fil", "fil", "vsdm-exempel", "vsdm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDM - Microsoft Visio Ritningsfilformat",
  "description":"Läs mer om VSDM-filformat och API:er som kan skapa och öppna VSDM-filer.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VSDM fil?

Filer med filtillägget .vsdm är ritfiler skapade med Microsoft Visio-applikationen som stöder makron. VSDM-filer är OPC/XML-ritningar som liknar VSDX men som också ger möjlighet att köra makron när filen öppnas. Makron är användardefinierade åtgärder/steg som är utvecklade i Visual Basic for Applications (VBA) och kan användas för att utföra repetitiva uppgifter. VSDM-filformat introducerades i och med lanseringen av Microsoft Visio 2013. Visio-filer används för att skapa ritningar som innehåller visuella objekt, flödesscheman, UML-diagram, informationsflöde, organisationsdiagram, programvarudiagram, nätverkslayout, databasmodeller, objektkartläggning och annat liknande information. Filer som genereras med Visio kan också exporteras till olika filformat som [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra.

## VSDM filformat

VSDM-filer är baserade på Open Packaging Conventions och XML och utvecklare kan dra nytta av detta format genom att lära sig hur man arbetar med dessa filer programmatiskt. Formatet ärver många av samma XML-strukturer som dess delar från filformatet Visio XML Drawing (.vdx). Interoperabiliteten med Visio-filer ökar avsevärt eftersom programvara från tredje part kan manipulera Visio-filer på filformatsnivå.

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations" delar.

### Dokument ###

Dokumentdelarna innehåller det faktiska innehållet och metadata för Visio-filen, som namnet på filen, den första sidan och alla former som den innehåller, och till och med dataanslutningarna för formerna. Bilder och textfiler i paketet betraktas som dokumentdelar.

### Relationer ###

Relationsdelarna i en Visio-fil lagras i mappen "\_rels" och beskriver hur delarna i paketet är relaterade till var och en. Det ger också filens struktur. Ett fristående XML-dokument använder elementets överordnade/underordnade relation för att bestämma förhållandet mellan enheter och varandra. Ett giltigt Visio 2013-filformat innehåller rätt uppsättning delar och paketet innehåller relationerna mellan delarna.

Relationsdelar är XML-dokument som beskriver relationerna mellan olika dokumentdelar inom paketet. De definierar en association mellan två objekt: en specificerad källa (definierad av namnet och platsen för relationsfilen) och en specificerad måldokumentdel. Till exempel används relationsdelar för att beskriva vilka formmaster som är associerade med filen, hur sidor relaterar till filen och till varandra, eller hur bilder och objekt relaterar till en specifik sida.

## Referenser ##

* [Introduktion till Visio-filformat](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

