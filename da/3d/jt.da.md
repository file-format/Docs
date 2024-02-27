{
  "date": "2019-12-12",
  "keywords": [
"JT",
"fil",
"udvidelse",
"format",
"3D fbx",
""
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om JT filformat og API'er, der kan oprette og åbne JT filer.",
  "title": "JT - Jupiter Tessellation File Format",
  "linktitle": "JT",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-j-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er JT fil?

**JT** (Jupiter Tessellation) er et effektivt, industrifokuseret og fleksibelt ISO-standardiseret 3D-dataformat udviklet af Siemens PLM Software. Mekaniske CAD-domæner inden for rumfart, bilindustrien og tungt udstyr bruger JT som deres mest førende 3D-visualiseringsformat.

JT-format er en scenegraf, der understøtter de attributter og noder, der er CAD-specifikke. Sofistikerede komprimeringsteknikker bruges til at lagre facetdata (trekanter). Dette format er struktureret til at understøtte visuelle attributter, produkt- og produktionsoplysninger (PMI) og metadata. Der er god understøttelse for asynkron streaming af indhold. I den tunge mekaniske industri bruger fagfolk JT-fil i deres CAD-løsninger og softwareprogrammer til produktlivscyklusstyring (PLM) til at undersøge geometrien af komplicerede varer.

As JT supports nearly all important 3D CAD formats its assembly can deal with a variety of combination which is known as "multi-CAD". This multi-CAD assembly is always well managed and up-to-date because synchronization among native CAD product description files with their associated JT files takes place automatically. JT files are originally lightweight, so considered to be suitable for internet collaborations. Companies Collaborate through sending 3D visualizations over the media much more easily as compared to “heavy" original CAD files. In addition, JT files ensures many security feature that make intellectual property sharing more secure.

## Kort historie om JT-filformat

Engineering Animation, Inc. og Hewlett Packard var de oprindelige designere af JT, som udviklede dette format som Direct Model-værktøjssættet. Efter at EAI blev opkøbt af UGS Corp. blev JT en del af UGS's suite. Tidligt i 2007 annoncerede UGS JT som deres master 3D-format. Samme år købte Siemens AG UGS og viste sig at være Siemens PLM Software. Siemens bruger JT som det fælles interoperabilitetsformat og dataarkiveringsformat. I 2009 accepterede ISO JT-specifikation til offentliggørelse som en ISO Publicly Available Specification (PAS). I midten af 2010 annoncerede ProSTEP iViP, at på industrielt niveau kan JT og STEP AP 242 XML bruges sammen for at opnå den maksimale fordel i data udvekslingsscenarier. I 2012 er JT officielt blevet erklæret som et ISO-standardiseret (ISO 14306:2012 (ISO JT V1)) 3D-visualiseringsformat.

## JT filformat ##

Alle objekter i JT-formatet er repræsenteret gennem en objektidentifikator, og referencer mellem objekter håndteres gennem refererede objekters identifikator. Integriteten af disse objektreferencer kan vedligeholdes gennem pegepinde, der trækker/drejer.

En JT-fil er arrangeret som en serie af blokke, og Header-blok er altid den første blok af data i filen. En række datasegmenter og et TOC-segment følger umiddelbart efter headerblokken. Det ene datasegment (6 LSG-segment) har en referencekompatibel JT-fil eksisterer altid. TOC-segmentet indeholder placeringsoplysningerne for alle andre datasegmenter i den pågældende fil.

{{< figure src="../JT-1.png" alt="JT filformat" >}}

### Filoverskrift ###

File Header er den første blok i JT-filens datahierarki. Versioneringsoplysninger og TOC-placeringsoplysninger er indesluttet i headeren, hvilket letter indlæsere i fillæsning. Filoverskriftens indhold er arrangeret som følger.

### TOC-segment ###

TOC-segmentet skal eksistere i en fil og indeholde identifikation og placeringsoplysninger for alle andre datasegmenter. Den faktiske placering af TOC-segmentet er angivet af TOC Offset-feltet i filoverskriften. Hvert individuelt adresserbart datasegment er repræsenteret af TOC-indtastning i et TOC-segment.

### Datasegment ###

JT-fil definerer alle lagrede data i et datasegment. Nogle datasegmenter kan komprimere alle databytes af information, der er tilbage i segmentet. Datasegmenter har følgende struktur:

![alt text](../JT-2.png "JT Data Segment")

Følgende tabel beskriver forskellige typer datasegmenter:

|Navn|Beskrivelse
---|---|
|LSG segment|Omfatter en samling af objekter, der er forbundet via rettede referencer til dannelse af LSG (dirigeret acyklisk grafstruktur)
|Shape LOD segment|indeholder de definerende data for de geometriske former (f.eks. hjørner, normaler, polygoner osv.)
|JT B-Rep Segment|Har element til dataene til at repræsentere den præcise geometriske grænse for en individuel del i JT B-Rep format.
|XT B-Rep segment|Har element til dataene til at repræsentere den præcise geometriske grænse for en individuel del i grænserepræsentationsformat
|Wireframe-segment|Dataene repræsenterer den præcise 3D-wireframe for en bestemt del er defineret af et element indeholdt i dette segment.
|Metadatasegment|Tillader at gemme metadata i særskilte adresserbare segmenter.
|JT ULP-segment|Har et element til, at dataene repræsenterer den semi-præcise geometriske grænse for en individuel del i JT ULP-format.
|JT LWPA segment|Indeholder et element definere analytiske data for en bestemt del. LWPA omslutter den analytiske overfladesamling i b-rep definitionen af delen.

## Kompression ##

Kravene til transmission og lagring af 3D-modeller er mere krævende, så JT-filer kan drage fordel af komprimering. En JT-datamodel kan være sammensat af forskellige filer ved hjælp af forskellige komprimeringsteknikker, men komprimeringsprocessen er gennemsigtig for JT-databrugeren.

Indtil videre er JT Open Toolkit (som standard) og avanceret komprimering to komprimeringsteknikker, der bruges af JT-filer. JT Open Toolkit anvender en nem, tabsfri komprimeringsalgoritme, mens den avancerede komprimering anvender en mere raffineret, domænespecifik komprimeringsteknik, der fører til tabsgivende geometrikomprimering. Klientapplikationer foretrækker avanceret komprimering frem for at bruge standardkomprimering, da avanceret komprimering giver ret høje kompressionsforhold. Bagudkompatibilitet med almindelige JT-filvisningsapplikationer opretholdes gennem levering af standardkomprimering. Komprimeringsformularen skal være kompatibel med JT-filformatversionen, som kan ses, når en JT-fil åbnes ved hjælp af teksteditor og indesluttet i ASCII-headeroplysninger.

## Referencer ##

* [JT File Format Reference](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)

* [JT (visualiseringsformat)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)


