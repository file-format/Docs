{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "vdw-fil", "vdw-filformat", "vdw-filtyp", "fil", "typ", "vad är en vdw-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio Graphics Service File Format",
  "description":"Läs mer om VDW-filformat och API:er som kan skapa och öppna VDW-filer.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Vad är VDW fil?

VDW är filformatet Visio Graphics Service som anger de strömmar och lagringar som krävs för att rendera en webbritning. En webbritning är en samling ritsidor, former, typsnitt, bilder, dataanslutningar och diagramuppdateringsinformation som kan renderas som en vektor- eller rasterritning. VDW-filer kan också öppnas i Microsoft Visio men sparas i första hand för användning på webben. Microsoft Visio erbjuder möjligheten att konvertera Visio-filer till ett antal olika filformat inklusive [PNG](/sv/image/png/), [BMP](/sv/image/bmp/), [PDF](/sv/pdf/) och andra.

## **VDW** Filformat

De tekniska specifikationerna för VDW-filformat är tillgängliga online av [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) och kan refereras av utvecklare för att skapa applikationer. Det tekniska dokumentet beskriver data som finns i en sammansatt fil som innehåller lagringar och strömmar. Representationen av en webbritning är möjlig genom en ström, som heter VisioServerData, via ett ZIP-arkiv. En ShapGraphic XML-del i arkivet beskriver de grafiska elementen som visas i webbritningen och uttrycks i Extensible Application Markup Language (XAML). En samling XML-delar i ZIP-arkivet beskriver webbritningens dataanslutning, information om dess form och diagramuppdateringslogiken. Dessa delar uttrycks som XML. DataGraphic XML-delen beskriver omräknade egenskaper som ska utvärderas efter att data i webbritningen har uppdaterats från datakällan. Ytterligare objekt i ZIP-arkivet innehåller information om typsnitt och bilder som används i webbritningen.

|![Möjlig implementering av en fil](/sv/web/vdw.png "Möjlig implementering av en fil")

## Referenser

* [[MS-VGSFF]: Visio Graphics Service (.vdw) filformat](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

