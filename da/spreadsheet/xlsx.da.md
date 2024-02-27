{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
"fil",
"udvidelse",
"filformat",
"Excel",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om, hvad en XLSX-fil og API'er er, der kan oprette og åbne XLSX-filer.",
  "title": "XLSX-filformat - Hvad er en XLSX-fil?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-dax"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en XLSX fil?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Baseret på struktur organiseret i henhold til Open Packaging-konventionerne som beskrevet i [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/) i OOXML-standarden ECMA-376, er det nye format en zip-pakke, der indeholder en række XML-filer. Den underliggende struktur og filer kan undersøges ved blot at udpakke .xlsx-filen.

## Kort historie om XLSX-filformat

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Før XLSX var det almindelige anvendte filformat [XLS](/spreadsheet/xls/), der var rent binært filformat. Den nye filtype har tilføjet fordele ved små filstørrelser, færre ændringer af korruption og velformaterede billeder. Det var i begyndelsen af 2000, da Microsoft besluttede at gå efter ændringen for at imødekomme standarden for **Office Open XML**. I 2007 blev dette nye filformat en del af Office 2007 og videreføres også i de nye versioner af Microsoft Office.

## XLSX filformatspecifikationer

De officielle [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) er tilgængelige online fra Microsoft. For at se, hvad der er inde i XLSX-filen, skal du blot omdøbe den til [ZIP](/compression/zip/)-filen ved at ændre dens udvidelse og derefter udpakke den for at se bestandsfilerne i denne Excel-projektmappe. En tom projektmappe, når den udpakkes til dens filer, har følgende bestanddel af filer og mapper.

### [Content_Types].xml ###

Dette er den eneste fil, der findes på basisniveauet, når zip-filen udpakkes. Den viser indholdstyperne for dele i pakken. Alle referencer til XML-filerne inkluderet i pakken er refereret i denne XML-fil.

### \_rels (mappe) ###

Dette er mappen Relationer, der indeholder en enkelt XML-fil, der gemmer relationerne på pakkeniveau. Links til de vigtigste dele af Xlsx-filerne er indeholdt i denne fil som URI'er. Disse URI'er identificerer typen af relation mellem hver nøgledel til pakken. Dette inkluderer forholdet til det primære kontordokument placeret som xl/workbook.xml og andre dele i docProps som kerneegenskaber og udvidede egenskaber.

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


## XLSX-formateksempel ##


For hvert Excel-regneark, der er indeholdt i en projektmappe, er der én XML-fil. Du kan finde disse XML-filer i mappen xl/arbejdsark. Alle oplysninger indeholdt i et regneark er organiseret i forskellige sektioner i XML-filen. Lad os undersøge et eksempel på et regneark fra en projektmappe, som er vist i det følgende billede.

{{< figure src="../XLSX file format.png" alt="XLSX filformat" >}}

Som det kan ses, indeholder dette regneark indhold i cellerne A1 til B2 og et billede. Derudover er celle G13 i øjeblikket den aktive celle i regnearket. Lad os nu undersøge filen xl/worksheets/sheet1.xml for at se, hvordan denne information er repræsenteret i XML-filen. Indholdet af denne XML-fil er som vist nedenfor.

{{< figure src="../XLSX File Format Details.png" alt="XPS filformat" >}}

1. Fanen har en temafarve påført. Det er nævnt i XML-filen med tag<tabColor> efter tema-id.
1. TabSelected-værdien er sat til 1, hvilket viser, at dette er det valgte ark
1. Som det kan ses på det første billede ovenfor, er celle G13 i regnearket aktiv celle, som også er nævnt i XML-filen.
1. SheetData-fanen repræsenterer de data, der er indeholdt i regnearket. Du kan dog se, at det originale indhold af regnearket ikke er nogen steder i dette afsnit. Dette skyldes, at teksten er indirekte henvist fra sharedStrings XML-ark. Denne sammenkædning sikrer, at hver tekst kun gemmes én gang og kan refereres igen for at spare plads.
1. Billedet, som det kan ses, er refereret med reference-id rId2

## Bidrage

Skal du dele noget om XLSX- eller Spreadsheet-filformater? Du kan sende dine resultater i afsnittet [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Referencer

* [[MS-XLSX] - XLSX-filformat](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


