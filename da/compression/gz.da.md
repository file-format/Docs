{
  "date": "2019-10-11",
  "keywords": [
"gz filen",
"gz filformat",
"hvad er en gz-fil",
"fil",
"gz eksempel",
"gz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZ-filformat - GNU Zipped Archive File",
  "description": "Lær om, hvad en GZ-fil og API'er er, der kan oprette og åbne GZ-filer.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-daz"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GZ fil?

En GZ-fil er et komprimeret arkiv, der er oprettet ved hjælp af standardkompressionsalgoritmen [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Det kan indeholde flere komprimerede filer, mapper og filstubber. Dette format blev oprindeligt udviklet til at erstatte komprimeringsformater på UNIX-systemer. og er stadig en af de mest almindelige arkivtyper på Linux-systemer. Programmer såsom [WinZip](https://www.winzip.com/en/) kan åbne GZ-filer for at se indholdet på både Windows og MacOS.

## GZ-filformat - flere oplysninger

Gzip bruger [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE)-algoritmen til komprimering af arkiv og adskiller sig fra [ZIP](/compression/zip/)-arkivformatet ved at anvende komprimeringsalgoritmen på komplet arkiv frem for individuelle filer. GZIP-filformatspecifikationerne version 4.3 udgivet af Internet Engineering Task Force (IETF) indeholder detaljerede oplysninger om filformatet. Filformatet består af:

* Filoverskrift

* Valgfri overskrifter

* Komprimerede data

* Filsidefod


## GZ-filoverskrift ##

GZ-filheaderen består af 10 bytes som følger:

|Offset|Størrelse|Værdi|Beskrivelse
---|---|---|---|
|0|2|0x1f 0x8b|Magisk nummer, der identificerer filtype
|2|1| |Compression Method * 0-7 (Reserveret) * 8 (Tøm for luft)
|3|1| |Fil flag
|4|4| |32-bit tidsstempel
|8|1| |Kompressionsflag
|9|1| | Operativsystem ID

### Filflag ###

|Værdi|Identifier|Beskrivelse
---|---|---|
|0x01|FTEXT|Hvis indstillet skal de ukomprimerede data behandles som tekst i stedet for binære data. Dette flag antyder end-of-line-konvertering for tekstfiler på tværs af platforme, men håndhæver det ikke.
|0x02|FHCRC|Filen indeholder en header checksum (CRC-16)
|0x04|FEXTRA|Filen indeholder ekstra felter
|0x08|FNAME|Filen indeholder en original filnavnstreng
|0x10|FCOMMENT|Filen indeholder kommentar
|0x20| |Reserveret
|0x40| |Reserveret
|0x80| |Reserveret

### Operativ system ###

|Værdi|Beskrivelse
---|---|
|0|FAT-filsystem (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (eller OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS-filsystem (OS/2, NT)
|7|Macintosh
|8|Z-system
|9|CP/M
|10|TOPS-20
|11|NTFS-filsystem (NT)
|12|QDOS
|13|Acorn RISCOS
|255|ukendt

## GZ valgfri overskrifter ##

De valgfrie ekstra overskrifter er dem, som er angivet med filflag og inkluderer information såsom det originale filnavn, ekstra felter, kommentarer og overskriftskontrolsum.

## Komprimerede data ##

Dette afsnit indeholder de komprimerede data ved hjælp af DEFLATE-komprimeringsalgoritmen.

## GZ File Footer ##

Filfoden er 8 bytes stor og indeholder følgende oplysninger.

|Offset|Størrelse|Beskrivelse
---|---|---|
|0|4|Tjeksum (CRC-32)
|4|4|Ukomprimeret datastørrelsesværdi i bytes

## Referencer ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP-filformatspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), af IETF.


