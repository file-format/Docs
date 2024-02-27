{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Filformat",
"CAD",
"Åben",
"skab"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DWG-filformat og API'er, der kan oprette og åbne DWG-filer.",
  "title": "DWG filformat",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DWG fil?

Filer med DWG-udvidelse repræsenterer proprietære binære filer, der bruges til at indeholde 2D- og 3D-designdata. Ligesom DXF, som er ASCII-filer, repræsenterer DWG det binære filformat for CAD-tegninger (Computer Aided Design). Den indeholder vektorbilleder og metadata til repræsentation af indholdet af CAD-filer. Der er gratis fremvisere til rådighed for visning af DWG-filer på Windows-operativsystemet, såsom Autodesks gratis DWG TrueView. Der er også andre tredjepartsapplikationer, der understøtter at nå DWG-filer. DWG-filer indeholder brugeroprettet information og inkluderer:

* Designs

* Geometriske data

* Kort og fotos


Dette format er meget brugt af arkitekter, ingeniører og designere til forskellige designformål.

## Kort historie ##

DWG file format has evolved with the time since its formal introduction in 1982. En kort oversigt over de tidligere begivenheder fra historieperspektiv er som følger.

**1982:** Autodesk licenserede DWG-filformatet, som blev udviklet af Mike Riddle i 1970, som grundlag for AutoCAD.

**1998:** Med udgivelsen af AutoCAD R14.01 tilføjede Autodesk filbekræftelse gennem en funktion kaldet DWGCHECK, der indlejrede en krypteret kontrolsum og produktkode, kaldet WaterMark af Autodesk, i DWG-filer oprettet af programmet.

**2006:** Autodesk modificerede AutoCAD 2007 til at inkludere TrustedDWG-teknologi for at indlejre tekststrengen Autodesk DWG. Denne fil er en Trusted DWG, der sidst er gemt af et Autodesk-program eller Autodesk-licenseret program i DWG-filerne. Formålet med dette var at hjælpe Autodesk-softwarebrugere med at sikre, at disse filer blev oprettet af en Autodesk- eller RealDWG-applikation, hvilket helt sikkert skulle hjælpe med at reducere risikoen for inkompatibiliteter.

## Filstruktur ##

DWG har været et af de meget anvendte filformater af en række applikationer og har en robust filstruktur. Da DWG er et binært filformat, kan det ikke læses af mennesker som det almindelige ASCII [DXF](/cad/dxf/) filformat. DWG-filer indeholder normalt oplysninger om billedkoordinaterne og alle metadata, der er knyttet til dem. Fuldstændige [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) af DWG-filformatet er tilgængelige for download af OpenDesign. Filstrukturen af DWG-filformat er opsummeret som følger.

**Header**: Filheaderen består af DWG Header-variabler og information om Cyclic Redundancy Check (CRC), som bruges til fejldetektion. Hver undersektion er en specialiseret vektor, hvor forskellige bitlængder bruges til at repræsentere forskellige etiketter. For eksempel står de første 6 bit af DWG Header-variablen for versionsstrengen.

**Klassedefinitioner:** En DWG-fil kan indeholde adskillige klasser afhængigt af det specifikke formål med .dwg-filen. Information såsom klassemetadatastørrelse på klassedataområde, klassenummer og kontrolsum ud over andre.

**Skabelon**: Dette er valgfrit, og for R15- og R15-versioner er dette afsnit under sektionen Objektfri plads.

**Padding**: Metadataene er suffikset og efterfikset med et bestemt antal bytes, hvilket gør de ældre AutoCAD-softwareversioner til at være videreforenelige med det nye DWG-filformat.

**Billeddata**: Metadataene for dette afsnit afhænger af den specifikke .dwg-type. For R14- og R15-brugere er dette afsnit valgfrit.

**Objektdata**: Objektdataene består af en komplet liste over tabelenheder, ordbogsposter osv. svarende til den eksisterende liste over objekter.

**Objektkort**: Placeringen af hvert objekt i filen er specificeret i denne sektion af filen. De fleste af metadataene i dette afsnit er filhåndtag, der spiller en rolle i identifikation og gengivelse af objektet.

**Objekt ledig plads**: Denne sektion er valgfri for alle brugere

**Anden overskrift**: En duplikat af filoverskriftssektionen mod slutningen af DWG-filen

## Referencer ##

* [DWG-filformatspecifikationer](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [DWG-filspecifikationen](https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG - af Wikipedia](https://en.wikipedia.org/wiki/.dwg)


