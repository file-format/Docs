{
  "date" : "2019-10-11",
  "keywords" :[ "dcm fil", "dcm filformat", "vad är en dcm fil", "fil", "dcm exempel", "dcm filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM-filformat - Digital medicinsk informationsfil",
  "description":"Läs mer om DCM-filformat och API:er som kan skapa och öppna DCM-filer.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Vad är en DCM fil?

Filer med filtillägget .dcm representerar digitala bilder som lagrar medicinsk information om patienter såsom MRI, datortomografi och ultraljudsbilder. DCM-filer använder bildfilformatet [DICOM](/sv/image/dicom) (Digital Imaging and Communications in Medicine) och kan innehålla patientinformation som referens. Det utvecklades av [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) och var tänkt att standardisera bildformatet för distribution och visning av medicinska bilder.

## DCM filformat

DCM-filer lagrar information i DICOM-bildformat. Dessa filer lagrar datamängden, som är information från den verkliga världen, som representerar en SOP-instans relaterad till en DICOM IOD. DICOM-filmetainformation lagras i filen följt av byteströmmen för den faktiska datamängden.

### Metainformation för DICOM-fil ##

Varje DICOM-fil innehåller en identifieringsinformationsrubrik för den inkapslade datamängden som består av:
* En 128-byte filpreambel
* 4 byte DICOM-prefix
* Fil Meta Elements

Denna rubrik är ett måste för varje DICOM-fil.

### Filmetaelement ###
|Attributnamn|Tagg|Typ| Attributbeskrivning
---|---|---|---|
|File Preamble|Inga tagg- eller längdfält|1|Ett fast 128 byte-fält tillgängligt för applikationsprofil eller implementeringsspecifik användning. Om den inte används av en applikationsprofil eller en specifik implementering ska alla bytes ställas in på 00H. Filuppsättningsläsare eller -uppdaterare ska inte förlita sig på innehållet i denna inledning för att avgöra att denna fil är eller inte är en DICOM-fil.
|DICOM-prefix|Inga tagg- eller längdfält|1|Fyra byte som innehåller teckensträngen "DICM". Detta prefix är avsett att användas för att identifiera att den här filen är eller inte en DICOM-fil.
|File Meta Information Group Length|(0002,0000)|1|Antal byte efter detta filmetaelement (slutet på värdefältet) upp till och inklusive det sista filmetaelementet i grupp 2-filens metainformation
|Version för filmetainformation|(0002,0001)|1|Detta är ett tvåbytefält där varje bit identifierar en version av denna filmetainformationshuvud. I version 1 är det första bytevärdet 00H och det andra bytevärdet är 01H. Implementeringar som läser filer med metainformation där detta attribut har bit 0 (lsb) av den andra byten satt till 1 kan tolka filmetainformationen som specificeras i denna version av PS3.10. Alla andra bitar ska inte kontrolleras.
|Medielagring SOP-klass UID|(0002,0002)|1|Identifierar unikt SOP-klassen som är associerad med datamängden. SOP Class UIDs som är tillåtna för medialagring specificeras i PS3.4 - Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Identifierar unikt SOP-instansen som är associerad med datamängden som placerats i filen och följer filens metainformation.
|Transfer Syntax UID|(0002,0010)|1|Identifierar unikt överföringssyntaxen som används för att koda följande datamängd. Denna överföringssyntax gäller inte för filmetainformationen.
|Implementation Class UID|(0002,0012)|1|Identifierar unikt implementeringen som skrev den här filen och dess innehåll. Det ger en entydig identifiering av vilken typ av implementering som senast skrev filen i händelse av utbytesproblem.
|Implementationsversionsnamn|(0002,0013)|3|Identifierar en version för ett Implementation Class UID (0002,0012) med upp till 16 tecken i repertoaren.
|Source Application Entity Title|(0002,0016)|3|DICOM Application Entity (AE) Titeln på AE som skrev filens innehåll (eller senast uppdaterade den). Om den används tillåter den spårning av felkällan i händelse av problem med mediautbyte.
|Private Information Creator UID|(0002,0100)|3|UID för skaparen av den privata informationen (0002,0102).
|Privat information|(0002,0102)|1C|Innehåller privat information placerad i filens metainformation. Skaparen ska identifieras i (0002,0100). Krävs om Private Information Creator UID (0002,0100) finns.

### Data Set Incapsulation ###

En DICOM-fil innehåller en enda datamängd som representerar en enda SOP-instans relaterad till en enda SOP-klass. Överföringssyntaxens UID för DICOM-filens metainformation ska definiera överföringssyntaxen som används för att koda datamängden.

### Stöd för filhanteringsinformation ###

Medieformatlagret tillhandahåller följande filhanteringsinformation om nödvändigt för en given DICOM-applikationsprofil.

* Identifiering av filinnehållsägare

* Statistik för filåtkomst (t.ex. datum och tid för skapandet)

* Kontroll av åtkomst till applikationsfiler

* Fysisk mediaåtkomstkontroll (t.ex. skrivskydd)

## Referenser ##
* [DICOM Standard](https://www.dicomstandard.org/current/)
* [DICOM-filformat](http://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

