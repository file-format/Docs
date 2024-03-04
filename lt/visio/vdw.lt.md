{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW – „Visio Graphics Service“ failo formatas",
  "description":"Sužinokite apie VDW failo formatą ir API, kurios gali kurti ir atidaryti VDW failus.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-lt",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Kas yra VDW failas?

VDW yra Visio Graphics Service failo formatas, nurodantis srautus ir saugyklas, reikalingas žiniatinklio brėžiniui pateikti. Žiniatinklio brėžinys yra piešimo puslapių, formų, šriftų, vaizdų, duomenų jungčių ir diagramos atnaujinimo informacijos rinkinys, kurį galima pateikti kaip vektorinį arba rastrinį piešinį. VDW failus taip pat galima atidaryti Microsoft Visio, bet pirmiausia jie išsaugomi naudoti žiniatinklyje. Microsoft Visio siūlo galimybę konvertuoti Visio failus į įvairius failų formatus, įskaitant [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ir kitus.

## **VDW** failo formatas

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|![Possible Implementation of a File](/web/vdw.png "Possible Implementation of a File")

## Nuorodos

* [[MS-VGSFF]: „Visio Graphics Service“ (.vdw) failo formatas](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


