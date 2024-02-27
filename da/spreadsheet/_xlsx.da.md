{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en _XLSX-fil og API'er er, der kan oprette og åbne _XLSX-filer.",
  "title": "Hvad er en _XLSX fil?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-dax"
}
},
  "lastmod": "2021-11-22"
}

## Hvad er en _XLSX fil?

En fil med filtypen .\_xlsx er faktisk en [XLSX](/spreadsheet/xlsx/) fil, der er omdøbt af et andet program. Dette kan ske i visse tilfælde, når filnavnet indeholder en . i slutningen af filnavnet. \_XLSX-filerne kan åbnes i Microsoft Excel svarende til XLSX-filerne ved igen at omdøbe disse til .xlsx-udvidelsen.

## _XLSX filformat - Flere oplysninger

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Før XLSX var [XLS](/spreadsheet/xls/) det primære filformat, der blev brugt til at arbejde med Excel-regneark til at gemme dokumenter i binært format. Dette nye XML-baserede filformat kom med fordele såsom små filstørrelser, modstand mod filkorruption og velformaterede billeder. Dette nye XML-baserede filformat blev en del af Office 2007 og udføres også i de nye versioner af Microsoft.

## \_XLSX filformatspecifikationer

Da en \_XLSX-fil er en XLSX-fil omdøbt, har den samme specifikationer som den originale fil. Det er kun en arkivfil, der er baseret på arkivfilformatet [ZIP](/compression/zip/). Hvis du vil se indholdet af dette arkiv, skal du blot omdøbe filen til .zip-udvidelsen og udpakke den for at se bestandsfilerne i denne Excel-projektmappe. En tom projektmappe, når den udpakkes til dens filer, har følgende bestanddel af filer og mapper.

### [Content_Types].xml

Dette er den eneste fil, der findes på basisniveauet, når zip-filen udpakkes. Den viser indholdstyperne for dele i pakken. Alle referencer til XML-filerne inkluderet i pakken er refereret i denne XML-fil.

### \_rels (mappe)

Dette er mappen Relationer, der indeholder en enkelt XML-fil, der gemmer relationerne på pakkeniveau. Links til de vigtigste dele af Xlsx-filerne er indeholdt i denne fil som URI'er. Disse URI'er identificerer typen af relation mellem hver nøgledel til pakken. Dette inkluderer forholdet til det primære kontordokument placeret som xl/workbook.xml og andre dele i docProps som kerneegenskaber og udvidede egenskaber.

### docProps

Denne mappe indeholder de overordnede dokumentegenskaber. Disse omfatter et sæt kerneegenskaber, et sæt udvidede eller applikationsspecifikke egenskaber og et miniaturebillede af dokumentet. En tom projektmappe har to filer i denne mappe, nemlig app.xml og core.xml. Core.xml indeholder oplysninger som forfatter, dato oprettet og gemt og ændret. App.xml indeholder information om indholdet af filen.

### xl (mappe)

Dette er hovedmappen, der indeholder alle detaljer om indholdet af projektmappen. Som standard har den følgende mapper:

* \_rels

* tema

* arbejdsark


og følgende xml-filer:

* styles.xml

* arbejdsbog.xml


## Referencer

* [MS-XLSX - .xlsx filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


