{
  "date": "2019-12-16",
  "keywords": [
"XLS",
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
  "description": "Din filformatguide for at vide, hvad en XLS-fil og API'er er, der kan oprette og åbne dem.",
  "title": "Hvad er XLS filformat? Lær af filformateksperter!",
  "linktitle": "XLS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-das"
}
},
  "lastmod": "2019-12-16"
}

## Hvad er en XLS fil?

Files with XLS extension represent Excel Binary File Format. Such files can be created by Microsoft Excel as well as other similar spreadsheet programs such as OpenOffice Calc or Apple Numbers. File saved by Excel is known as Workbook where each workbook can have one or more worksheets. Data is stored and displayed to users in table format in worksheet and can span numeric values, text data, formulas, external data connections, images, and charts. Applications like Microsoft Excel lets you export workbook data to several different formats including [PDF](/pdf/), [CSV](/spreadsheet/csv/), [XLSX](/spreadsheet/xlsx/), [TXT](/word-processing/txt/), [HTML](/web/html/), [XPS](/page-description-language/xps/), and several others. The XLS file format was replaced with a more open and structured format, XLSX, with the release of Microsoft Excel 2007. The latest versions still provide support for creating and reading XLS files, though XLSX is the first choice of use now.

## Kort historie

XLS was created by Microsoft for use with Microsoft Excel and is also known as Binary Interchange File Format (BIFF). This file type was introduced for the first time by making it part of Excel for Windows in 1987. XLS file format specifications were made public for the first in June 2008 as Revision 1. After that, the specifications were continuously updated and the latest revision available is as of August 2018 that is marked as Revision 8.0. A brief history of different versions of XLS file format is as follow:

* Version 7.0 (released with office 95):  This version of excel was the most robust and faster among all the versions and internal stream rewrites were updated to 32 bits.
* Version 8 (frigivet med office 97): VBA blev introduceret som et standardsprog, og fjernede naturlige sprogetiketter blev indarbejdet i denne version for første gang. Det introducerede også en papirklip kontorassistent for første gang.

* Version 9 (udgivet med office 2000): Der var kun mindre ændringer i version 9, hvor papirclips kontorassistent samtidig kunne holde flere genstande, som ikke tidligere var mulige.

* Version 10 (udgivet med office XP): Denne version indeholdt ingen mærkbar forbedring.

* Version 11 (Released with office 2003): Major update in version 11, excel 2003 was the introduction of new tables.

## XLS-filformatspecifikationer ##

Data er arrangeret i en XLS-fil som binære strømme i form af en sammensat fil som beskrevet i [MS-CFB]. Data is stored in the compound file by using storages, streams, and substreams that contain information about the content and structure of a workbook, including workbook data such as worksheet definitions. Each stream or substream contains a series of binary records. Each binary record contains zero or more structured fields that contain the workbook data. This section gives a brief overview of XLS File Structure, but for detailed file format specifications, one must consult the [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx) dokument af Microsoft.

#### Stream og Substream ####

En projektmappe er repræsenteret af projektmappestrømmen. Hvert regneark i en projektmappe er repræsenteret af understrømme. Derudover har den Chart Sheet Substream, Macro Sheet Substream eller Dialog Sheet Substream, der følger den globale understrøm. Hver binær strøm eller understrøm, der indeholder projektmappedata, SKAL skrives som en række binære poster.

#### Optag ####

Oplysninger om funktioner i en projektmappe gemmes som en post, der er en sekvens af bytes med variabel længde. En binær post består af følgende tre komponenter:

**Record Type:** Record-typen er et to-byte usigneret heltal, der specificerer, hvilken type information der er specificeret af posten, og hvordan strukturen af postdataene, der er specifikke for denne post, er ordnet og struktureret. Recordtypeværdier SKAL være en værdi fra Record Enumeration (afsnit 2.3), eller posten SKAL gøre brug af den fremtidige postarkitektur (afsnit 2.1.6).

**Record Size**: Poststørrelsen er et to-byte usigneret heltal, der angiver antallet af bytes, der specificerer den samlede størrelse af postdataene. Poststørrelsen SKAL være større end eller lig med 0 og SKAL være mindre end eller lig med 8224.

