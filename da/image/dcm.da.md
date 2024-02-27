{
  "date": "2019-10-11",
  "keywords": [
"dcm fil",
"dcm filformat",
"hvad er en dcm fil",
"fil",
"dcm eksempel",
"dcm filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DCM-filformat - Digital medicinsk informationsfil",
  "description": "Lær om DCM-filformat og API'er, der kan oprette og åbne DCM-filer.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-dam"
}
},
  "lastmod": "2021-07-03"
}

## Hvad er en DCM fil?

Filer med filtypenavnet .dcm repræsenterer et digitalt billede, som gemmer medicinsk information om patienter, såsom MRI'er, CT-scanninger og ultralydsbilleder. DCM-filer bruger [DICOM](/image/dicom/) (Digital Imaging and Communications in Medicine) billedfilformat og kan indeholde patientoplysninger til reference. Det blev udviklet af [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) og var beregnet til at standardisere billedfilformatet til distribution og visning af medicinske billeder.

## DCM filformat

DCM-filer gemmer information i DICOM-billedformat. Disse filer gemmer datasættet, som er information fra den virkelige verden, som repræsenterer en SOP-instans relateret til en DICOM IOD. DICOM-filmetaoplysninger gemmes i filen efterfulgt af bytestrømmen for det faktiske datasæt.

### DICOM Fil Meta Information ##

Hver DICOM-fil indeholder en identifikationsinformationsheader for det indkapslede datasæt, som består af:
   * En 128-byte filpræamble
   * 4 byte DICOM-præfiks
   * Fil Meta Elementer

Denne header er et must for hver DICOM-fil.

### Fil-metaelementer ###
|Attributnavn|Tag|Type| Attributbeskrivelse
---|---|---|---|
|Fil præamble|Ingen tag eller længdefelter|1|Et fast 128 byte felt tilgængeligt for applikationsprofil eller implementering specificeret brug. Hvis den ikke bruges af en applikationsprofil eller en specifik implementering, skal alle bytes indstilles til 00H. Filsætlæsere eller -opdateringer må ikke stole på indholdet af denne præamble for at bestemme, om denne fil er eller ikke er en DICOM-fil.
|DICOM-præfiks|Ingen tag eller længdefelter|1|Fire bytes, der indeholder tegnstrengen DICM. Dette præfiks er beregnet til at blive brugt til at genkende, at denne fil er en DICOM-fil eller ej.
|Fil Meta Information Group Længde|(0002,0000)|1|Antal bytes efter dette Fil Meta Element (slutningen af feltet Værdi) til og med det sidste Fil Meta Element i Gruppe 2 Fil Meta Information
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Alle andre bits skal ikke kontrolleres.
|Medielager SOP-klasse UID|(0002,0002)|1|Identificerer unikt den SOP-klasse, der er knyttet til datasættet. SOP-klasse-UID'er, der er tilladt til medielagring, er angivet i PS3.4 - Media Storage Application Profiles.
|Media Storage SOP Instance UID|(0002,0003)|1|Identificerer unikt den SOP Instance, der er knyttet til det datasæt, der er placeret i filen og efter filmetaoplysningerne.
|Overførselssyntaks UID|(0002,0010)|1|Identificerer entydigt den overførselssyntaks, der bruges til at kode følgende datasæt. Denne overførselssyntaks gælder ikke for filmetaoplysningerne.
|Implementation Class UID|(0002,0012)|1|Identificerer entydigt den implementering, der skrev denne fil, og dens indhold. Det giver en entydig identifikation af den type implementering, der sidst skrev filen i tilfælde af udvekslingsproblemer.
|Implementeringsversionsnavn|(0002,0013)|3|Identificerer en version for et implementeringsklasse-UID (0002,0012) med op til 16 tegn i repertoiret.
|Kilde Application Entity Title|(0002,0016)|3|DICOM Application Entity (AE) Titlen på den AE, der skrev denne fils indhold (eller sidst opdaterede den). Hvis det bruges, tillader det sporing af fejlkilden i tilfælde af problemer med medieudveksling.
|Private Information Creator UID|(0002,0100)|3|UID for skaberen af de private oplysninger (0002,0102).
|Privat information|(0002,0102)|1C|Indeholder private oplysninger placeret i filens metainformation. Skaberen skal identificeres i (0002,0100). Påkrævet, hvis Private Information Creator UID (0002,0100) er til stede.

### Datasætindkapsling ###

En DICOM-fil indeholder et enkelt datasæt, som repræsenterer en enkelt SOP-instans relateret til en enkelt SOP-klasse. Overførselssyntaks-UID for DICOM-filmetainformationen skal definere den overførselssyntaks, der bruges til at kode datasættet.

### Understøttelse af filhåndteringsoplysninger ###

Medieformatlaget giver følgende filhåndteringsoplysninger, hvis det er nødvendigt for en given DICOM-applikationsprofil.

  * Identifikation af filindholdsejer

  * Statistik over filadgang (f.eks. dato og tidspunkt for oprettelse)

  * Adgangskontrol til applikationsfiler

  * Fysisk medieadgangskontrol (f.eks. skrivebeskyttelse)

## Referencer ##
  * [DICOM Standard](https://www.dicomstandard.org/current/)
  * [DICOM-filformat](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

