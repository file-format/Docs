{
  "date": "2021-06-09",
  "keywords": [
"m4b",
"mp3",
"failu",
"pagarinājumu",
"formātā",
"kas ir m4b faila formāts",
"mūzika",
"m4b faila formātā",
"M4b pret MP3",
"m4b faila formāta specifikācija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par M4B failu formātu un API, kas var izveidot, konvertēt un atvērt M4B failus.",
  "title": "M4B — MPEG-4 audiogrāmatas faila formāts",
  "linktitle": "M4B",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-lvb"
}
},
  "lastmod": "2021-06-09"
}

## Kas ir M4B fails?

Fails ar paplašinājumu .m4b ir audiogrāmata, ko parasti izmanto Apple Books un iTunes. Šajā formātā izmantotais audio tiek saglabāts MPEG-4 formātā un saspiests, izmantojot AAC kodējumu. M4B fails ir ļoti līdzīgs M4A failam, taču tas atbalsta ar audiogrāmatu saistītās funkcijas, piemēram, grāmatzīmes un nodaļu pārtraukumus. M4B faili ir pieejami gan DRM iespējotā, gan bezmaksas DRM versijā. DRM šifrētas audiogrāmatas parasti ir maksas audiogrāmatas no iTunes Store. Tā kā bez DRM var viegli atrast internetā.

## M4B faila formāts

Audiogrāmatas failus, kas satur metadatus, attēlus, grāmatzīmes un hipersaites, var saglabāt ar paplašinājumu .m4a, bet parasti saglabāšanas laikā tiek izmantots paplašinājums .m4b, lai norādītu, ka failam ir audiogrāmatas faila formāts. Fairplay DRM (digitālo tiesību pārvaldība) tiek izmantota, lai aizsargātu savus M4B failus. Tādējādi no iTunes lejupielādētos failus var atskaņot tikai autorizētās ierīcēs vai datoros.


## M4B pret M4A

Gan M4B, gan [MP3](/audio/mp3/) ir tikai audio failu formāti.

**M4B**: kvalitātes ziņā uzvar, salīdzinot ar MP3, ja abi tiek kodēti ar vienādu bitu pārraides ātrumu. M4B ir audiogrāmatas fails, kas tiek saspiests, izmantojot AAC kodējumu. Tas būtībā ir saistīts ar MPEG-4 audio slāni”, faili ar paplašinājumu .m4b ir MPEG-4 filmu audio slānis, bet ar papildu audiogrāmatu funkcijām. Tās mērķis ir apsteigt MP3 un kļūt par jaunu audio kompresijas standartu. Daudzos veidos tas ir ļoti tuvs MP3, taču izstrādāts, lai tā kvalitāte būtu labāka tādā pašā vai pat mazākā faila izmērā. M4B formātu pirmo reizi ieviesa Apple. Formāta tips tiek realizēts arī kā Apple bezzudumu kodētājs (ALE).

Tāpēc pašlaik M4B nevarēja gūt MP3 galvenos panākumus, jo audio formāts vēl nav parasti atskaņojams.

**Mp3**: digitālais audio formāts, kas ir labi pazīstams visiem. Pati pirmais kompresijas formāts uz skatuves un kļuva ļoti slavens mūzikas klausītāju vidū. Tā galvenie panākumi ir tik strauji, ka faila tipu var atskaņot universāli un saderīgi ar gandrīz jebko, aparatūru vai programmatūru. Vispārīgā nozīmē M4A radīs labāku skaņas kvalitāti, taču daudzi iebilst, ka neatkarīgi no tā, vai tā ir patiesība vai nē, skaņas atšķirības nav salīdzināmas, un tā būtu laika izšķiešana, mēģinot pārvērst MP3 failus M4A failos. Visbeidzot, konvertēšana tikai liks jums zaudēt sākotnējo skaņas kvalitāti.

## M4B faila formāta specifikācija

Līdzīgi kā [M4A](/audio/m4a/), arī M4B faili sastāv no secīgiem gabaliem. Katrai daļai ir 8 baitu galvene, un tā ir sadalīta šādi:
- 4 baitu gabala lielums (lielais baits, vispirms augstais baits)
- 4 baitu gabala tips — viens no iepriekš definētiem parakstiem: ftyp, mdat, moov, pnot, moof, udta, uuid, free, ctab, skip, jP2, wide, load, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT , scpt, ssrc.

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. M4B, kas definēts pēc apakštipa, kam jābūt M4B_.

Atkārtojot gabalus, līdz tiek atklāts nezināma veida gabals, tiks izveidots M4B (MPEG-4 audio) fails.

## Atsauces

* [MPEG-4 14. daļa — Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14. daļas audio (M4A,M4B,M4P) formāta un atkopšanas piemērs](https://www.file-recovery.com/m4a-signature-format.htm)


