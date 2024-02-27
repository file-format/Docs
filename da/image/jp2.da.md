{
  "date": "2019-10-11",
  "keywords": [
"jp2 fil",
"jp2 filformat",
"hvad er en jp2-fil",
"fil",
"jp2 eksempel",
"jp2 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 - Billedfilformat",
  "description": "Lær om JP2-filformat og API'er, der kan oprette og åbne JP2-filer.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-da2"
}
},
  "lastmod": "2020-08-10"
}

## Hvad er JP2 fil? ##

JPEG 2000 (**JP2**) er et billedkodningssystem og en avanceret billedkomprimeringsstandard. Det bruger wavelet-teknologi til at kode tabsfrit indhold i enhver kvalitet på én gang. Uden nogen væsentlig bøde i kodningseffektivitet har JPEG 2000 desuden mulighed for at få adgang til og afkode det samme indhold effektivt til en række andre opløsninger og kvaliteter. Kodestrømmene i JPEG 2000 er betydeligt skalerbare med områder af interesse, der giver mulighed for rumlig tilfældig adgang.

JPEG 2000 skiller sig ud som en af de mest skalerbare standarder. Forskellige dele af et billede kan gemmes ved hjælp af forskellige kvaliteter. En bemærkelsesværdig eskalering af ydeevnen kan opnås ved at bestille kodestrømmen på en række forskellige måder. Ikke desto mindre kræver JP2 komplekse og beregningsmæssigt udfordrende indkodere/dekodere, som et resultat af denne fleksibilitet. Sammenlignet med JPEG producerer JPEG 2000 kun ringeartefakter, der laver ringe tæt på billedkanten og kan være slørede, mens JPEG bruger 8×8 visuelle artefakterblokke, som både kan være ringende og blokerende artefakter. Besidder op til 16384 forskellige komponenter med dimensionerne i terapixels og præcision, der kan være op til 38 bits/prøve.

## Historie ##

I 2000 designede Joint Photographic Experts Group-komiteen JP2 med det formål at forbedre deres egen diskrete cosinustransformationsbaserede JPEG-standard med denne nye wavelet-baserede metode. JPEG-udvalget havde til formål at give deres basismetoder fri for licensgebyrer. I JP2-licensen, der fik konkurrence blandt 20 virksomheder, vandt de med knurhår. JPEG 2000 er blevet erklæret som en ISO-standard, selvom de fleste webbrowsere ikke er klar til at give en hånd med JPEG 2000 siden 2017.

## Dele af JPEG 2000 billedkodningssystem ##

Følgende er de vigtigste dele, der udgør den komplette suite af standarder for JPEG 2000.


|Del|Titel|Beskrivelse|Nummer
---|---|---|---|
|Del 1|Kernekodningssystem| Definerer syntaks for kodestrøm. Forskellige stadier involveret i afkodning af JPEG 2000-billeder. Forklarer grundlæggende filformat JP2, metadata og IP-rettigheder, der skal leveres.|ISO/IEC 15444-1
|Del 2|Udvidelser|Definerer udvidelser til filformatkodestrøm og tillader HDR-eksempeldemonstrationer, farverumsspecifikation, beskæring, geometriske transformationer; forskellige animationer, metadata og flere kodestrømme.|ISO/IEC 15444-2
|Del 3|Motion JPEG 2000 (MJ2 eller MJP2)|Introducer et filformat til bevægelsessekvenser, der koder billeder i en uafhængig kodestrøm.|ISO/IEC 15444-3
|Del 4|Konformance|Angiver testteknikker til kodning og afkodning og kontrollerer filer for både bare code-streams og JP2-filer.|ISO/IEC 15444-4
|Del 5|Referencesoftware|Består af to kildekodepakker (Java, C), der implementerer Core-kodningssystem og er tilgængelig under open source-licenser.|ISO/IEC 15444-5
|Del 6|Sammensat billedfilformat|Definerer JPM-filformatet og tillader flersidet dokumentafbildning til faxlignende applikationer. Understøtter brugen af JBIG2 og JPEG.|ISO/IEC 15444-6
|Del 8|JPEG 2000 Secured (JPSEC)|Sikrer sikkerheden for transaktioner, indhold og teknologier og tillader sikrede JPEG 2000 bit-streams.|ISO/IEC 15444-8
|Del 9|JPIP|Definerer værktøjer i et netværksmiljø for at få adgang til metadata og billeder og angiver interaktive og effektive protokoller|ISO/IEC 15444-9
|Del 10|JP3D|Volumetric udvidelse af Del 1 og introducerer Z-dimensionen. Udvider konceptet med fliser, kodeblokke, områder og 3D-område-af-interesse tilgængelighedsfunktioner.|ISO/IEC 15444-10
|Del 11|JPWL|Omhandler velorganiseret transmission over et fejludsat trådløst netværk. Denne udvidelse er kompatibel med dekodere|ISO/IEC 15444-11
|Del 13|Entry-level Encoder|Definerer en entry level encoder-implementering af Core-kodningssystem.|ISO/IEC 15444-13
|Del 14|JPXML|En repræsentation i XML og forklarer markørsegmenter og metoder til at få adgang til de interne data i billeder.|ISO/IEC 15444-14
|Del 15|HTJ2K (Under-udvikling)|Specificerer en alternativ blokkodningsalgoritme. Algoritme tilbyder en ti gange øget gennemstrømning og tabsfri kodning/afkodning.|

