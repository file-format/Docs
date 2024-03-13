{
  "date" : "2019-10-11",
  "keywords" : [ "vdw","vdw file", "vdw file format", "vdw file type", "file", "type", "what is an vdw file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VDW - Visio Graphics Service File Format",
  "description":"VDW faylları yarada və aça bilən VDW fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw-az",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## VDW faylı nədir?

VDW, Veb rəsmini göstərmək üçün tələb olunan axınları və yaddaşları təyin edən Visio Qrafik Xidməti fayl formatıdır. Veb-rəsm vektor və ya rastr rəsm kimi göstərilə bilən rəsm səhifələrinin, formaların, şriftlərin, şəkillərin, məlumat əlaqələrinin və diaqram yeniləmə məlumatlarının toplusudur. VDW faylları Microsoft Visio-da da açıla bilər, lakin əsasən internetdə istifadə üçün saxlanılır. Microsoft Visio Visio fayllarını [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) və başqaları daxil olmaqla bir sıra müxtəlif fayl formatlarına çevirmək imkanı təklif edir.

## **VDW** Fayl Formatı

The technical specifications of VDW file format are available online by [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) and can be referenced by developers for creating applications. The technical document describes data contained in a compound file which contains storages and streams. The representation of a Web Drawing is made possible through a stream, named VisioServerData, via a ZIP archive. A ShapGraphic XML Part in the archive describes the graphical elements displayed in the Web drawing and are expressed in Extensible Application Markup Language (XAML). A collection of XML parts in the ZIP archive describes the Web drawing's data connection, information about its shape and the diagram update logic. These parts are expressed as XML. The DataGraphic XML part describes recalculated properties that are to be evaluated after the data in the Web drawing has been refreshed from the data source. Additional items in the ZIP archive contain information for the fonts and images used in the Web drawing.

|![Possible Implementation of a File](/web/vdw.png "Possible Implementation of a File")

## İstinadlar

* [[MS-VGSFF]: Visio Graphics Service (.vdw) Fayl Format](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)


