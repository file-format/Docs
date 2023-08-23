{
  "date" : "2019-10-11",
  "keywords" :[ "vssm-fil", "vssm-filformat", "vad är en vssm-fil", "fil", "vssm-exempel", "vssm-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSSM - Microsoft Visio Macro Enabled File Format",
  "description":"Läs mer om VSSM-filformat och API:er som kan skapa och öppna VSSM-filer.",
  "linktitle" : "VSSM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vssm",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är VSSM fil?

Filer med filtillägget .vssm är Microsoft Visio Stencil-filer som stöder ger stöd för makron. En VSSM-fil när den öppnas gör det möjligt att köra makron för att uppnå önskad formatering och placering av former i ett diagram. I allmänhet är Microsoft Visio ritprogram som gör det möjligt att skapa filer som kan innehålla och representera användardefinierad information i olika former. De vanligaste av dessa inkluderar, men inte begränsat till, UML-diagram, flödesscheman, visuella objekt, informationsflöde, organisationsdiagram, programvarudiagram, nätverkslayout, databasmodeller, objektkartläggning och annan liknande information. Filer som genereras med Visio kan också konverteras till olika filformat såsom [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra.

## VSSM filformat

VSSM-filformatet introducerades med Microsoft Visio 2013 som är baserat på OpenOffice XML-specifikationerna. Vissa andra filtyper som utgör filformatet Visio 2013 inkluderar:

* .vsdm (Visio makroaktiverad ritning)
* .vssx (Visio stencil)
* .vssm (Visio makroaktiverad stencil)
* .vstx (Visio-mall)
* .vstm (Visio makroaktiverad mall)

Under huven använder Visio 2013-filformatet ett strukturerat sätt att lagra applikationsdata tillsammans med relaterade resurser i ett arkiv som [ZIP](/sv/compression/zip/). ZIP-filen kan extraheras med vilket standardextraktionsverktyg som helst där den också innehåller andra typer av filer.

Varje Visio-fil kallas paket som innehåller andra filer eller delar. En paketdel kan vara en XML-fil, en bild eller till och med en VBA-lösning. Delarna i paketet kan delas upp i "dokument" och "relations"-delar.

## Referenser ##

* [Introduktion till Visio-filformat](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)

