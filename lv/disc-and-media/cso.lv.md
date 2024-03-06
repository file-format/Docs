{
  "date": "2021-08-09",
  "keywords": [
"cso fails",
"cso faila formātā",
"kas ir cso fails",
"failu",
"cso piemērs",
"cso faila paplašinājums",
"pagarinājumu",
"formātā",
"iso",
"DAX saspiešana"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CSO failu formātu un API, kas var izveidot un atvērt CSO failus.",
  "title": "CSO — saspiests ISO diska attēls",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-lvo"
}
},
  "lastmod": "2021-08-09"
}

## Kas ir CSO fails?

Fails ar paplašinājumu .cso ir saspiests ISO attēla fails. CSO ir alternatīva DAX saspiešanas metodei; pazīstams arī kā CISO; bija pirmā metode [ISO](/compression/iso/) failu saspiešanai, un parasti tā ir ieteicamā metode PlayStation Portable satura arhivēšanai. Šajā formātā tiek izmantota saspiešanas deflācija, kas var ietvert līdz deviņiem saspiešanas slāņiem. Attēlu izveidošanai tiek izmantota programmatūra, piemēram, Prometheus un YACC.

## CSO faila formāts

CSO faila formāts bija pirmā ISO saspiešanas metode, lai ietaupītu vairāk vietas atmiņā. Uzlabojumi tika veikti laiku pa laikam, lai nodrošinātu labāku saspiešanu. CSO izmanto Deflate saspiešanu ar deviņiem iepriekš iestatītu līmeņu līmeņiem, parasti katrs līmenis var apstrādāt 2 KiB blokus atsevišķi. Lai gan augstākie saspiešanas līmeņi var palēnināt un paildzināt ielādes laiku programmatūrā, kas lielā mērā ir atkarīga no diska straumēšanas, arī zemākie līmeņi var veikt ievērojamu saspiešanu.

### CSO failu struktūra

CSO faila formātā ir 24 baitu galvene, datu bloki un indeksa tabula. Tiek pieņemts Little-endian laukiem, kas ir lielāki par baitu. PlayStation Portable arhitektūras galīgums ir norādīts zemāk.

#### Galvene

| Nobīde (baiti) | Vārds | Izmērs (baitos) | Mērķis |
----------|----------|--------------|---------|
| 0x0 | Maģija | 4 | Vienmēr CISO vai 0x4F534943, lasot kā 32 bitu veselu skaitli. Šis lauks tiek izmantots, lai identificētu CSO failu. Ņemiet vērā, ka šis lauks var atšķirties citiem CSO atvasinājumiem, piemēram, ZSO izmantoja maģisko kodu ZISO. |
| 0x4 | Virsraksta izmērs | 4 | Sākotnējam CSO v1” faila formātam šis lauks tiek ignorēts, un tāpēc tam nav jābūt precīzam. Tomēr v2 un ZSO formātā šim laukam vienmēr jābūt 0x18 (24 baiti). |
| 0x8 | Nesaspiests izmērs | 8 | Sākotnējā nesaspiestā ISO lielums baitos. |
| 0x10 | Bloka izmērs | 4 | Katra datu bloka lielums baitos pirms saspiešanas. Parasti 2048 baiti, kas ir tāds pats kā katra ISO 9660 sektora lielums. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. Formātam v2 tam ir jābūt 2. Turklāt ZSO formātam tam ir jābūt 1. |
| 0x15 | Indeksa izlīdzināšana | 1 | Katra indeksa ieraksta līdzinājums, kas norādīts bitos. |
| 0x16 | Rezervēts | 2 | Šis lauks nav izmantots. Formātā v1” šis lauks tiek ignorēts, un tajā var būt patvaļīgas vērtības. Formātā v2” šim laukam ir jābūt nullei. |

#### Indeksu tabula

Indeksa tabulā ir vairāki 4 baitu ieraksti, kas norāda katra datu bloka pozīciju, un papildu, pēdējais ieraksts, kas norāda uz faila beigām.
Katra ieraksta saturs ir šāds:
| Bits | Garums | Maska | Vārds | Mērķis |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Pozīcija | Šis lauks, kad tas tiek pārvietots pa kreisi ar indeksa līdzinājumu, kas norādīts galvenē, parāda pozīciju, kurā sākas datu bloks. |
| 31 | 1 | 0x80000000 | Kompresijas veids | ZSO formātam ir līdzīga semantika, tikai tas, ka 0 apzīmē LZ4, nevis Deflate. v2 formātā. Bloks netieši tiek uzskatīts par nesaspiestu, ja bloka izmērs ir vienāds ar faila galvenē norādīto bloka izmēru vai lielāks par to. |

#### Datu bloki

Datu bloki sastāv no nesaspiestiem vai saspiestiem datiem. Bloka lielumu aprēķina, iegūstot tā pozīciju un pēc tam atņemot to no nākamā bloka pozīcijas. Ja indeksa līdzinājums ir lielāks par nulli, iespējams, ka bloka lielums ir lielāks nekā tajā glabātie dati.


## Atsauces 

* N/A


