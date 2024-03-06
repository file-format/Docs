{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"wpl failu",
"pagarinājumu",
"formātā",
"kas ir wpl fails",
"mūzika",
"wpl faila formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par WPL failu formātu un API, kas var izveidot, konvertēt un atvērt WPL failus.",
  "title": "WPL — Windows Media Player atskaņošanas saraksta fails",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-lvl"
}
},
  "lastmod": "2021-06-11"
}

## Kas ir WPL fails?

Fails ar paplašinājumu .wpl satur dziesmu atskaņošanas sarakstu, kas jāpalaiž programmā Microsoft Windows Media Player. Šos failus parasti izveido lietotāji savām video un audio kolekcijām. WPL failā rakstītais saturs ir tikai direktoriju ceļi vai atrašanās vietas multivides failiem, ko atlasījis .wpl faila veidotājs, lai multivides atskaņotāja lietojumprogramma varētu ātri atrast un atskaņot multivides saturu no to direktoriju atrašanās vietām.

## WPL faila formāts

WPL (Windows Media Player atskaņošanas saraksts) ir patentēts faila formāts, ko izmanto Microsoft Windows Media Player 9 vai jaunākās versijās. Tas ir datora faila formāts, kurā tiek saglabāti multivides atskaņošanas saraksti. Pēc noklusējuma atskaņošanas saraksts tiek saglabāts ar paplašinājumu .wpl (Windows Media Player atskaņošanas saraksts). Tā vietā varat izmantot paplašinājumu [.m3u](/audio/m3u/), ja vēlaties atskaņot savus datu diskus ierīcē, kas neatbalsta šo paplašinājumu. WPL faila elementi tiek attēloti XML formātā.

Augstākā līmeņa elements smil norāda, ka faila elementi atbilst sinhronizētās multivides integrācijas valodas (SMIL) struktūrai. Fails tiek izveidots un saglabāts ar paplašinājumu .wpl, un tā MIME tips ir application/vnd.ms-wpl.

### WPL piemērs

Šeit ir wpl faila piemērs:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Atsauces Nr.

* [MPEG-1 Audio Layer II — Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


