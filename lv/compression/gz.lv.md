{
  "date": "2019-10-11",
  "keywords": [
"gz failu",
"gz faila formātā",
"kas ir gz fails",
"failu",
"gz piemērs",
"gz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GZ faila formāts — GNU ZIP arhīva fails",
  "description": "Uzziniet, kas ir GZ fails un API, kas var izveidot un atvērt GZ failus.",
  "linktitle": "GZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-g-lvz"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir GZ fails?

GZ fails ir saspiests arhīvs, kas tiek izveidots, izmantojot standarta [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) saspiešanas algoritmu. Tajā var būt vairāki saspiesti faili, direktoriji un failu stubsti. Šis formāts sākotnēji tika izstrādāts, lai aizstātu saspiešanas formātus UNIX sistēmās. un joprojām ir viens no visizplatītākajiem arhīvu veidiem Linux sistēmās. Tādas lietojumprogrammas kā [WinZip](https://www.winzip.com/en/) var atvērt GZ failus, lai skatītu to saturu gan operētājsistēmā Windows, gan MacOS.

## GZ faila formāts — vairāk informācijas

Gzip arhīva saspiešanai izmanto algoritmu [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE), un tas atšķiras no [ZIP](/compression/zip/) arhīva formāta, izmantojot saspiešanas algoritmu visam arhīvam, nevis atsevišķiem failiem. Internet Engineering Task Force (IETF) publicētajā GZIP faila formāta specifikāciju versijā 4.3 ir ietverta detalizēta informācija par faila formātu. Faila formāts sastāv no:

* Faila galvene

* Izvēles galvenes

* Saspiesti dati

* Faila kājene


## GZ faila galvene ##

GZ faila galvene sastāv no 10 baitiem šādi:

|Nobīde|Izmērs|Vērtība|Apraksts
---|---|---|---|
|0|2|0x1f 0x8b|Maģisks numurs, kas identificē faila tipu
|2|1| |Compression Method * 0-7 (rezervēts) * 8 (deflācija)
|3|1| |Failu karogi
|4|4| |32 bitu laikspiedols
|8|1| |Kompresijas karodziņi
|9|1| |Operētājsistēmas ID

### Failu karodziņi ###

|Vērtība|Identifier|Apraksts
---|---|---|
|0x01|FTEXT|Ja iestatīts, nesaspiestie dati ir jāapstrādā kā teksts, nevis bināri dati. Šis karodziņš norāda uz rindas beigu konvertēšanu starpplatformu teksta failiem, bet neveicina to.
|0x02|FHCRC|Fails satur galvenes kontrolsummu (CRC-16)
|0x04|FEXTRA|Fails satur papildu laukus
|0x08|FNAME|Fails satur oriģinālā faila nosaukuma virkni
|0x10|FCOMMENT|Fails satur komentāru
|0x20| |Rezervēts
|0x40| |Rezervēts
|0x80| |Rezervēts

### Operētājsistēma ###

|Vērtība|Apraksts
---|---|
|0|FAT failu sistēma (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (vai OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|HPFS failu sistēma (OS/2, NT)
|7|Macintosh
|8|Z-sistēma
|9|KP/M
|10|TOPS-20
|11|NTFS failu sistēma (NT)
|12|QDOS
|13|Acorn RISCOS
|255|nezināms

## GZ izvēles galvenes ##

Izvēles papildu galvenes ir tās, kas apzīmētas ar faila karodziņiem, un ietver tādu informāciju kā sākotnējais faila nosaukums, papildu lauki, komentāri un galvenes kontrolsumma.

## Saspiesti dati ##

Šajā sadaļā ir saspiestie dati, izmantojot saspiešanas algoritmu DEFLATE.

## GZ faila kājene ##

Faila kājenes izmērs ir 8 baiti, un tajā ir šāda informācija.

|Nobīde|Izmērs|Apraksts
---|---|---|
|0|4|Kontrolsumma (CRC-32)
|4|4|Nesaspiesta datu lieluma vērtība baitos

## Atsauces Nr.

* [gzip — Wikipedia](https://en.wikipedia.org/wiki/Gzip)

* [RFC1952: GZIP faila formāta specifikācija](https://datatracker.ietf.org/doc/html/rfc1952), IETF.


