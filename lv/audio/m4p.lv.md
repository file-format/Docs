{
  "date": "2021-06-09",
  "keywords": [
"m4p",
"mp3",
"failu",
"pagarinājumu",
"formātā",
"kas ir m4p faila formāts",
"mūzika",
"m4p faila formātā",
"M4b pret MP3",
"m4p faila formāta specifikācija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par M4P failu formātu un API, kas var izveidot, konvertēt un atvērt M4P failus.",
  "title": "M4P — MPEG-4 audiogrāmatas faila formāts",
  "linktitle": "M4P",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-lvp"
}
},
  "lastmod": "2021-06-09"
}

## Kas ir M4P fails?
Fails ar paplašinājumu .m4p ir audio fails, kas parasti ir pieejams lejupielādei Apple iTunes veikalā. Citiem vārdiem sakot, mēs varam teikt, ka M4P ir AAC fails, taču tas ir aizsargāts pret kopēšanu, izmantojot digitālo tiesību pārvaldību (DRM). Tas nozīmē, ka M4P failus var atskaņot tikai autorizētās sistēmās vai ierīcēs. Parasti M4P faili ir raksturīgi Apple multivides ierīcēm. Tāpēc šos failus var atskaņot tikai Apple Macbook datoros, aplādes un viedtālruņos, piemēram, iPhone 6 vai iPhone 7.

## M4P faila formāts
M4P apzīmē MPEG 4 Protected (audio), un tas kodē audio ar uzlabotu audio kodeku (AAC) un aizsargā failu no nesankcionētas faila izmantošanas. Šis faila formāts parasti tiek uzskatīts par iTunes mūzikas veikala audio faila formātu. Apple izmanto savu FairPlay digitālo tiesību pārvaldības (DRM) sistēmu, lai aizsargātu M4P failus. FairPlay DRM ir balstīta uz Veridisc izstrādāto tehnoloģiju. Tās aizsardzības mehānisms darbojas, šifrējot AAC audio straumi, izmantojot AES šifrēšanu. Lietotājs saņem galveno atslēgu, kas tiek piešķirta viņa kontam atšifrēšanai. Šis faila formāts tika ieviests kā MP3 faila formāta aizstājējs, jo sākotnēji MP3 nebija paredzēts kā audio fails, bet gan kā III slānis MPEG 1 vai 2 video failā.


## M4P faila formāta specifikācijas

Līdzīgi kā [M4A](/audio/m4a/), M4P faili arī sastāv no secīgiem gabaliem. Katrai daļai ir 8 baitu galvene, un tā ir sadalīta šādi:
- 4 baitu gabala lielums (lielais baits, vispirms augstais baits)
- 4 baitu gabala tips — viens no iepriekš definētiem parakstiem: mdat, moov, pnot, moof, udta, uuid, free, skip, ftyp, jP2, wide, load, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT, scpt , ctab, ssrc.

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. M4P, kas definēts pēc apakštipa, kam jābūt M4P_.

Atkārtojot gabalus, līdz tiek atklāts nezināma veida gabals, tas veidos M4P (MPEG-4 Audio) failu.

## Atsauces Nr.

* [MPEG-4 14. daļa — Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14. daļas audio (M4A,M4B,M4P) formāta un atkopšanas piemērs](https://www.file-recovery.com/m4a-signature-format.htm)


