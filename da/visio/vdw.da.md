{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW - Visio Graphics Service File Format",
  "description":"Lær om VDW-filformat og API'er, der kan oprette og åbne VDW-filer.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-da",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Hvad er en VDW fil?

VDW er Visio Graphics Service-filformatet, der specificerer de streams og lager, der kræves for at gengive en web-tegning. En webtegning er en samling af tegningssider, figurer, skrifttyper, billeder, dataforbindelser og diagramopdateringsoplysninger, der kan gengives som en vektor- eller rastertegning. VDW-filer kan også åbnes i Microsoft Visio, men gemmes primært til brug på nettet. Microsoft Visio tilbyder muligheden for at konvertere Visio-filer til en række forskellige filformater, herunder [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) og andre.

## **VDW** Filformat

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|![Possible Implementation of a File](/web/vdw.png "Possible Implementation of a File")

## Referencer

* [[MS-VGSFF]: Visio Graphics Service (.vdw) filformat](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


