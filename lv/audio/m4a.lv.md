{
  "date": "2021-04-26",
  "keywords": [
"m4a",
"mp3",
"failu",
"pagarinājumu",
"formātā",
"kas ir m4a faila formāts",
"mūzika",
"m4a faila formātā",
"M4A pret MP3",
"m4a faila formāta specifikācija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par M4A faila formātu un API, kas var izveidot, konvertēt un atvērt M4A failus.",
  "title": "M4A — MPEG-4 audio fails",
  "linktitle": "M4A",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-lva"
}
},
  "lastmod": "2021-04-26"
}

## Kas ir M4A fails?

**M4A faila formāts** ir audio fails, kas izveidots, izmantojot AAC (Advanced Audio Coding), ko sauc par kompresiju ar zaudējumiem. Vārds M4A saīsināts kā MPEG 4 Audio. Šiem audio failiem parasti ir .m4a faila paplašinājums. Tas jo īpaši attiecas uz neaizsargātu saturu. Tajā var saglabāt dažāda veida audio saturu, piemēram, audiogrāmatas, dziesmas un aplādes. M4A parasti tiek realizēts kā uzlabots formāts nekā MP3, kas parasti nebija paredzēts tikai audio. Tas ir tikai audio slānis MPEG 1 vai 2 video failos.

M4A formātu šifrē FairPlay Digital Rights Management, jo tie tika pārdoti, izmantojot iTunes Store, izmantojot paplašinājumu .m4p. Apple iPhone tālruņos zvana signāliem tiek izmantots MPEG-4 audio, bet šajos audio failos tiek izmantots paplašinājums .m4r.


## M4A pret MP3

Gan M4A, gan [MP3](/audio/mp3/) ir tikai audio failu formāti.

**M4A**: labāk nekā MP3 kvalitātes un izmēra ziņā, ja tas ir kodēts ar tādu pašu bitu pārraides ātrumu. Faila paplašinājums .m4a ir tik izplatīts, jo Apple tos ir izmantojis iTunes mūzikas veikalā. M4A ir audio fails, kas ir saspiests, izmantojot MPEG-4 tehnoloģiju; algoritms kompresijai ar zaudējumiem. Tas būtībā ir saistīts ar MPEG-4 audio slāni”, faili ar paplašinājumu .m4a ir MPEG-4 filmu audio slānis. Tas ir paredzēts, lai apsteigtu MP3 un kļūtu par jaunu audio kompresijas standartu. Daudzos veidos tas ir ļoti tuvu MP3, taču ieviests, lai būtu labāka kvalitāte tādā pašā vai pat mazākā faila izmērā. M4A formātu pirmo reizi ieviesa Apple. Formāta tips tiek realizēts arī kā Apple bezzudumu kodētājs (ALE).

Tāpēc pašlaik M4A nevarēja gūt MP3 galvenos panākumus, jo audio formāts vēl nav atskaņojams. Tas kaut kā ir ierobežots tikai ar MacOS, iPod un citiem Apple produktiem.

**Mp3**: slavenākais digitālais audio formāts. Tas bija arī viens no pirmajiem kompresijas formātiem uz skatuves un kļuva ļoti populārs mūzikas cienītāju vidū. Tā galvenie panākumi ir tik ātri, ka faila tipu var atskaņot universāli un ar gandrīz jebko, aparatūru vai programmatūru. Vispārīgā nozīmē M4A radīs labāku skaņas kvalitāti, taču daudzi iebilst, ka neatkarīgi no tā, vai tā ir patiesība vai nē, skaņas atšķirības nav nosakāmas, un tas būtu laika izšķiešana, mēģinot pārvērst MP3 failus M4A failos. Galu galā konvertēšana tikai liks jums zaudēt sākotnējo skaņas kvalitāti.

## M4A faila formāta specifikācija

M4A faili sastāv no secīgiem gabaliem. Katrai daļai ir 8 baitu galvene, un tā ir sadalīta šādi:
- 4 baitu gabala lielums (lielais baits, vispirms augstais baits)
- 4 baitu gabala tips — viens no iepriekš definētiem parakstiem: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide, load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt , ssrc, PICT.

First chunk will be of type "ftype" and has a sub-type at offset 8. M4A, kas definēts pēc apakštipa, kuram ir jābūt M4A_, M4B apakštipam jābūt M4B_ un M4P apakštipam jābūt M4P_.

Atkārtojot gabalus, līdz tiek atklāts nezināma veida gabals, tas veidos M4A (MPEG-4 Audio) failu.

## Atsauces Nr.

* [MPEG-4 14. daļa — Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14. daļas audio (M4A,M4B,M4P) formāta un atkopšanas piemērs](https://www.file-recovery.com/m4a-signature-format.htm)


