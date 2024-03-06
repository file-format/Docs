{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW — Visio Graphics Service faila formāts",
  "description":"Uzziniet par VDW failu formātu un API, kas var izveidot un atvērt VDW failus.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-lv",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Kas ir VDW fails?

VDW ir Visio Graphics Service faila formāts, kas nosaka straumes un krātuves, kas nepieciešamas tīmekļa zīmējuma renderēšanai. Tīmekļa zīmējums ir zīmējumu lapu, formu, fontu, attēlu, datu savienojumu un diagrammas atjaunināšanas informācijas kolekcija, ko var atveidot kā vektora vai rastra zīmējumu. VDW failus var atvērt arī programmā Microsoft Visio, taču tie galvenokārt tiek saglabāti lietošanai tīmeklī. Microsoft Visio piedāvā iespēju pārveidot Visio failus dažādos failu formātos, tostarp [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) un citos.

## **VDW** faila formāts

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|!{{HIPERSAITE1}}

## Atsauces

* [[MS-VGSFF]: Visio Graphics Service (.vdw) faila formāts](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


