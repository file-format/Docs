{
  "date": "2021-08-09",
  "keywords": [
"mmf",
"failu",
"pagarinājumu",
"formātā",
"audio",
"smaf",
"mmf paplašinājums",
"mmf faili",
"mobilais mūzikas fails",
"yamaha"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MMF failu formātu un API, kas var izveidot un atvērt MMF failus.",
  "title": "MMF — mobilās mūzikas faila formāts",
  "linktitle": "MMF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mm-lvf"
}
},
  "lastmod": "2021-08-09"
}

## Kas ir MMF fails?

MMF ir faila paplašinājums, kas saistīts ar SMAF failu. MMF apzīmē mobilo mūzikas failu, savukārt SMAF apzīmē sintētiskās mūzikas mobilās lietojumprogrammas formātu. Viedtālruņa MMF faili satur sistēmas zvana signālus, skaņu un var ietvert arī grafiku un teksta displeju. Turklāt NTF satur trīs veidu instrumentu parametrus, tostarp FM, PCM un straumēšanas PCM. Šie failu formāti ir saderīgi ar Windows sistēmas platformu. NTF faili tiek klasificēti kā datu faili. Parasti Microsoft Mail atbalsta MMF failus. Failu ar MMF sufiksu var kopēt uz jebkuru mobilo ierīci vai sistēmas platformu.

Turklāt šie faili ir daudz mazāki, salīdzinot ar standarta MIDI formāta failiem. [WAV](/audio/wav/) un [MID](/audio/mid/) failus var konvertēt MMF formātā, ko pēc tam var kopīgot un izplatīt kā audio saturu. Šos failus var saņemt pa e-pastu tieši uz tālruņiem un personālo datoru.


## Īsa NTF faila formāta vēsture

Yamaha izstrādāja SMAF rīkus kā skaņas failus, lai viedtālruņi varētu saglabāt lielāku skaitu unikālu zvana signālu. Yamaha iepazīstināja ar SMAF, ražojot MA-1, MA-2, MA-3, MA-5 un MA-7 LSI skaņas mikroshēmas. Visi šie formāti kļuva diezgan pazīstami starp mobilajiem tālruņiem Austrumāzijas tirgū 2000. gada sākumā.

Starptautiskā līmenī NTF formātu atļāva Samsung. Ar MMF formāta palīdzību Samsung varēja izveidot plašu polifonisko zvana signālu klāstu, ko izmantot Samsung viedtālruņos.

Yamaha vēlējās padarīt formātu vēl populārāku, tāpēc oficiālajos Yamaha SMAF failos tā publicēja vairāk rīku, kas ir saderīgi ar šo formātu. Izmantojot šo iespēju, lietotāji tagad var viegli atskaņot MMF failus savos datoros.


## MMF faila formāta specifikācijas ##

NTF faili ir iedalīti datu sadaļās. Katra segmenta aprakstīšanai tiek izmantota prefiksēta struktūra ap 8 baitiem.
4 baitu etiķete ietver CNTI, OPDA, MSTR, MTR un ATR. Datu lielums plus 8 baiti ir gabala lielums; viss faila lielums tiek aprēķināts, summējot visus gabalu izmērus. Ja fails nav bojāts, summētajam faila lielumam ir jābūt tādam pašam kā primārā galvenes izmēram.

### Virsraksts ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Šeit ir MMF faila piemērs:

![](../mmf.png)

## Atsauces

* [MMF — Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)


