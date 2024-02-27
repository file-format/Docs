{
  "date": "2019-10-11",
  "keywords": [
"wmf fil",
"wmf filformat",
"hvad er en wmf-fil",
"fil",
"wmf eksempel",
"wmf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMF - Microsoft Windows Metafil Format",
  "description": "Lær om WMF filformat og API'er, der kan oprette og åbne WMF filer.",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er WMF fil?

Filer med WMF-udvidelse repræsenterer Microsoft Windows Metafile (WMF) til lagring af vektor- såvel som bitmap-format billeddata. For at være mere præcis hører WMF til vektorfilformatkategorien af grafikfilformater, der er enhedsuafhængig. Windows Graphical Device Interface (GDI) bruger de funktioner, der er gemt i en WMF-fil, til at vise et billede på skærmen. En mere forbedret version af WMF, kendt som Enhanced Meta Files (EMF), blev udgivet senere, hvilket gør formatet mere funktionsrigt. Praktisk talt ligner WMF SVG.

## WMF filformatspecifikationer ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. Filformatet består af en række poster med variabel længde, der indeholder grafiktegningskommandoer, objektdefinitioner og egenskaber. Da WMF-filer er baseret på kommandoer gengivet til GDI'en til at tegne billedet, er det også kendt som en digital optagelse af billedet, som kan afspilles for at gengive billedet. De komplette filformatspecifikationer for WMF er tilgængelige online og bør henvises til udvikling af applikationer til at arbejde med WMF-filer. En WMF-fil er organiseret i en:

* WMF Header Record

* WMF Record(s)

* WMF End-of-File Record


### WMF Header Record ###

**META_HEADER Record** indeholder oplysninger, der definerer metafilens karakteristika, herunder:

* Metafilens type

* Versionen af metafilen

* Størrelsen af metafilen

* Antallet af objekter defineret i metafilen

* Størrelsen af den største enkeltpost i metafilen


### WMF Placerbar Header Record ###

**META_PLACEABLE Record** indeholder udvidede oplysninger om billedet, herunder:

* Et afgrænsende rektangel

* Logisk enhedsstørrelse, til skalering

* En kontrolsum til validering


### WMF Record ###

WMF-poster har et generisk format, som er specificeret i specifikationsdokumentet. Hver WMF-post indeholder følgende information:

* Rekordstørrelsen

* Optagefunktionen

* Eventuelle parametre for registreringsfunktionen


## Referencer ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)


