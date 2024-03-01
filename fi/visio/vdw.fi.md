{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW - Visio Graphics Service -tiedostomuoto",
  "description":"Opi VDW-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VDW-tiedostoja.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-fi",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Mikä on VDW-tiedosto?

VDW on Visio Graphics Service -tiedostomuoto, joka määrittää verkkopiirustuksen hahmontamiseen tarvittavat virrat ja tallennustilat. Verkkopiirustus on kokoelma piirustussivuja, muotoja, fontteja, kuvia, tietoyhteyksiä ja kaaviopäivitystietoja, jotka voidaan renderöidä vektori- tai rasteripiirroksina. VDW-tiedostoja voidaan avata myös Microsoft Visiossa, mutta ne tallennetaan ensisijaisesti verkkokäyttöä varten. Microsoft Visio tarjoaa mahdollisuuden muuntaa Visio-tiedostoja useisiin eri tiedostomuotoihin, mukaan lukien [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ja muut.

## **VDW** tiedostomuoto

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|!{{HYPERLINKKI1}}

## Viitteet

* [[MS-VGSFF]: Visio Graphics Service (.vdw) -tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


