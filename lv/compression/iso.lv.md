{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - diska attēla faila formāts",
  "description":"Kas ir ISO fails un API, kas var izveidot un atvērt ISO failus.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso-lv",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Kas ir ISO fails?

Fails ar paplašinājumu .iso ir nesaspiests arhīva diska attēla fails, kas attēlo visu optiskā diska, piemēram, CD vai DVD, datu saturu. Pamatojoties uz standartu [ISO-9660](https://www.iso.org/standard/17505.html), ISO attēla faila formāts satur diska datus un tajā saglabāto failu sistēmas informāciju. ISO failu spēja saturēt precīzu satura kopiju padara to par ideālu faila tipu kompaktdisku/DVD disku kopiju izveidei, un tos galvenokārt izmanto, lai saglabātu sāknēšanas datus instalēšanai. Vairumā gadījumu ISO faili tiek ierakstīti USB/CD/DVD diskā kā sāknējams saturs, lai palaistu mašīnu instalēšanai. ISO failiem ir MIME tipa lietojumprogramma/x-iso9660-image.

## ISO faila formāts

ISO faila formāts nav līdzīgs citiem konteinera failu formātiem, lai gan tas arhivē norādīto datu saturu. Arhīvs tiek izveidots kā binārs fails ar precīzu satura un failu sistēmas informācijas struktūru. ISO faila formātu [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) apraksta šādi.

### ISO faila augstākā līmeņa struktūra

Kopējā faila struktūra sastāv no:

 * Sistēmas apgabals — 32 768 baiti, un to neizmanto ISO_9660
 * Datu apgabals - sastāv no apjoma deskriptoru kopas un ceļa tabulām, direktorijiem un failiem

### Skaļuma deskriptora komplekts

Datu apgabals sākas ar apjoma deskriptoru kopu, viena vai vairāku apjoma deskriptoru kopu, kas beidzas ar apjoma deskriptoru kopas beigu. Tie kopā darbojas kā datu apgabala galvene, aprakstot tā saturu (līdzīgi BIOS parametru blokam, ko izmanto FAT, HPFS un NTFS formatēti diski).

Skaļuma deskriptora kopa ir tāda, kā parādīts zemāk.

|Skaļuma deskriptoru kopa|
---|
|Skaļuma deskriptors #1|
|...|
|Skaļuma deskriptors #N|
|Volume desscriptor set terminator|

#### Sējuma deskriptors

Katrs apjoma deskriptors ir 2048 baiti liels, un tam ir šāda struktūra:

|Daļa |Tips |Identifier |Versija |Dati|
---|---|---|---|---|
|Izmērs |1 baits |5 baiti (vienmēr 'CD001') |1 baits (vienmēr 0x01) |2041 baits|

## Atsauces

* [Optiskā diska attēls — Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)

* [Failu paraksti](https://www.garykessler.net/library/file_sigs.html)

* [ISO 9660 — Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)


