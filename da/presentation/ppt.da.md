{
  "date": "2019-12-13",
  "keywords": [
"ppt fil",
"ppt filformat",
"hvad er en ppt-fil",
"fil",
"ppt eksempel",
"ppt filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om PPT-filformat og API'er, der kan oprette og åbne PPT-filer.",
  "title": "PPT - PowerPoint-filformat",
  "linktitle": "PPT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pp-dat"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PPT fil?

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. En PPT-fil kan indeholde flere forskellige typer information såsom tekst, punktopstillinger, billeder, multimedier og andre indlejrede OLE-objekter. Microsoft kom op med et nyere filformat til PowerPoint, kendt som [PPTX](/presentation/pptx/), fra 2007 og frem, der er baseret på Office OpenXML og adskiller sig fra dette binære filformat. Flere andre applikationsprogrammer såsom OpenOffice Impress og Apple Keynote kan også oprette PPT-filer.

## Kort historie ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. Det stabile binære format blev delt som standard i PowerPoint 97-2003 til Windows. Det binære filformat understøttes til læsning og skrivning af de seneste versioner af PowerPoint samt PowerPoint 2016.

## Filformatspecifikationer ##

Siden introduktionen har PPT-filformatet gennemgået adskillige revisioner for tilføjelser af nye funktioner og forbedringer. De seneste tilgængelige versionsspecifikationer er version 6.0, der blev offentliggjort i august 2018, som ikke bør blandes med det rigtige produktnummer i PPT-filformatet, da Microsoft ikke længere leverer ændringer til dette format.

### Filformatoversigt ###

Nogle af nøglekomponenterne i et PPT-filformat er som følger:

#### Slides ####

Brugerdata såsom figurer, tekst, animationer og medier føjes til en præsentation i et dias. En præsentation kan indeholde et eller flere dias, der vises som diasshow, når en præsentation køres. En præsentation indeholder master-slides og titel-master-slides, der fungerer som skabelon for de almindelige visuelle egenskaber ved præsentationsdias. Der er også et note-master-slide og et uddelings-master-dias, der tjener et lignende formål og giver fælles visuelle egenskaber for alle noteslides og alle udskrevne uddelingskopier.

#### Former ####

Former er objekter, der giver brugerne mulighed for at tilføje en række indhold til et dias i form af pladsholderformer, billeder og grafer. Figurer på en masterdias definerer fælles data for grupper af figurer.

#### Pladsholdere figurer ####

Disse er specielle pladsholdere, der fungerer som beholdere til en række forskellige objekter. Forskellige pladsholderformer kan bruges til at give ledetråde til at indsætte specifikke typer former såsom tabeller eller diagrammer. Inde i et dias tilpasser en pladsholderform sig til de visuelle egenskaber fra et hoved-master-dias, titel-master-dias eller note-master-dias.

#### Eksterne objekter ####

Eksterne objekter såsom indlejret og sammenkædet lyd, sammenkædet video, indlejrede og sammenkædede OLE-objekter og hyperlinks kan indlejres i et dias. Disse objekter kan bruges til at aktivere sammenkædede objekter for at få adgang til eksterne ressourcer under et diasshow.

### Filformatstrukturer ###

PowerPoint binære filformater består af følgende strømme for at repræsentere den overordnede dokumentstruktur og data.

* Aktuel brugerstrøm

* PowerPoint-dokumentstream

* Billedstrøm

* Sammenfatningsoplysninger og dokumentoversigtsoplysninger (valgfrit)


De komplette specifikationer for DOC-filformat kan findes som angivet af [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) og bør konsulteres med henvisning til sektioner nævnt i de følgende detaljer.

#### Nuværende brugerstream ####

Den registrerer den sidste bruger, der åbnede dokumentet, og dens navn skal være Nuværende bruger.

#### PowerPoint-dokumentstream ####

Registrerer alle oplysninger om en PowerPoint-præsentation og forklarer dens layout og indhold. Det er en påkrævet stream, hvis navn SKAL være PowerPoint Document. Indholdet af denne strøm er specificeret af en sekvens af poster på øverste niveau. Delvis bestillingsrestriktioner på postsekvensen er specificeret i PersistDirectoryAtom- og UserEditAtom-posterne.

Som containerposter er DocumentContainer, MainMasterContainer (afsnit 2.5.3), HandoutContainer (afsnit 2.5.8), SlideContainer (afsnit 2.5.1) og NotesContainer (afsnit 2.5.6) hver især roden af et træ af containerposter og atomregistreringer. Inde i enhver containerpost kan der eksistere andre poster, der ikke udtrykkeligt er angivet som underordnede poster. Ukendte poster identificeres, når recType-feltet i RecordHeader-strukturen (afsnit 2.3.1) indeholder en værdi, der ikke er angivet af RecordType-opregningen (afsnit 2.13.24). Disse ukendte poster SKAL, hvis de stødes, ignoreres, og MAY<1> bevares. Ukendte poster kan ignoreres ved at søge frem recLen-bytes fra slutningen af RecordHeader-strukturen.

Hver gang denne strøm skrives, kan nye poster på øverste niveau, en brugerredigering, føjes til den eksisterende strøm, eller hele strømindholdet kan erstattes med en opdateret sekvens af poster på øverste niveau. Hvis hele strømmen ikke erstattes, kan alle tidligere eksisterende poster på øverste niveau, der omfattede enhver tidligere brugerredigering, blive forældet af de efterfølgende vedhæftede poster på øverste niveau, der omfatter den aktuelle brugerredigering.

#### Billedstream ####

Dette er en valgfri strøm, der indeholder data om billederne i en PowerPoint-præsentation. Dens navn SKAL være Billeder. Indholdet af denne strøm er specificeret af OfficeArtBStoreDelay-posten som specificeret i [MS-ODRAW] afsnit 2.2.21.

#### Oversigtsinformationsstrøm ####

Det fører statistik om dokumentet efter Microsoft Office-standarden. Navnet på oversigtsinformationsstrømmen skal være \005SummaryInformation, hvor \005 er tegnet med værdien 0x0005, ikke strengen \005. Denne stream SKAL udelades for krypterede dokumenter. Indholdet af denne strøm er specificeret i [MS-OSHARED] afsnit 2.3.3.2.1.

#### Informationsstrøm for dokumentoversigt ####

En valgfri strøm, hvis navn SKAL være \005DocumentSummaryInformation, hvor \005 er tegnet med værdien 0x0005, ikke den bogstavelige streng \005. Denne strøm KAN <2> udelades for krypterede dokumenter. Indholdet af denne strøm er specificeret i [MS-OSHARED] afsnit 2.3.3.2.2.

#### Krypteret oversigtsinformationsstrøm ####

En valgfri stream, hvis navn SKAL være EncryptedSummary. Denne strøm findes kun i et krypteret dokument. Indholdet af denne strøm er specificeret i [MS-OFFCRYPTO] afsnit 2.3.5.4.

#### Digital signaturlagring ####

Et valgfrit lager, hvis navn SKAL være _xmlsignatures. Det KAN udelades og KAN blive ignoreret. Indholdet af dette lager er specificeret i [MS-OFFCRYPTO] afsnit 2.5.2.

#### Tilpasset XML-datalagring ####

Et valgfrit lager, hvis navn SKAL være MsoDataStore. Indholdet af lageret er specificeret i [MS-OSHARED] afsnit 2.3.6.

#### Signaturstream ####

En valgfri stream, hvis navn SKAL være _signatures. Det BØR udelades og KAN ignoreres. Indholdet af denne strøm er specificeret i [MS-OFFCRYPTO] afsnit 2.5.1.

## Referencer ##

* [PPT-filformatspecifikationer](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint-filformater](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


