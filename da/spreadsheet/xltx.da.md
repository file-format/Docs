{
  "date": "2019-12-10",
  "keywords": [
"XLTX",
"fil",
"udvidelse",
"filformat",
"Excel åben XML",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en XLTX-fil og API'er er, der kan oprette og åbne dem.",
  "title": "Hvad er en XLTX fil?",
  "linktitle": "XLTX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-dax"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en XLTX fil?

Filer med filtypenavnet .xltx repræsenterer Microsoft Excel-skabelonfiler, der er baseret på Office OpenXML-filformatspecifikationerne. Den bruges til at oprette en standard skabelonfil, der kan bruges til at generere [XLSX](/spreadsheet/xlsx/) filer, der udviser de samme indstillinger som angivet i XLTX-filen.

## Kort historie

Det var i begyndelsen af 2000, da Microsoft besluttede at gå efter ændringen for at imødekomme standarden for **Office Open XML**. Dokumenter af forskellige typer under denne nye standard blev identificeret ved at tilføje X i deres udvidelser, hvor X er for XML. I 2007 blev dette nye filformat en del af Office 2007 og videreføres også i de nye versioner af Microsoft Office. Den nye filtype har tilføjet fordele ved små filstørrelser, færre ændringer af korruption og velformaterede billeder.

## XLTX filformatspecifikationer

XLTX-filer er baseret på Office OpenXML-filformatet og bruger XML og [ZIP](/compression/zip/) til at reducere filstørrelsen. Det blev oprettet med udgivelsen af Microsoft Office 2007 for at erstatte det binære XLT-filformat. I lighed med XLTX kan XLT-filformatet bruges til at oprette [XLS](/spreadsheet/xls/)-filer ved hjælp af Microsoft Excel 2003 og 2007. Disse kan åbnes med Microsoft Excel ved at dobbeltklikke på filen. Filorganisationen i et XLTX-filformat kan observeres ved at omdøbe filen til ZIP og derefter udpakke dens indhold til disk.

### [Content_Types].xml ###

Dette er den eneste fil, der findes på basisniveauet, når zip-filen udpakkes. Den viser indholdstyperne for dele i pakken. Alle referencer til XML-filerne inkluderet i pakken er refereret i denne XML-fil.

### \_rels (mappe) ###

Dette er mappen Relationer, der indeholder en enkelt XML-fil, der gemmer relationerne på pakkeniveau. Links til de vigtigste dele af Xltx-filerne er indeholdt i denne fil som URI'er. Disse URI'er identificerer typen af relation mellem hver nøgledel til pakken. Dette inkluderer forholdet til det primære Office-dokument placeret som xl/workbook.xml og andre dele i docProps som kerne og udvidede egenskaber.

### docProps ###

Denne mappe indeholder de overordnede dokumentegenskaber. Disse omfatter et sæt kerneegenskaber, et sæt udvidede eller applikationsspecifikke egenskaber og et miniaturebillede af dokumentet. En tom projektmappe har to filer i denne mappe, nemlig app.xml og core.xml. Core.xml indeholder oplysninger som forfatter, dato oprettet og gemt og ændret. App.xml indeholder information om indholdet af filen.

### xl (mappe) ###

Dette er hovedmappen, der indeholder alle detaljer om indholdet af projektmappen. Som standard har den følgende mapper:

* \_rels

* tema

* arbejdsark


og følgende xml-filer:

* styles.xml

* arbejdsbog.xml


## Referencer ##

* [[MS-XLSX] - .Xlsx filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


