{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 fails — Web Open Font Format 2.0 fails",
  "description": "Uzziniet, kas ir WOFF2 fails un API, kas var izveidot un atvērt WOFF2 failu.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-lv2"
}
},
  "lastmod": "2023-01-10"
}

## Kas ir WOFF2 fails?

WOFF2 ir fonta faila formāts, kas ir vairāk saspiesta Web Open Font Format (WOFF) versija. Tas tika izstrādāts kā veids, kā samazināt tīmekļa fontu faila lielumu, ļaujot tiem ātrāk ielādēt un izmantot mazāku joslas platumu. WOFF2 izmanto saspiešanas algoritmu, ko sauc par Brotli, lai saspiestu fontu datus, kā rezultātā failu izmēri var būt ievērojami mazāki par līdzvērtīgiem [WOFF](/font/woff/) fontiem. Šo formātu atbalsta lielākā daļa mūsdienu tīmekļa pārlūkprogrammu, tostarp Chrome, Firefox, Safari, Opera un Edge (versija 14 un jaunāka).

## WOFF2 faila formāts — vairāk informācijas

WOFF2 fonta faila iekšējā faila struktūra sastāv no vairākām dažādām daļām, ieskaitot galvenes, metadatus, tabulas direktoriju un pašus fonta datus.

 1. Galvene satur informāciju par kopējo faila formātu, tostarp versijas numuru un failā esošo tabulu skaitu.

 1. Metadatu sadaļa satur tādu informāciju kā fonta nosaukums, autortiesības un cita ar fontu saistīta informācija.

 1. Tabulu direktorijā ir informācija par dažādām tabulām, kas veido fontu, tostarp to atrašanās vieta failā un garums.

 1. Paši fonta dati ir sadalīti vairākās dažādās tabulās, no kurām katra satur konkrētu informāciju par fontu, piemēram, tā rakstzīmes un to atbilstošos glifus. Šīs tabulas var ietvert:

 * Glyf tabulā ir faktiskās fontu kontūras, tostarp katras rakstzīmes forma un izmērs.
 * Tabulā galva ir vispārīga informācija par fontu, piemēram, tā versijas numurs, dizaina izmērs utt.
 * Tabulā hmtx ir informācija par fonta metriku, tostarp rakstzīmju platumu un atrašanās vietu.
 * Katra tabula tiek saspiesta un saglabāta WOFF2 faila formātā pēc kodēšanas procesa pabeigšanas.

Struktūra kopumā ir izstrādāta, lai nodrošinātu ātru parsēšanu un dekodēšanu, lai tīmekļa pārlūkprogrammas varētu ātri un efektīvi ielādēt un parādīt fontu vietnē.

### WOFF2 galvene
WOFF galvene sastāv no identificējoša paraksta, kas norāda failā iekļauto datu veidu. WOFF galvene kopā ar tās laukiem ir šāda.

|Tips|Lauka nosaukums|Apraksts|
---|---|---|
|UInt32|paraksts |0x774F4632 'wOF2' |
|UInt32| flavor |Ievades fonta sfnt versija.|
|UInt32| garums |WOFF faila kopējais lielums.|
|UInt16| numTables |Ierakstu skaits fontu tabulu direktorijā.|
|UInt16| rezervēts |Rezervēts; iestatīts uz nulli.|
|UInt32| totalSfntSize |Kopējais lielums, kas nepieciešams nesaspiestiem fontu datiem, tostarp sfnt galvenei, direktorijam un fontu tabulām (ieskaitot pildījumu).|
|UInt32| totalCompressedSize Kopējais saspiestā datu bloka garums.|
|UInt16| majorVersion |WOFF faila galvenā versija.|
|UInt16| minorVersion |WOFF faila neliela versija.|
|UInt32| metaOffset |Nobīde uz metadatu bloku, no WOFF faila sākuma.|
|UInt32| metaLength |Saspiestā metadatu bloka garums.|
|UInt32| metaOrigLength |Nesaspiests metadatu bloka izmērs.|
|UInt32| privOffset |Nobīde uz privāto datu bloku, no WOFF faila sākuma.|
|UInt32| privLength |Privātā datu bloka garums.|


## Atsauces
 * [w3 WOFF2 faila formāts](https://www.w3.org/TR/WOFF2/)

