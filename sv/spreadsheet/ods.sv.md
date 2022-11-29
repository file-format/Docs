{
  "date" : "2019-12-10",
  "keywords" :[ "ODS", "fil", "tillägg", "filformat", "OpenDocument Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en ODS-fil och API:er är som kan skapa och öppna dem.",
  "title" :"Vad är en ODS-fil?",
  "linktitle" : "ODS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är ODS fil?

Filer med tillägget .ods står för OpenDocument Spreadsheet Document-format som kan redigeras av användaren. Data lagras i ODF-filen i rader och kolumner. Det är XML-baserat format och är en av flera undertyper i familjen Open Document Formats (ODF). Formatet specificeras som en del av ODF 1.2-specifikationerna som publiceras och underhålls av OASIS. Ett antal applikationer på Windows såväl som andra operativsystem kan öppna ODS-filer för redigering och manipulering, inklusive Microsoft Excel, NeoOffice och LibreOffice. ODS-filer kan också konverteras till andra kalkylbladsformat liksom [XLS](/sv/spreadsheet/xls/), [XLSX](/sv/spreadsheet/xlsx/) och andra av olika applikationer.

## Kortfattad bakgrund ##

ODS filformatspecifikationer är baserade på standarden utvecklad som ODF-specifikationer. Dessa specifikationer har utvecklats under tidigare i form av tre versioner utvecklade och publicerade av OASIS enligt följande:

`2005`- Version 1.0 publicerades i maj 2005

`2007` - Version 1.1 publicerades i februari 2007

`2011` - Version 1.2 publicerades i september 2011

Det var ganska små förändringar i övergången från ODF 1.0 till 1.1 versioner. [ODF 1.2-versionen](https://www.oasis-open.org/standards#opendocumentv1.2) är den senaste versionen för ODF-specifikationer och bör konsulteras av utvecklare för utveckling av applikationer relaterade till ODS-läsning/skrivning.

## ODS-filformat ##

OpenDocument-formatet stöder dokumentrepresentation som ett enda XML-dokument samt en samling av flera underdokument i ett paket som [ZIP](/sv/compression/zip/)-arkiv. Var och en av filerna från ZIP-arkivet lagrar en del av det fullständiga dokumentet. Varje underdokument lagrar en viss aspekt av dokumentet. Till exempel innehåller ett underdokument stilinformationen och ett annat underdokument innehåller dokumentets innehåll. Ett typiskt ODF-dokument har följande komponenter:

* `content.xml` – Dokumentinnehåll och automatiska stilar som används i innehållet.
* `styles.xml` – Stilar som används i dokumentinnehållet och automatiska stilar som används i själva stilarna.
* `meta.xml` – Dokumentmetainformation, till exempel författaren eller tidpunkten för den senaste lagringsåtgärden.
* `settings.xml` – Programspecifika inställningar, såsom fönsterstorlek eller skrivarinformation.

Förutom dessa kan i paketet finnas många andra underdokument som dokumentminiatyrer, bilder etc.

Kalkylarksdokumentfiler är underuppsättningen av ODF-filer där innehållet (ark) lagras i underdokumentet content.xml.

## Referenser ##

* [OpenDocument - Av Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

