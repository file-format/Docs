{
  "date": "2021-08-04",
  "keywords": [
"mod",
"mp3",
"failu",
"pagarinājumu",
"formātā",
"kas ir mod faila formāts",
"mūzika",
"mod faila formātā",
"mod vs MP3",
"mod faila formāta specifikācija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MOD failu formātu un API, kas var izveidot, konvertēt un atvērt MOD failus.",
  "title": "MOD — mūzikas moduļa fails",
  "linktitle": "MOD",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mo-lvd"
}
},
  "lastmod": "2021-08-04"
}

## Kas ir MOD fails?
Fails ar paplašinājumu .mod ir mūzikas moduļa fails, kas izveidots, izmantojot standarta mūzikas moduļa formātu, kura pamatā ir **Amiga moduļa formāts**, ko izstrādājis Karstens Obarskis un izlaists ar Commodore programmatūru **Ultimate Soundtracker**. Amiga sistēma. Līdzīgi kā [MIDI](/audio/mid/) fails, tas sastāv no nošu rakstiem un skaņu paraugiem, kas atspoguļo dažādus instrumentus, kas tiek atskaņoti atbilstoši notīm. MOD faili tiek īpaši izmantoti videospēlēs kā fona mūzika un **demoscene** datormākslas subkultūrā.

## MOD faila formāts

MOD ir datora faila formāts, kura pamatfunkcija ir mūzikas attēlošana, un tas bija pirmais moduļa faila formāts. MOD failiem tiek izmantots faila paplašinājums .mod, izņemot **Amiga**, kas nolasa faila galveni, lai noteiktu faila tipu, tāpēc tas nav atkarīgs no faila nosaukuma paplašinājumiem. MOD fails sastāv no dažādu instrumentu kopas paraugu veidā, vairākiem modeļiem, kas norāda, kā un kad paraugi ir jāatskaņo, un sarakstu ar paraugiem, kurus atskaņot kādā secībā.

### MOD faila formāta specifikācijas

MOD faila modelis faktiski ir izveidots sekvencera lietotāja saskarnē kā tabula ar vienu kolonnu katrā kanālā, tāpēc šai tabulai ir četras kolonnas (viena katram Amiga aparatūras kanālam. Katrā kolonnā ir 64 rindas).

Tabulas šūna var izraisīt kādu no tālāk norādītajām darbībām tās kolonnas kanālā, kad ir sasniegts tās rindas laiks:

- Sāciet instrumentu atskaņot jaunu noti šajā kanālā noteiktā skaļumā, iespējams, izmantojot īpašu efektu.
- Mainiet skaļumu vai īpašo efektu, kas tiek piemērots pašreizējai notij
- Mainīt modeļa plūsmu; pāriet uz noteiktu dziesmas vai raksta pozīciju vai cilpu rakstā
- Neko nedarīt; visas esošās notis, kas tiek atskaņotas šajā kanālā, tiks atskaņotas

Instruments ir viens paraugs kopā ar neobligātu specifikāciju, kuru parauga daļu var atkārtot, lai saglabātu viengabalainu noti.

### Laiks
Sākotnējā MOD failā minimālais laika posms bija 0,02 sekundes jeb vertikālās dzēšanas (VSync) intervāls, jo sākotnējā programmatūra izmantoja monitora VSync laiku, kas darbojās ar 50 Hz (PAL) vai 60 Hz (NTSC) laika noteikšanai.

## Atsauces

* [MOD (faila formāts) — Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))


