{
  "date": "2019-12-03",
  "keywords": [
"dok",
"fil",
"udvidelse",
"filformat",
"Ord",
"Dokument"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOC - Microsoft Word-dokumentfil",
  "description": "Lær om DOC-filformat og API'er, der kan oprette og åbne DOC-filer.",
  "linktitle": "DOC",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-do-dac"
}
},
  "lastmod": "2019-12-03"
}

## Hvad er en DOC fil?

Filer med filtypen .doc repræsenterer dokumenter genereret af Microsoft Word eller andre tekstbehandlingsdokumenter i binært filformat. Udvidelsen blev oprindeligt brugt til almindelig tekstdokumentation på flere forskellige operativsystemer. Det kan indeholde flere forskellige typer data såsom billeder, formateret såvel som almindelig tekst, grafer, diagrammer, indlejrede objekter, links, sider, sideformatering, udskriftsindstillinger og meget andet. Formatet var populært til al slags dokumentation på grund af de mange muligheder, det giver brugerne til at skrive manualer, forslag, specifikationer, CV'er, artikler eller lignende dokumenter. Den opdaterede version af DOC er [DOCX](/word-processing/docx/), som er baseret på Office OpenXML, hvis specifikationer er åbent tilgængelige.

## Kort historie ##

WordPerfect, a product of [Corel](https://www.corel.com/en/), used DOC as the extension of their proprietary format. In 1980s, WordPerfect remained the choice of usage on most of the computers due to its easy availability, conformance with most computer machines and Operating systems. However, WordPerfect saw its downfall on Windows OS when Microsoft introduced Microsoft Word as its product for documents file format and chose DOC extension for their proprietary format. As Microsoft Word became more and more popular, the DOC file format underwent several revisions from Microsoft Word 97 - 2003. Det var i 2007, da standard DOC-filformatet blev erstattet af Office Open XML-formatet (kendt som DOCX), og de nye versioner af Microsoft Word bruger nu denne nye udvidelse som standardfilformat.

## DOC-filformatspecifikationer - flere oplysninger

Microsoft didn't release the DOC file format specifications for a long time until 2008. In Feb 2008, format specifications were released for .doc file format under the Microsoft Open Specification Promise. Though the specification does not describe all of the features used by the DOC format, it gives ample information about the knowledge required to work with this file format. Still, reverse engineering is required to make use of the available information. The specifications have been updated several times and the latest [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 which was updated as of August 2018.

### Nogle grundlæggende begreber ###

Før vi går ind i detaljer om filformatspecifikationerne for DOC, er nogle grundlæggende begreber nødvendige at forstå for at kunne arbejde med dette filformat.

**Filinformationsbase (Fib):** Fib-strukturen indeholder oplysninger om dokumentet og specificerer filpegerne til forskellige dele, der udgør dokumentet.
Fib er en struktur med variabel længde. Med undtagelse af basisdelen, som er fast i størrelse, indledes hver sektion med et tællefelt, der angiver størrelsen af den næste sektion.

**Tegnposition:** CP eller tegnposition repræsenterer et 32-bit heltal uden fortegn, der fungerer som det nul-baserede indeks for et tegn i dokumentteksten. Placeringen og størrelsen af hvert tegn i filen kan ikke hentes direkte og skal beregnes ved hjælp af en foruddefineret algoritme. Karakterer inkluderer:

* Tekst i dokumentet

* Ankre af objekter såsom fodnoter eller tekstbokse

* Styretegn såsom afsnitsmærker og tabelcellemærker


**PLC:** PLC-strukturen er en række CP'er efterfulgt af en række dataelementer. Dataelementerne for enhver PLC skal have samme størrelse på nul eller flere bytes, og af denne grund skal antallet af CP'er være én mere end antallet af dataelementer. PLC-strukturer er af forskellige typer, hvor hver type specificerer, om duplikat-CP'er er tilladt for den type eller ej. En PLC-struktur består af:

* **aCP (variabel længde):** En række CP-elementer. Hver type **PLC**-struktur specificerer betydningen af CP-elementerne og det tilladte område.

* **aData (variabel længde):** Hver type **PLC**-struktur specificerer strukturen og betydningen af dataelementerne, eventuelle begrænsninger for antallet af dataelementer og eventuelle begrænsninger for de data, der er indeholdt deri. Den specificerer også forholdet mellem dataelementerne og de tilsvarende CP'er.


**Gyldigt udvalg:** .DOC-filkonstruktionerne er hovedsageligt beskrevet af en række CP'er. Der er en række [rules](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) specificeret af Microsoft, som skal følges i sådanne tilfælde.

**STTB:** STTB er en strengtabel, der består af en header, der efterfølges af en række elementer. Værdien **cData** angiver antallet af elementer, der er indeholdt i arrayet.

**Ejendomslagring:** En word-fil kan have forskellige elementer såsom tekst, afsnit, tabeller, billeder og sektioner, hvor hver enkelt kan have sine egne egenskaber. Egenskaber for disse er gemt i Word-filen som forskelle fra standard. Sådanne forskelle er specificeret af PRl, der består af en Single Property Modifier (Sprm) og dens operand. En applikation kan bestemme det endelige sæt af egenskaber ved anvendelse af lister over **Prl**s.

**Adgangskodebeskyttelse:** Word-filer kan også beskyttes med adgangskode, hvortil en af følgende mekanismer kan bruges.

* XOR sløring

* Office binært dokument RC4-kryptering

* Office binært dokument RC4 CryptoAPI-kryptering


Hvis FibBase.fEncrypted og FibBase.fObfuscation begge er 1, sløres filen ved at bruge XOR-obfuscation.

Hvis FibBase.fEncrypted er 1 og FibBase.fObfuscation er 0, krypteres filen ved at bruge enten Office Binary Document RC4 Encryption eller Office Binary Document RC4 CryptoAPI Encryption, med EncryptionHeader gemt i de første FibBase.lKey bytes i tabelstrømmen. EncryptionHeader.EncryptionVersionInfo angiver, hvilken krypteringsmekanisme der blev brugt til at kryptere filen.

### Filstruktur ###

En binær Word-fil i sin originalitet er en OLE-sammensat fil, der består af flere lager og streams. Disse lagre og strømme har deres egen struktur og størrelse, der specificerer parametrene for skrivning og læsning. Disse er:

#### WordDocument Stream ####

This stream contains the document text and other information referenced from other parts of the file. The stream has no predefined structure other than the FIB at the beginning which is mandatory and should be at offset 0. Denne stream må ikke være større end 2147 MB.

#### 1TableStream eller 0TableStream ####

En binær Word-fil kan indeholde Table Streams kendt som 1Table stream eller 0Table stream. Mindst én af disse skal være til stede i dokumentet. Men hvis et dokument indeholder både 1Table- og 0Table-strømme, bruges kun strømmen, der refereres til af base.fWhichTblStm. Den ikke-refererede stream SKAL ignoreres.
Table Stream MÅ IKKE være større end 2147 MB.

#### Datastrøm ####

Datastrømmen har ingen foruddefineret struktur. Den indeholder data, der refereres fra FIB eller fra andre dele af filen. Denne stream behøver ikke at være til stede, hvis der ikke er referencer til den. Datastrømmen MÅ IKKE være større end 2147 MB.

#### Opbevaring af objektpool ####

Objektpuljelageret indeholder lager til indlejrede OLE-objekter. Dette lager behøver ikke være til stede, hvis der ikke er indlejrede OLE-objekter i dokumentet.

#### Tilpasset XML-datalagring ####

Det brugerdefinerede XML-datalager er et valgfrit lager, hvis navn SKAL være MsoDataStore.

#### Oversigtsinformationsstrøm ####

Opsummeringsinformationsstrømmen er en valgfri strøm, hvis navn SKAL være \005SummaryInformation, hvor \005 er tegnet med værdien 0x0005, og ikke strengen bogstaveligt \005.

#### Informationsstrøm for dokumentoversigt ####

Dokumentoversigtsinformationsstrømmen er en valgfri strøm, hvis navn SKAL være \005DocumentSummaryInformation, hvor \005 er tegnet med værdien 0x0005, ikke den bogstavelige streng \005.

#### Krypteringsstream

Krypteringsstrømmen er en valgfri stream, hvis navn SKAL være kryptering. Denne stream MÅ IKKE være til stede, medmindre begge følgende betingelser er opfyldt:

* Dokumentet er krypteret med Office Binary Document RC4 CryptoAPI-kryptering.

* fDocProps-værdien er indstillet i EncryptionHeader.Flags.


#### Makrolager

Makrolageret er et valgfrit lager, der indeholder makroerne til filen. Hvis det er til stede, SKAL det være en Project Root Storage.

#### Opbevaring af XML-signaturer

XML-signaturlageret er et valgfrit lager, hvis navn SKAL være \_xmlsignatures.

#### Signaturstream

Signaturstrømmen er en valgfri strøm, hvis navn SKAL være \_signaturer. Denne stream indeholder digitale signaturer.

#### Information Rights Management Data Space Storage

Information Rights Management Data Space-lageret er et valgfrit lager, hvis navn SKAL være \006DataSpaces, hvor \006 er tegnet med værdien 0x0006, og ikke den bogstavelige streng \006. Hvis denne lagring er til stede, SKAL den beskyttede indholdsstrøm også være til stede.
Hvis denne lagring er til stede, BØR alle specificerede streams og lagringssteder ud over denne lagring og den beskyttede indholdsstrøm læses fra den beskyttede indholdsstrøm som specificeret i [MS-OFFCRYPTO], og hvis nogen af disse streams og lagringer findes uden for det beskyttede indhold Stream, de SKAL ignoreres.

#### Beskyttet indholdsstrøm

Den beskyttede indholdsstrøm er en valgfri strøm, hvis navn SKAL være \009DRMContent, hvor \009 er tegnet med værdien 0x0009, og ikke strengen \009.
Hvis denne strøm er til stede, SKAL Information Rights Management Data Space Storage også være til stede.

## Referencer ##

* [MS-DOC fildannelsesspecifikationer](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)

* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))


