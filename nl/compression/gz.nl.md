{
  "date" : "2019-10-11",
  "keywords" :[ "gz-bestand", "gz-bestandsindeling", "wat is een gz-bestand", "bestand", "gz-voorbeeld", "gz-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GZ-bestandsindeling - GNU-gezipte archiefbestand",
  "description":"Meer informatie over wat een GZ-bestand is en API's die GZ-bestanden kunnen maken en openen.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GZ-bestand?

Een GZ-bestand is een gecomprimeerd archief dat is gemaakt met behulp van het standaard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) compressie-algoritme. Het kan meerdere gecomprimeerde bestanden, mappen en bestandsstubs bevatten. Dit formaat is oorspronkelijk ontwikkeld om compressie-indelingen op UNIX-systemen te vervangen. en is nog steeds een van de meest voorkomende archieftypen op Linux-systemen. Toepassingen zoals [WinZip](https://www.winzip.com/en/) kunnen GZ-bestanden openen om de inhoud ervan te bekijken op zowel Windows als MacOS.

## GZ-bestandsindeling - Meer informatie

Gzip gebruikt het [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algoritme voor het comprimeren van archief en verschilt van het [ZIP](/nl/compression/zip/) archiefformaat bij het toepassen van het compressiealgoritme op het volledige archief in plaats van individuele bestanden. De GZIP-bestandsformaatspecificaties versie 4.3 gepubliceerd door Internet Engineering Task Force (IETF) bevat gedetailleerde informatie over het bestandsformaat. Het bestandsformaat bestaat uit:

* Bestandskoptekst
* Optionele kopteksten
* Gecomprimeerde gegevens
* Bestandsvoettekst

## GZ-bestandskop ##

De GZ-bestandskop bestaat als volgt uit 10 bytes:

|Offset|Grootte|Waarde|Beschrijving
---|---|---|---|
|0|2|0x1f 0x8b|Magisch nummer dat bestandstype identificeert
|2|1| |Compressiemethode * 0-7 (gereserveerd) * 8 (leeglopen)
|3|1| |Bestandsvlaggen
|4|4| |32-bits tijdstempel
|8|1| |Compressie vlaggen
|9|1| |Besturingssysteem-ID

### Bestandsvlaggen ###

|Waarde|Identificatie|Beschrijving
---|---|---|
|0x01|FTEXT|Indien ingesteld moeten de niet-gecomprimeerde gegevens worden behandeld als tekst in plaats van binaire gegevens. Deze vlag verwijst naar end-of-line conversie voor cross-platform tekstbestanden, maar dwingt deze niet af.
|0x02|FHCRC|Het bestand bevat een header checksum (CRC-16)
|0x04|FEXTRA|Het bestand bevat extra velden
|0x08|FNAME|Het bestand bevat een originele bestandsnaamstring
|0x10|FCOMMENT|Het bestand bevat commentaar
|0x20| |Gereserveerd
|0x40| |Gereserveerd
|0x80| |Gereserveerd

### Besturingssysteem ###

|Waarde|Beschrijving
---|---|
|0|FAT-bestandssysteem (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (of OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS-bestandssysteem (OS/2, NT)
|7|Macintosh
|8|Z-systeem
|9|CP/M
|10|TOPS-20
|11|NTFS-bestandssysteem (NT)
|12|QDOS
|13|Eikel RISCOS
|255|onbekend

## GZ optionele headers ##

De optionele extra headers zijn die zoals aangegeven door de bestandsvlaggen en bevatten informatie zoals de originele bestandsnaam, extra velden, opmerkingen en header checksum.

## Gecomprimeerde gegevens ##

Dit gedeelte bevat de gecomprimeerde gegevens met behulp van het DEFLATE-compressiealgoritme.

## GZ-bestandsvoettekst ##

De voettekst van het bestand is 8 bytes groot en bevat de volgende informatie.

|Offset|Grootte|Beschrijving
---|---|---|
|0|4|Checksum (CRC-32)
|4|4|Ongecomprimeerde gegevensgrootte in bytes

## Referenties ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP-bestandsformaatspecificatie](https://datatracker.ietf.org/doc/html/rfc1952), door IETF.

