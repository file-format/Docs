{
  "date" : "2019-10-11",
  "keywords" :[ "wmf-fil", "wmf-filformat", "vad är en wmf-fil", "fil", "wmf-exempel", "wmf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafil Format",
  "description":"Läs mer om WMF-filformat och API:er som kan skapa och öppna WMF-filer.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är WMF fil?

Filer med WMF-tillägg representerar Microsoft Windows Metafile (WMF) för lagring av vektor- och bitmappsformat bilddata. För att vara mer exakt tillhör WMF kategorin vektorfilformat för grafikfilformat som är enhetsoberoende. Windows Graphical Device Interface (GDI) använder funktionerna som är lagrade i en WMF-fil för att visa en bild på skärmen. En mer förbättrad version av WMF, känd som Enhanced Meta Files (EMF), publicerades senare som gör formatet mer funktionsrikt. Praktiskt taget liknar WMF SVG.

## WMF filformatspecifikationer ##

En WMF-fil hänvisade till 16-bitars filformat vid tidpunkten för dess lansering med Windows 3.0. Filformatet består av en serie poster med variabel längd som innehåller grafikritningskommandon, objektdefinitioner och egenskaper. Eftersom WMF-filer är baserade på kommandon som återges till GDI för att rita bilden, är det också känt som en digital inspelning av bilden som kan spelas upp för att återge den bilden. De fullständiga filformatspecifikationerna för WMF finns tillgängliga online och bör hänvisas till för utveckling av applikationer för att fungera med WMF-filer. En WMF-fil är organiserad i en:

* WMF Header Record
* WMF Record(s)
* WMF End-of-File Record

### WMF Header Record ###

**META_HEADER-posten** innehåller information som definierar metafilens egenskaper, inklusive:

* Typen av metafil
* Versionen av metafilen
* Storleken på metafilen
* Antalet objekt som definieras i metafilen
* Storleken på den största enskilda posten i metafilen

### WMF Placeable Header Record ###

**META_PLACEABLE Record** innehåller utökad information om bilden, inklusive:

* En avgränsande rektangel
* Logisk enhetsstorlek, för skalning
* En kontrollsumma, för validering

### WMF Record ###

WMF-poster har ett generiskt format, vilket anges i specifikationsdokumentet. Varje WMF-post innehåller följande information:

* Rekordstorleken
* Inspelningsfunktionen
* Eventuella parametrar för inspelningsfunktionen

## Referenser ##

* [[MS-WMF]: Windows metafilformat](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

