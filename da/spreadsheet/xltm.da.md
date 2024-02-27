{
  "date": "2019-12-10",
  "keywords": [
"XLTM",
"fil",
"udvidelse",
"filformat",
"Excel Open XML Macro",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en XLTM-fil og API'er er, der kan oprette og åbne dem.",
  "title": "Hvad er en XLTM fil?",
  "linktitle": "XLTM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xlt-dam"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en XLTM fil?

XLTM filtypenavnet repræsenterer filer, der er genereret af Microsoft Excel som makroaktiverede skabelonfiler. XLTM-filer ligner [XLTX](/spreadsheet/xltx/) i struktur, bortset fra at de senere ikke understøtter oprettelse af skabelonfiler med makroer. Sådanne skabelonfiler bruges til at generere og indstille layout, formatering og andre indstillinger sammen med makroerne for at lette oprettelse af lignende XLSX-filer.

## Kort historie ##

Det var i begyndelsen af 2000, da Microsoft besluttede at gå efter ændringen for at imødekomme standarden for **Office Open XML**. Dokumenter af forskellige typer under denne nye standard blev identificeret ved at tilføje X i deres udvidelser, hvor X er for XML. I 2007 blev dette nye filformat en del af Office 2007 og videreføres også i de nye versioner af Microsoft Office. Den nye filtype har tilføjet fordele ved små filstørrelser, færre ændringer af korruption og velformaterede billeder.

## XLTM filformatspecifikationer ##

XLTM-filer er baseret på Office OpenXML-filformatet og bruger XML og [ZIP](/compression/zip/) til at reducere filstørrelsen. Disse kan åbnes med Microsoft Excel ved at dobbeltklikke på filen. Filorganisationen i et XLTM-filformat kan observeres ved at omdøbe filen til ZIP og derefter udpakke dens indhold til disk.

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

* [MS-XLSX filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