## JP2 filformat ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Selvom billedeksempler udelukkende beskrives af JPEG 2000, indeholder JPEG-1 dog andre tilføjede oplysninger om farverum og opløsning, der er afgørende for at kode billedet. Hvis et billede er gemt som JPEG 2000-fil, bruges **.jp2** som filtypenavn. Dette filformat forbedres yderligere med JPEG 2000 del-2-udvidelsen, som definerer animationsmekanismer og konfiguration af adskillige kodestrømme til ét enkelt billede. **.jpx**-udvidelsen bruges, når billeder gemmes i dette udvidede filformat. Da kodestrømsdata primært ikke anses for at være gemt i filer, er der ikke defineret nogen standardudvidelse til dette formål. Til testformål får den dog ofte udvidelsen **.jpc** eller **.j2k**. I modsætning til JPEG-1 vælger JPEG 2000 en anden måde at kode metadata på i XML-format. Standarden 12234-1.4 (af ISO TC42-komiteen) bruges som reference mellem Exif-tags og XML-komponenterne. JPEG 2000 kan indeholde en ISO-standard, XMP indeni.

### Klumper ###
JPEG 2000-filer består af på hinanden følgende bidder. Hver chunk har 8 byte header: 4-byte chunk størrelse (big-endian, high byte first) og 4-byte chunk type - en af foruddefinerede signaturer: jP eller jP2.

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000 defineret af undertype, som skal være en af værdierne: jp2 (filtype \*.JP2), jp20 (filtype \*.JPA), jpm  (filtype \*.JPM), jpx  (filtype \*.JPX).

Gentager bidder, indtil ukendt type er fundet, komponerer vi JPEG 2000 billed-/videofil.

### Farvetransformation ###

I første omgang kræves transformation af billeder fra RGB-farverum til et andet farverum. Til dette formål er der to måder: Irreversible Color Transform (ICT) og Reversible Color Transform (RCT). Tidligere bruger YC,,B,,C,,R,, farverum og skal implementeres i fix/floating-point, mens det senere er et modificeret YUV-farverum og vendbart i naturen.// //Ikke begrænset til RGB-model, JPEG 2000 sprog bruger multiple komponent transformation.

### Flisebelægning ###

Når farvetransformationen er færdig, konverteres billedet til rektangulære områder kaldet fliser, der kan transformeres og kodes separat. Størrelsen på alle fliser vil have den samme eller hele billedet kan betragtes som en enkelt flise. Dekoder udnytter fordelen ved fliselægning og bruger mindre hukommelse eller kan delvist kode nogle fliser. Selvom denne teknik har en ulempe ved kvalitetsforringelse af billedet.

### Wavelet transform ###

Billedet efter fliselægning er wavelet-transformeret, som enten kan være irreversibelt eller reversibelt og implementeret ved at bruge foldnings- eller løfteskemaet.

### Kompressions forhold ###

Afhængigt af et billedes fysiske karakteristika opnås en komprimeringsforstærkning på 20 %. Rumlig redundans forudsigelse af JPEG 2000 spiller en afgørende rolle i komprimeringsprocessen, og billeder med høj opløsning har en tendens til at opnå størst fordel.

## Applikationer tjent med standarden ##

* Optagelse, redigering og lagring af frame-baserede HD-videoer

* Medicinsk billedsprog og biometri

* Satellitbilleder, fjernmåling og bevægelsesdetektering

* Klient/server kommunikation, netværksdistribution og lagring.

* Digital biograf, Live HDTV-feedbidrag, digitaliserede audiovisuelle ting


## Referencer ##

* [Oversigt over JPEG 2000](https://jpeg.org/jpeg2000/)

* [JPEG 2000 billedkodningssystem](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


