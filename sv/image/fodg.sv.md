{
  "date" : "2019-10-11",
  "keywords" :[ "fodg fil", "fodg filformat", "vad är en fodg fil", "fil", "fodg exempel", "fodg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FODG - OpenDocument Drawing File Format",
  "description":"Läs mer om FODG-filformat och API:er som kan skapa och öppna FODG-filer.",
  "linktitle" : "FODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är FODG fil?

En fil med filtillägget .fodg är ett Apache OpenOffice Drawing-filformat för att lagra ritelement. Den är baserad på filformatspecifikationerna som beskrivs av Advancement of Structural Information Standards (OASIS). Ett annat liknande filformat för OpenOffice-grafik är [ODG](/sv/image/odg/) som lagrar ritelement som en vektorbild. FODG-filer kan öppnas med OpenOffice såväl som LibreOffice. Andra filformat som stöds av OpenOffice, till exempel, inkluderar [ODT](/sv/ordbehandling/odt/), ODF, [ODP](/sv/presentation/odp/) och [ODS](/sv/spreadsheet/ods/).

## FODG filformat

FODG är baserat på OpenDocuments XML-filformat som överensstämmer med OASIS OpenDocument Format ISO/IEC 26300. Det har Internet Media Type application/vnd.oasis.opendocument.graphics och överensstämmer även med org.oasis-open.opendocument public.composite-content . XML-strukturen är gemensam för alla dokumenttyper som kalkylblad, ritfiler och textdokument. OpenOffice-dokument drar fördel av separation av problem genom att separera innehåll, stilar, metadata och programinställningar i fyra separata XML-filer.

`<office:document-content> ` - Dokumentinnehåll och automatiska stilar som används i innehållet.
`<office:document-styles> ` - Stilar som används i dokumentinnehållet och automatiska stilar som används i själva stilarna.
`<office:document-meta> ` - Dokumentmetainformation, såsom författaren eller tidpunkten för den senaste sparande åtgärden.
`<office:document-settings> ` - Programspecifika inställningar, såsom fönsterstorlek eller skrivarinformation.

## Referenser ##
* [Framtida specifikationer för v 1.3 standardisering ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

