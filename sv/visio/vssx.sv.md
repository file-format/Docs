{
  "date" : "2019-10-11",
  "keywords" :[ "vssx fil", "vssx filformat", "vad är en vssx fil", "fil", "vssx exempel", "vssx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSX - Visio Stencil File Format",
  "description":"Läs mer om VSSX-filformat och API:er som kan skapa och öppna VSSX-filer.",
  "linktitle" : "VSSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssx",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en VSSX fil?

Filer med tillägget .vssx är ritstenciler skapade med [Microsoft Visio](https://products.office.com/en/visio/flowchart-software) 2013 och senare. VSSX-filformatet kan öppnas med Visio 2013 och högre. Visio-filer är kända för representation av en mängd ritningselement såsom samling av former, kopplingar, flödesscheman, nätverkslayout, UML-diagram, programvarudiagram, databasmodeller, objektkartläggning och annan liknande information. Microsoft Visio ger också möjlighet att konvertera Visio-filer till olika filformat såsom [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra. Den är tillgänglig för både Windows och Mac OS.

## VSSX filformat

VSSX-filformatet är baserat på OpenOffice-formatet som antagits av Microsoft sedan 2007. Det är baserat på [ZIP](/sv/compression/zip/)-arkivet som representerar det övergripande filformatet baserat på XML-filformatspecifikationer. Det binära filformatets motsvarighet till VSSX var VSS som stöddes fram till Visio 2007. Du kan se innehållet i VSSX-filformatet genom att ersätta dess tillägg med .ZIP och öppna i valfritt arkiveringsfilformat som WinZIP.

VSDX-filer är baserade på Open Packaging Conventions och XML och utvecklare kan dra nytta av detta format genom att lära sig hur man arbetar med dessa filer programmatiskt. Formatet ärver många av samma XML-strukturer som dess delar från filformatet Visio XML Drawing (.vdx). Interoperabiliteten med Visio-filer ökar avsevärt eftersom programvara från tredje part kan manipulera Visio-filer på filformatsnivå.

Vissa andra filtyper som utgör filformatet Visio 2013 inkluderar:

* .vsdm (Visio makroaktiverad ritning)
* .vssx (Visio stencil)
* .vssm (Visio makroaktiverad stencil)
* .vstx (Visio-mall)
* .vstm (Visio makroaktiverad mall)

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations" delar.

## Referenser ##

* [Introduktion till Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)
* [Schemakarta - Visio XML](https://learn.microsoft.com/en-us/office/client-developer/visio/schema-mapvisio-xml)

