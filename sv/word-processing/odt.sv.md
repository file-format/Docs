{
  "date" : "2019-10-11",
  "keywords" :[ "odt-fil", "odt-filformat", "vad är en odt-fil", "fil", "odt-exempel", "odt-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - OpenDocument Text File",
  "description":"Läs mer om ODT-filformat och API:er som kan skapa och öppna ODT-filer.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en ODT fil?

ODT-filer är typ av dokument skapade med ordbehandlingsprogram som är baserade på OpenDocument Text File-format. Dessa skapas med ordbehandlingsprogram som gratis OpenOffice Writer och kan innehålla innehåll som text, bilder, objekt och stilar. ODT-filen är för Writers ordbehandlare vad [DOCX](/sv/ord-behandling/docx/) är för Microsoft Word. Flera applikationer inklusive Google Docs och Googles webbaserade ordbehandlare som ingår i Google Drive kan öppna ODT-filerna för redigering. Microsoft Word kan också öppna ODT-filer och spara dem i andra format som [DOC](/sv/ordbehandling/doc/) och DOCX.

## Kortfattad bakgrund ##

ODP-filformatspecifikationer baseras på standarden som utvecklats som ODF-specifikationer. Dessa specifikationer har utvecklats under tidigare i form av tre versioner utvecklade och publicerade av OASIS enligt följande:

**2005** Version 1.0 publicerades i maj 2005

**2007:** Version 1.1 publicerades i februari 2007

**2011:** Version 1.2 publicerades i september 2011

Det var ganska små förändringar i övergången från ODF 1.0 till 1.1 versioner. [ODF 1.2-versionen](https://www.oasis-open.org/standards#opendocumentv1.2) är den senaste versionen för ODF-specifikationer och bör konsulteras av utvecklare för utveckling av applikationer relaterade till ODS-läsning/skrivning.

## Filformatspecifikationer ##

OpenDocument-formatet stöder dokumentrepresentation som ett enda XML-dokument samt en samling av flera underdokument i ett paket som [ZIP](/sv/compression/zip/)-arkiv. Var och en av filerna från ZIP-arkivet lagrar en del av det fullständiga dokumentet. Varje underdokument lagrar en viss aspekt av dokumentet. Till exempel innehåller ett underdokument stilinformationen och ett annat underdokument innehåller dokumentets innehåll. Ett typiskt ODF-dokument har följande komponenter:

* content.xml – Dokumentinnehåll och automatiska stilar som används i innehållet.
* styles.xml – Stilar som används i dokumentinnehållet och automatiska stilar som används i själva stilarna.
* meta.xml – Dokumentmetainformation, såsom författaren eller tidpunkten för den senaste lagringsåtgärden.
* settings.xml – Programspecifika inställningar, såsom fönsterstorlek eller skrivarinformation.

Förutom dessa kan i paketet finnas många andra underdokument som dokumentminiatyrbilder, bilder etc. Dokumentfiler är en delmängd av ODF-filer där innehållet (ark) lagras i //content.xml// underdokument.

## Referenser ##

* [OpenDocument - Av Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

