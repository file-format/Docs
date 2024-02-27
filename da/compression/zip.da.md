{
  "date": "2019-12-09",
  "keywords": [
"zip-fil",
"zip-filformat",
"hvad er en zip-fil",
"fil",
"zip eksempel",
"zip filudvidelse",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIP",
  "description": "Hvad er en ZIP-fil og API'er, der kan oprette og åbne ZIP-filer.",
  "linktitle": "ZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-dap"
}
},
  "lastmod": "2019-12-09"
}

## Hvad er en ZIP-fil? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## Kort historie om ZIP-filformat

Historien om ZIP-filformat går tilbage til tilfældet af en retssag, som System Enhancement Associates (SEA) har indført mod PKWARE for at bruge dets ARC-værktøj uden tilladelse til dets varemærke og ophavsretten til produktets udseende og brugergrænseflade. Før dette havde Phil Katz omskrevet SEA's kildekode og frigivet PKXARC, en ARC-udtrækker, og PKARC, en filkomprimering, som freeware til MS-DOS baserede systemer. Da PKWARE tabte til retssagen, kunne PKWARE ikke bruge noget, der var relateret til ARC længere. Det er her, oprettelsen af en ny filkomprimering blev til, navngivet som ZIP, som blev gjort til en del af PKZIP-værktøjet hos PKWARE, Inc.

Katz frigav ZIP-filformatspecifikationerne til det offentlige domæne, mens han beholdt de ejendomsretlige rettigheder over sit komprimerings- og udtræksværktøj, dvs. PKZIP. ZIP-komprimeringssystemet var (og er) i stand til at arkivere filer i en mappe ved hjælp af en 32-bit cyklisk redundanskontrol ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algoritme til at komprimere filstørrelser. I modsætning til ARC indeholdt .ZIP-mapper en mappefil, der spillede rollen som en kryptografs kodebog, der indeholdt den nødvendige information til at gengive de komprimerede filer.

## Understøttede komprimeringsmetoder i ZIP

I henhold til .ZIP-filformatspecifikationerne understøttes følgende komprimeringsmetoder.

* Store - indebærer ingen komprimering

* Krympe

* Reduktion (Dette indebærer kompressionsfaktorer fra niveau 1 til niveau 4)

* Implodere

* Tøm luften ud

* Deflat64

* BZIP2

* LZMA (EFS)

* WavPack

* PPMd version I, Rev 1


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## ZIP-filformatspecifikationer

ZIP-filer har mulighed for at gemme flere filer ved hjælp af forskellige komprimeringsteknikker, mens de på samme tid understøtter lagring af en fil uden nogen form for komprimering. Hver fil gemmes/komprimeres individuelt, hvilket hjælper med at udpakke dem, eller tilføje nye, uden at anvende komprimering eller dekomprimering til hele arkivet.

### Samlet ZIP-filformat

Hver Zip-fil er struktureret på følgende måde:


|ZIP-filformat
---|
|Lokal filoverskrift 1
|Fildata 1
|Databeskrivelse 1
|Lokal filoverskrift 2
|Fildata 2
|Databeskrivelse 2
| ....
| ....
|Lokal filoverskrift N
|Fil data N
|Databeskrivelse N
|Arkivdekrypteringshoved
|Arkiv ekstra datapost
|Central bibliotek

ZIP-filformat bruger 32-bit CRC-algoritme til arkivering. For at gengive de komprimerede filer, har et ZIP-arkiv en mappe i sin ende, der gemmer indtastningen af de indeholdte filer og deres placering i arkivfilen. Det spiller således rollen som kodning til indkapsling af information, der er nødvendig for at gengive de komprimerede filer. ZIP-læsere bruger biblioteket til at indlæse listen over filer uden at læse hele ZIP-arkivet. Formatet beholder to kopier af mappestrukturen for at give større beskyttelse mod tab af data.

