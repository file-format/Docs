{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"wpl failą",
"pratęsimas",
"formatu",
"kas yra wpl failas",
"muzika",
"wpl failo formatas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie WPL failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti WPL failus.",
  "title": "WPL – „Windows Media Player“ grojaraščio failas",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-ltl"
}
},
  "lastmod": "2021-06-11"
}

## Kas yra WPL failas?

Faile su plėtiniu .wpl yra dainų, kurios bus paleistos Microsoft Windows Media Player, grojaraštis. Šiuos failus paprastai kuria vartotojai savo vaizdo ir garso kolekcijoms. Turinys, parašytas WPL faile, yra tik .wpl failo kūrėjo pasirinktų daugialypės terpės failų katalogų keliai arba vietos, todėl medijos leistuvo programa gali greitai rasti ir paleisti daugialypės terpės turinį iš savo katalogo vietų.

## WPL failo formatas

WPL (Windows Media Player grojaraštis) yra patentuotas failo formatas, naudojamas Microsoft Windows Media Player 9 ar naujesnėse versijose. Tai kompiuterio failo formatas, kuriame saugomi daugialypės terpės grojaraščiai. Pagal numatytuosius nustatymus grojaraštis išsaugomas naudojant .wpl (Windows Media Player grojaraščio) plėtinį. Vietoj to galite naudoti plėtinį [.m3u](/audio/m3u/), jei norite leisti duomenų diskus įrenginyje, kuris nepalaiko šio plėtinio. WPL failo elementai pateikiami XML formatu.

Aukščiausio lygio elementas smil nurodo, kad failo elementai atitinka sinchronizuotos daugialypės terpės integravimo kalbos (SMIL) struktūrą. Failas sukuriamas ir išsaugomas su plėtiniu .wpl, o jo MIME tipas yra application/vnd.ms-wpl.

### WPL pavyzdys

Štai wpl failo pavyzdys:
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




## Nuorodos Nr.

* [MPEG-1 Audio Layer II – Vikipedija](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


