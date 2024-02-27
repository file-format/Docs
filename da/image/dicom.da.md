{
  "date": "2019-10-11",
  "keywords": [
"dicom fil",
"dicom filformat",
"hvad er en dicom fil",
"fil",
"dicom eksempel",
"dicom filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM - Digital Imaging and Communications File Format",
  "description": "Lær om DICOM-filformat og API'er, der kan oprette og åbne DICOM-filer.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-dam"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DICOM fil?

DICOM er forkortelsen for Digital Imaging and Communications in Medicine og vedrører feltet medicinsk informatik. DICOM bruges til integration af medicinske billedbehandlingsenheder som printere, servere, scannere osv. fra forskellige leverandører og indeholder også identifikationsdata for hver patient for unikhed. DICOM-filer kan deles mellem to parter, hvis de er i stand til at modtage billeddata i DICOM-format. Kommunikationsdelen af DICOM er applikationslagsprotokol og bruger TCP/IP til at kommunikere mellem enheder. Versioner, der understøttes af webtjenester, er 1.0, 1.1, 2 eller nyere.

## Historie ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. Den anden version blev udgivet i 1988, som var mere populær blandt leverandører, men snart blev det indset, at anden version også trænger til forbedring. Den 3. version af standarden blev udgivet i 1993 som DICOM. 3.0 er stadig den nyeste version, men den er løbende blevet opdateret siden 1993.

## DICOM-filformat ##

DICOM er kombinationen af filformatdefinition og en netværkskommunikationsprotokol. DICOM bruger filtypenavnet .DCM. .DCM findes i to forskellige formater, dvs. format 1.x og format 2.x. DCM Format 1.x er yderligere tilgængelig i to versioner normal og udvidet. HTTP- og HTTPS-protokoller bruges til DICOMs webtjenester.

### Filoverskrift ###

Filhovedet indeholder 128 byte filpræamble og 4 byte DICOM-præfiks.

** Præambel # 128 Bytes**|** Præfiks # 4 Bytes D, I, C, M**

**Preamble** bruges til at få adgang til billederne og andre data i DICOM-fil, hvilket giver kompatibilitet med almindeligt anvendte billedfilformater.

**Præfiks** indeholder strengen DICM som store bogstaver.

### Datasæt ###

Hver fil skal indeholde et enkelt datasæt, der repræsenterer SOP-instansen og SOP-klassen med tilhørende IOD. Datasæt er en repræsentation af information fra den virkelige verden. Datasæt indeholder dataelementer, og dataelementer indeholder værdier for det pågældende objekts attributter. Struktur af attributter er specificeret i IOD'er. Et DICOM-dataobjekt består af en række attributter, herunder elementer som navn, ID osv., og også en speciel attribut, der indeholder billedpixeldataene.

### Dataelementer ###

Dataelementet består af dataelement Tag, Værdi længde og værdi for dataelementet. Der er 5 typer dataelementer, nemlig Type 1 påkrævede dataelementer, Type 1C betingede dataelementer, Type 2 påkrævede dataelementer, Type 2C betingede dataelementer og Type 3 valgfri dataelementer. Grundlæggende Tre typer dataelementstrukturer er som følger.

**Dataelement med en eksplicit VR**

|Gruppenummer|Elementnummer|Værdirepræsentation|Reserveret|Værdilængde|Værdifelt
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|Værdi Længde Bytes

**Dataelement med en eksplicit VR**

|Gruppenummer|Elementnummer|Værdirepræsentation|Værdilængde|Værdifelt
---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes|Værdi Længde Bytes

**Dataelement med en implicit VR**


|Gruppenummer|Elementnummer|Værdilængde|Værdifelt
---|---|---|---|
|2 Bytes|2 Bytes|4 Bytes|Værdi Længde Bytes

1. **Data Element Tag**: Et ordnet heltal, som repræsenterer gruppenummeret og elementnummeret
1. **Værdirepræsentation VR**: VR er en tegnstreng, som repræsenterer dataelementets VR.
1. **Værdilængde**: er det heltal uden fortegn repræsentere den eksplicitte længde af værdifeltet.
1. **Værdifelt**: Beskriver værdierne for dataelementerne.

## Overførselssyntaks ##

Overførselssyntaks er et sæt regler for kodning for utvetydigt at repræsentere mere abstrakte syntakser. Ved hjælp af overførselssyntaks forhandler kommunikerende enheder om almindelige kodningsteknikker, som de understøtter.

## SOP'er ##

Union of IOD og DIMSE definerer en SOP-klasse. SOP-klassedefinitionen indeholder regler og semantik, der kan begrænse brugen af tjenesterne i DIMSE Service Group eller IOD'ens attributter. Eksempler på Serviceelementer er Store, Hent, Find, Flyt osv. Eksempler på Objekter er CT-billeder, MR-billeder, men omfatter også skemalister, printkøer mv.

## Tjenester ##

DICOM leverer forskellige tjenester, hovedsagelig relateret til kommunikation af data. Hver enkelt er kort beskrevet nedenfor:


**Butik:** DICOM Store-tjenesten sender billeder eller andre objekter til et billedarkiverings- og kommunikationssystem (PACS) eller en server.


**Opbevaringsforpligtelse:** Opbevaringsforpligtelse bruges til at bekræfte, at et billede er blevet permanent gemt på en enhed på enhver type medie.


**Forespørgsel/hent:** Denne tjeneste gør det muligt for en arbejdsstation at finde lister over billeder eller andre objekter og derefter hente dem fra PACS.


**Modalitetsarbejdsliste:** Modalitetsarbejdslistetjenesten giver en liste over billedbehandlingsprocedurer, der er planlagt til ydelse af en billedopsamlingsenhed.


**Udskriv:** Denne tjeneste sender billeder til printeren.

## Portnumre over IP ##

DICOM bruger følgende TCP- og UDP-porte:

1. 104
1. 2761
1. 2762
1. 11112

## Referencer ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)