**Record Data:** Record data-komponenten indeholder felter, der svarer til en bestemt posttype og omfatter resten af posten. Rækkefølgen og strukturen af felterne for en given posttype er specificeret i det tilsvarende afsnit for den pågældende posttype. Størrelsen af registreringsdatakomponenten SKAL være lig med poststørrelsen. Felter i postdatakomponenten kan indeholde simple værdier, arrays af værdier, strukturer af flere felter, arrays af felter og arrays af strukturer.

#### Celletabel ####

Celler er de grundlæggende blokke i en projektmappe, der gemmer projektmappens indhold som tekst, formler og numeriske data. Celler opretholder registreringen af de lagrede data via en datastruktur kaldet celletabellen. Selve celletabellen gemmes i rækkefølgen af poster, der er i overensstemmelse med CELLTABLE-reglerne defineret i specifikationsdokumentet. Den består af en række rækkeblokke, hvor rækkerne er arrangeret i rækkeblokke. Hver rækkeblok indeholder rækker fra den første række, der indeholder data, til den sidste række, der indeholder data.

Data eller rækkeformatering gemmes i en rækkepost for hver rækkeblok. Hver celle, der indeholder data eller individuel celleformatering, er repræsenteret af en post. Formatering forbundet med en celle kan afledes fra individuel celleformatering, rækkeformatering, kolonneformatering eller standardcelleformatet. Rækkefølgen for formatering er individuel celleformatering med den højeste prioritet, efterfulgt af rækkeformatering og derefter kolonneformatering og derefter standardcelleformatet. Celler, der ikke indeholder data og ikke indeholder individuel formatering, gemmes ikke.

#### Formler ####

En formel er en sekvens af værdier, cellereferencer, navne, funktioner eller operatorer i en celle, der tilsammen producerer en ny værdi. Formler gemmes i en tokeniseret repræsentation kendt som parsed expressions. Et parset udtryk konverteres til en tekstformel ved kørsel til visning og brugerredigering. Celleformler er specificeret af formelposten. Matrixformler er angivet af Matrixposten. Delte formler er specificeret af ShrFmla-posten.

#### Diagrammer ####

Diagramarket specificerer et diagram, en grafik, der viser data eller relationerne mellem datasæt i en visuel form, og en diagramdatacache, en lokal kopi af de data, der bruges i diagramdataene mangler, eller hvis links til eksterne datakilder er brudt. Diagrammet specificerer en- eller toaksegrupper, et sæt akser, som diagramdataene er plottet mod, og sættet af serier, trendlinjer og fejlbjælke angivet i diagrammet. Hver aksegruppe angiver en til fire diagramgrupper, der angiver den type visualisering, der bruges til at vise dataene. Hver serie, trendlinje og fejlbjælke angiver en diagramgruppe, den er knyttet til.

#### Metadata ####

Metadata er yderligere data knyttet til en bestemt celle eller dens indhold. Metadata er kun registreret i BIFF8 til fremtidige udvidelsesformål.

#### Pivottabeller ####

En pivottabel er en mekanisme til at opsummere kildedata for at få et overblik over fordelingen af disse data. I en pivottabel bliver relevante kolonner af kildedata til felter, der kan bruges til at opsummere data. Når pivottabellens kildedata er OLAP-kildedata, bliver OLAP-hierarkier og nogle andre OLAP-enheder til felter i pivottabellen.
En pivottabel har to hoveddele, en pivotcache og en pivottabelvisning. Der kan være flere pivottabelvisninger baseret på en enkelt ikke-OLAP PivotCache.

#### Stilarter ####

Denne oversigt beskriver, hvordan formaterings- og beskyttelsesoplysninger for celler i et ark (1) er specificeret. Celleformatering er sammensat af flere sæt egenskaber:

* Skrifttypeegenskaber (fed, kursiv, skriftfarve, skriftstørrelse osv...)

* Fyldegenskaber (forgrundsfarve, baggrundsfarve, mønster, gradient osv...)

* Justeringsegenskaber (venstre-, center-, højrejustering osv...)

* Kantegenskaber (venstre, højre, top, bund, tyk eller tynd, farve osv...)

* Egenskaber til talformatering (dato, klokkeslæt, antal decimaler osv...)

* Beskyttelsesegenskaber (låst, skjult osv...)


Disse egenskaber beskriver som helhed, hvordan en bestemt celle vises og udskrives.

## Referencer ##

* [[MS-XLS] - Excel Binær filformatstruktur](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [[MS-CFB] - Sammensat fil binært filformat](https://msdn.microsoft.com/en-us/library/dd942138.aspx)


