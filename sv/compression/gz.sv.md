{
  "date" : "2019-10-11",
  "keywords" :[ "gz-fil", "gz-filformat", "vad är en gz-fil", "fil", "gz-exempel", "gz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ File Format - GNU Zipped Archive File",
  "description":"Läs mer om vad en GZ-fil och API:er är som kan skapa och öppna GZ-filer.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är GZ fil?

En GZ-fil är ett komprimerat arkiv som skapas med hjälp av standardkomprimeringsalgoritmen [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Den kan innehålla flera komprimerade filer, kataloger och filstubbar. Detta format utvecklades ursprungligen för att ersätta komprimeringsformat på UNIX-system. och är fortfarande en av de vanligaste arkivtyperna på Linux-system. Program som [WinZip](https://www.winzip.com/en/) kan öppna GZ-filer för att se innehållet på både Windows och MacOS.

## GZ-filformat - Mer information

Gzip använder algoritmen [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) för komprimering av arkiv och skiljer sig från arkivformatet [ZIP](/sv/compression/zip/) när det gäller att tillämpa komprimeringsalgoritmen på komplett arkiv snarare än enskilda filer. GZIP-filformatsspecifikationerna version 4.3 publicerad av Internet Engineering Task Force (IETF) innehåller detaljerad information om filformatet. Filformatet består av:

* Filhuvud
* Valfria rubriker
* Komprimerad data
* Filsidfot

## GZ-filhuvud ##

GZ-filhuvudet består av 10 byte enligt följande:

|Offset|Storlek|Värde|Beskrivning
---|---|---|---|
|0|2|0x1f 0x8b|Magiskt nummer som identifierar filtyp
|2|1| |Kompressionsmetod * 0-7 (Reserverad) * 8 (Tömma luft)
|3|1| | Arkiv Flaggor
|4|4| |32-bitars tidsstämpel
|8|1| |Kompressionsflaggor
|9|1| |Operativsystem-ID

### Filflaggor ###

|Värde|Identifierare|Beskrivning
---|---|---|
|0x01|FTEXT|Om inställt måste okomprimerad data behandlas som text istället för binär data. Den här flaggan antyder radslutkonvertering för plattformsoberoende textfiler men upprätthåller den inte.
|0x02|FHCRC|Filen innehåller en huvudkontrollsumma (CRC-16)
|0x04|FEXTRA|Filen innehåller extra fält
|0x08|FNAME|Filen innehåller en originalfilnamnssträng
|0x10|FCOMMENT|Filen innehåller kommentarer
|0x20| |Reserverad
|0x40| |Reserverad
|0x80| |Reserverad

### Operativ system ###

|Värde|Beskrivning
---|---|
|0|FAT-filsystem (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (eller OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS-filsystem (OS/2, NT)
|7|Macintosh
|8|Z-System
|9|CP/M
|10|TOPS-20
|11|NTFS-filsystem (NT)
|12|QDOS
|13|Ekollon RISCOS
|255|okänd

## GZ valfria rubriker ##

De valfria extra rubrikerna är de som anges av filflaggorna och inkluderar information som det ursprungliga filnamnet, extra fält, kommentarer och rubrikkontrollsumma.

## Komprimerad data ##

Det här avsnittet innehåller komprimerad data med hjälp av DEFLATE-komprimeringsalgoritmen.

## GZ-filsidfot ##

Filsidfoten är 8 byte stor och innehåller följande information.

|Offset|Storlek|Beskrivning
---|---|---|
|0|4|Kontrollsumma (CRC-32)
|4|4|Okomprimerat datastorleksvärde i byte

## Referenser ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP-filformatspecifikation](https://datatracker.ietf.org/doc/html/rfc1952), av IETF.

