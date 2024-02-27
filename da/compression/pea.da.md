{
  "date": "2021-04-21",
  "keywords": [
"ærtefil",
"ært filformat",
"hvad er en ærtefil",
"fil",
"ærte eksempel",
"pea filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PEA - PeaZip Archive File Format",
  "description": "Lær om PEA-filformat og API'er, der kan oprette og åbne PEA-filer.",
  "linktitle": "PEA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pe-daa"
}
},
  "lastmod": "2021-04-21"
}

## Hvad er PEA fil?

En fil med filtypenavnet .pea, akronym for Pack, Encrypt og Authenticate, er et [zip](/compression/zip/)-arkiv oprettet med [PeaZip](https://peazip.github.io/)-arkiveringssoftwareapplikationen. Den har komprimering og output af flere lydstyrker og tilbyder en fleksibel sikkerhedsmodel gennem autentificeret kryptering og kryptografi. Dette giver både privatliv og autentificering af dataene. PeaZip-værktøjet er tilgængeligt som open source-motor, der kan kompileres til forskellige OS i henhold til kravene.

## PEA filformat

[PEA file format specifications](https://peazip.github.io/pea_help.pdf) er offentligt tilgængelige for udviklerens reference. PEA-arkiver er binære filer med fleksibel sikkerhedsmodel og redundante integritetstjek lige fra kontrolsummer til kryptografisk stærke hashes. Dette definerer tre forskellige kommunikationsniveauer, der skal kontrolleres:

 * Strømme - den faktiske outputdatastrøm, der er dannet af flere inputfiler og kan skrives til flere outputvolumener
 * Objekter - inputfiler og mapper sendt til .pea-arkivet
 * Volumes - output arkivfil, der kan spændes til brugerdefineret størrelse

Hver af disse er valgfri og kan indbygges i henhold til brugernes krav. PEA-filformatet kan gemme en enkelt strøm indeholdende ubegrænsede objekter. Hver stream er op til 2^64 bytes stor.

PEA-filer tilbyder valgfri integritetskontrol og autentificeret kryptering ved hjælp af AES i EAX- eller HMAC-tilstand, alternativt Twofish og Serpent i EAX-tilstand.

### PEA Archive Header

Arkivhovedet er på 10 bytes og er struktureret som følger.

|Bytes|Beskrivelse|
---|---|
|1 | Magisk byte felt for filformat disambiguation: $EA|
|1 | Versionsnummer|
|1 | Revisionsnummer|
|1 | Volumenkontrolskema|
|1 | Erklærer det operativsystem, hvor streamen blev bygget|
|1 | Erklærer OS dato og klokkeslæt kodning|
|1 | Erklærer objektnavn tegnkodning|
|1 | Erklærer CPU-type (kodet i 7 bit) og endianness (i msb)|
|1 | Reserveret til fremtidig brug|

## Referencer

* [PEA filformatspecifikationer](https://peazip.github.io/pea_help.pdf)

* [PEA-filformat](https://peazip.github.io/pea-file-format.html#.pea_specifications)


