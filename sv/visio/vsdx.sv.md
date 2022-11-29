{
  "date" : "2019-10-11",
  "keywords" :[ "vsdx fil", "vsdx filformat", "vad är en vsdx fil", "fil", "vsdx exempel", "vsdx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSDX",
  "description":"Läs mer om VSDX-filformat och API:er som kan skapa och öppna VSDX-filer.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VSDX fil?

Filer med filtillägget .vsdx representerar filformatet Microsoft Visio som introducerades från Microsoft Office 2013 och framåt. Det utvecklades för att ersätta det binära filformatet, [.VSD](/sv/image/vsd/), som stöds av tidigare versioner av Microsoft Visio. Det stöds också på Visio Services i Microsoft SharePoint Server 2013 och kräver inget mellanliggande filformat för publicering till SharePoint Server. Visio-filer används för att skapa ritningar som innehåller visuella objekt, flödesscheman, UML-diagram, informationsflöde, organisationsdiagram, programvarudiagram, nätverkslayout, databasmodeller, objektkartläggning och annan liknande information. Filer som genereras med Visio kan också exporteras till olika filformat som [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra.

## Filformat ##

VSDX-filer är baserade på Open Packaging Conventions och XML och utvecklare kan dra nytta av detta format genom att lära sig hur man arbetar med dessa filer programmatiskt. Formatet ärver många av samma XML-strukturer som dess delar från filformatet Visio XML Drawing (.vdx). Interoperabiliteten med Visio-filer ökar avsevärt eftersom programvara från tredje part kan manipulera Visio-filer på filformatsnivå.

Vissa andra filtyper som utgör filformatet Visio 2013 inkluderar:

* .vsdm (Visio makroaktiverad ritning)
* .vssx (Visio stencil)
* .vssm (Visio makroaktiverad stencil)
* .vstx (Visio-mall)
* .vstm (Visio makroaktiverad mall)

Under huven använder Visio 2013-filformatet ett strukturerat sätt att lagra applikationsdata tillsammans med relaterade resurser i ett arkiv som [ZIP](/sv/compression/zip/). ZIP-filen kan extraheras med vilket standardextraktionsverktyg som helst där den också innehåller andra typer av filer. Du kan bara ersätta .vsdx-filtillägget med .zip i Windows Explorer för att se innehållet i VSDX-filen.

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations" delar.

### Dokument ###

Dokumentdelarna innehåller det faktiska innehållet och metadata för Visio-filen, som namnet på filen, den första sidan och alla former som den innehåller, och till och med dataanslutningarna för formerna. Bilder och textfiler i paketet betraktas som dokumentdelar.

### Relationer ###

Relationsdelarna i en Visio-fil lagras i mappen "\_rels" och beskriver hur delarna i paketet är relaterade till var och en. Det ger också filens struktur. Ett fristående XML-dokument använder elementets överordnade/underordnade relation för att bestämma förhållandet mellan enheter och varandra. Ett giltigt Visio 2013-filformat innehåller rätt uppsättning delar och paketet innehåller relationerna mellan delarna.

Relationsdelar är XML-dokument som beskriver relationerna mellan olika dokumentdelar inom paketet. De definierar en koppling mellan två objekt: en specificerad källa (definierad av namnet och platsen för relationsfilen) och en specificerad måldokumentdel. Till exempel används relationsdelar för att beskriva vilka formmaster som är associerade med filen, hur sidor relaterar till filen och till varandra, eller hur bilder och objekt relaterar till en specifik sida.

## Referenser ##

* [Introduktion till Visio-filformat](https://docs.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