Hver fil i et ZIP-arkiv er repræsenteret som en individuel post, hvor hver post består af en lokal filoverskrift efterfulgt af de komprimerede fildata. Kataloget i slutningen af arkivet indeholder referencerne til alle disse filposter. ZIP-fillæsere bør undgå at læse de lokale filoverskrifter, og alle slags fillister bør læses fra biblioteket. Denne mappe er den eneste kilde til gyldige filposter i arkivet, da filer også kan tilføjes mod slutningen af arkivet. Det er derfor, hvis en læser læser lokale overskrifter i et ZIP-arkiv fra begyndelsen, kan den læse ugyldige (slettede) poster, ligesom de ikke er en del af den mappe, der slettes fra arkivet.

Rækkefølgen af filposterne i det centrale bibliotek behøver ikke at falde sammen med rækkefølgen af filposterne i arkivet.

### ZIP-filposter

Indgange i ZIP-fil er arrangeret efter hinanden, hvor hver post består af:

* Lokal filoverskrift

* Valgfri ekstra datafelter

* Brugerdata (valgfrit komprimeret/valgfrit krypteret)


Den lokale filoverskrift for hver post repræsenterer information om filen, såsom kommentar, filstørrelse og filnavn. De ekstra datafelter (valgfrit) kan rumme oplysninger om udvidelsesmuligheder i ZIP-formatet.

#### Lokal filoverskrift

Den lokale filoverskrift har en specifik feltstruktur bestående af multi-byte værdier. Alle værdierne er gemt i little-endian byte rækkefølge, hvor feltlængden tæller længden i bytes. Alle strukturerne i en ZIP-fil bruger 4-byte signaturer for hver filindgang. Slutningen af den centrale bibliotekssignatur er 0x06054b50 og kan skelnes ved hjælp af sin egen unikke signatur. Følgende er rækkefølgen af oplysninger, der er gemt i lokal filoverskrift.


|Offset|Bytes|Beskrivelse
---|---|---|
|0|4|Lokal filoverskriftssignatur # 0x04034b50 (læses som et lille-endian tal)
|4|2|Version nødvendig for at udtrække (minimum)
|6|2|Bitflag til generelle formål
|8|2|Kompressionsmetode
|10|2|Sidste ændringstid for fil
|12|2|Fil sidste ændringsdato
|14|4|CRC-32
|18|4|Komprimeret størrelse
|22|4|Ukomprimeret størrelse
|26|2|Længde af filnavn (n)
|28|2|Ekstra feltlængde (m)
|30|n|Filnavn
|30+n|m|Ekstra felt

#### Central Directory File Header


|Offset|Bytes|Beskrivelse
---|---|---|
|0|4|Central mappe fil header signatur # 0x02014b50
|4|2|Version lavet af
|6|2|Version nødvendig for at udtrække (minimum)
|8|2|Bitflag til generelle formål
|10|2|Kompressionsmetode
|12|2|Sidste ændringstid for fil
|14|2|Fil sidste ændringsdato
|16|4|CRC-32
|20|4|Komprimeret størrelse
|24|4|Ukomprimeret størrelse
|28|2|Længde af filnavn (n)
|30|2|Ekstra feltlængde (m)
|32|2|Længde af filkommentar (k)
|34|2|Disknummer, hvor filen starter
|36|2|Interne filattributter
|38|4|Eksterne filattributter
|42|4|Relativ forskydning af lokal filoverskrift. Dette er antallet af bytes mellem starten af den første disk, hvorpå filen opstår, og starten af den lokale filoverskrift. Dette gør det muligt for software, der læser den centrale mappe, at finde filens position inde i ZIP-filen.
|46|n|Filnavn
|46+n|m|Ekstra felt
|46+n+m|k|Filkommentar

#### Slut på Central Directory Record


|Offset|Bytes|Beskrivelse
---|---|---|
|0|4|Slut på central bibliotekssignatur # 0x06054b50
|4|2|Nummer på denne disk
|6|2|Disk, hvor den centrale mappe starter
|8|2|Antal centrale mappeposter på denne disk
|10|2|Samlet antal centrale katalogposter
|12|4|Størrelse af central mappe (bytes)
|16|4|Forskydning af start af central mappe, i forhold til start af arkiv
|20|2|Kommentarlængde (n)
|22|n|Kommentar

## Referencer

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struktur af PKZip-fil](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


