{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"wpl fil",
"udvidelse",
"format",
"hvad er en wpl-fil",
"musik",
"wpl filformat"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om WPL-filformat og API'er, der kan oprette, konvertere og åbne WPL-filer.",
  "title": "WPL - Windows Media Player Playlist File",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-dal"
}
},
  "lastmod": "2021-06-11"
}

## Hvad er WPL fil?

En fil med filtypenavnet .wpl indeholder afspilningslisten over sange, der skal køres på Microsoft Windows Media Player. Disse filer er normalt oprettet af brugere til deres video- og lydsamlinger. Indholdet skrevet i en WPL-fil er kun mappestier eller placeringer for multimediefilerne, som er valgt af skaberen af .wpl-filen, så medieafspillerapplikationen kan straks finde og afspille multimedieindholdet fra deres mappeplaceringer.

## WPL filformat

WPL (Windows Media Player Playlist) er et proprietært filformat, der bruges i Microsoft Windows Media Player version 9 eller nyere. Det er et computerfilformat, der gemmer multimedieafspilningslister. Som standard gemmes afspilningslisten med udvidelsen .wpl (Windows Media Player Playlist). Du kan bruge udvidelsen [.m3u](/audio/m3u/) i stedet, hvis du vil afspille dine datadiske på en enhed, der ikke understøtter denne udvidelse. Elementerne i en WPL-fil er repræsenteret i XML-format.

Topniveauelementet smil angiver, at filens elementer følger SMIL-strukturen (Synchronized Multimedia Integration Language). Filen oprettes og gemmes med filtypen .wpl, og dens MIME-type er application/vnd.ms-wpl.

### WPL eksempel

Her er et eksempel på en wpl-fil:
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




## Referencer ##

* [MPEG-1 Audio Layer II - Af Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


