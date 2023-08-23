{
  "date" : "2019-10-11",
  "keywords" :[ "vstx fil", "vstx filformat", "vad är en vstx fil", "fil", "vstx exempel", "vstx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSTX - Microsoft Visio-filformat",
  "description":"Läs mer om VSTX-filformat och API:er som kan skapa och öppna VSTX-filer.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VSTX fil?

Filer med .vstx-tillägg är ritmallsfiler skapade med Microsoft Visio 2013 och senare. Dessa VSTX-filer ger en startpunkt för att skapa Visio-ritningar, sparade som [.VSDX](/sv/image/vsdx/)-filer, med standardlayout och inställningar. I allmänhet används Visio-filer för att skapa ritningar som innehåller visuella objekt, flödesscheman, UML-diagram, informationsflöde, organisationsdiagram, programvarudiagram, nätverkslayout, databasmodeller, objektkartläggning och annan liknande information. Filer som genereras med Visio kan också exporteras till olika filformat som [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra. Program som öppnar VSTX-filer inkluderar Microsoft Visio för Windows och Mac som låter dig öppna dessa filer för visning och redigering. Det gör det också möjligt att konvertera Visio-filformat till ett antal andra format.

# VSTX-filformat #

"X" i filtillägget hänvisar till OpenOffice-filformatet som introducerades av Microsoft som ett [ZIP](/sv/compression/zip/) arkivfilformat för ersättning av binära filformat som stöddes tidigare. VSTX-filer är därför baserade på XML-filformatet i OpenOffice-specifikationerna till skillnad från filformatet [.VST](/sv/image/vst/) som är i binärt format.

VSDX-filer är baserade på Open Packaging Conventions och XML och utvecklare kan dra nytta av detta format genom att lära sig hur man arbetar med dessa filer programmatiskt. Formatet ärver många av samma XML-strukturer som dess delar från Visio XML Drawing-filformatet (.vdx). Interoperabiliteten med Visio-filer ökar avsevärt eftersom programvara från tredje part kan manipulera Visio-filer på filformatsnivå.

Vissa andra filtyper som utgör filformatet Visio 2013 inkluderar:

* .vsdm (Visio makroaktiverad ritning)
* .vssx (Visio stencil)
* .vssm (Visio makroaktiverad stencil)
* .vstx (Visio-mall)
* .vstm (Visio makroaktiverad mall)

Under huven använder Visio 2013-filformatet ett strukturerat sätt att lagra applikationsdata tillsammans med relaterade resurser i ett arkiv som [ZIP](/sv/compression/zip/). ZIP-filen kan extraheras med vilket standardextraktionsverktyg som helst där den också innehåller andra typer av filer. Du kan bara ersätta .VSTX-filtillägget med .ZIP i Windows Explorer för att se innehållet i VSTX-filen.

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations" delar.

### Dokument ###

Dokumentdelarna innehåller det faktiska innehållet och metadata för Visio-filen, som namnet på filen, den första sidan och alla former som den innehåller, och till och med dataanslutningarna för formerna. Bilder och textfiler i paketet betraktas som dokumentdelar.

### Relationer ###

Relationsdelarna i en Visio-fil lagras i mappen "_rels" och beskriver hur delarna i paketet är relaterade till var och en. Det ger också filens struktur. Ett fristående XML-dokument använder elementets överordnade/underordnade relation för att bestämma förhållandet mellan enheter och varandra. Ett giltigt Visio 2013-filformat innehåller rätt uppsättning delar och paketet innehåller relationerna mellan delarna.

Relationsdelar är XML-dokument som beskriver relationerna mellan olika dokumentdelar inom paketet. De definierar en koppling mellan två objekt: en specificerad källa (definierad av namnet och platsen för relationsfilen) och en specificerad måldokumentdel. Till exempel används relationsdelar för att beskriva vilka formmaster som är associerade med filen, hur sidor relaterar till filen och till varandra, eller hur bilder och objekt relaterar till en specifik sida.

## Referenser ##

* [Introduktion till Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

