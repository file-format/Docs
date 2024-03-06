{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Nuvo Media's Rocket eBook ierīce",
"failu",
"pagarinājumu",
"formātā",
"e-grāmata"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par RB faila formātu Nuvo Media's Rocket eBook ierīcei un API, kas var izveidot un atvērt RB failus.",
  "title": "RB — raķešu e-grāmatu fails",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-lvb"
}
},
  "lastmod": "2021-03-08"
}

## Kas ir RB fails?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Lai gan Rocket eBook spēj attēlot attēlus, bet tikai melnbaltā displejā. Tam ir 106 dpi vai 480 x 320 pikseļu ekrāns ar 4,5 x 3 collu skārienekrānu. Rocket eBook tiek savienots ar datoru, izmantojot seriālā porta savienojumu, lai lejupielādētu e-grāmatas RB faila formātā. RB faili var izmantot DRM, taču šī tehnoloģija netiek izmantota mūsdienu e-grāmatās. RB fails parasti satur HTML failu ar attēliem un pseido-OPF failu ar visiem metadatiem (.info).

## RB faila formāta ## tehniskā specifikācija

Faila pirmajos 4 baitos parādās maģisks skaitlis (heksadecimālā formā): B0 0C B0 0C.

Šķiet, ka nākamie divi baiti ir versijas numurs, piemēram, 02 00, kas apzīmē galveno versiju 2 un mazo versiju 0.

Nākamajos četros baitos ir teksts NUVO, kam seko 4 baiti 00h.

The next 4-byte is the date when the book was created, encoded as an int16. Tas liek mums kompensēt 0Eh. ORocketLibrary vecajā versijā bija kodēta gada pilna vērtība (ti, 1999. gads bija CF 07, 2000. gads bija D0 07). Jaunākajā versijā tm_year tiek saglabāts burtiski, ti, 100 2000. gadam (64 00). Pēc gada nāk int8, kas apzīmē 1 relatīvo mēneša skaitli, un int8, kas apzīmē mēneša dienu.

Nākamie 6 baiti ir 00h. Laika iestatīšanai tos var rezervēt.

Satura rādītāja absolūtā nobīde ir ietverta int32 ar nobīdi 18h.

Pēc šī ir int32, kas satur .rb faila garumu. To izmanto, lai noteiktu, vai faili ir vai nav.

Šķiet, ka visa šī baitu daļa (no 20 h līdz 128 h) ir nepieciešama tikai šifrētam nosaukumam. Nešifrētos nosaukumos tie vienmēr ir nulle.

Vairumā gadījumu satura rādītājs seko (pie 128. nobīdes). Tas sākas ar int32 skaitu lapu ierakstiem (.rb-faila sadaļas) Pakalpojumā. Katrs ieraksts sastāv no nosaukuma (nulle polsterēts līdz 32 baitiem), kam seko 3 int32: datu segmenta garums, pozīcija .rb failā un šī ieraksta karodziņš. Šobrīd zināmās vērtības ir: 1 (šifrēta), 2 (informācijas lapa) un 8 (deflācija). Visi nosaukumi pēc vajadzības ir pielāgoti, lai nodrošinātu, ka tie visi ir unikāli.

## Atsauces

* [E-lasītājs — MobileRead](https://en.wikipedia.org/wiki/E-reader)


