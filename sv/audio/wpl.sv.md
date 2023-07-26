{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl-fil", "tillägg", "format", "vad är en wpl-fil", "musik", "wpl-filformat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Lär dig om WPL-filformat och API:er som kan skapa, konvertera och öppna WPL-filer.",
  "title" :"WPL - Windows Media Player Playlist File",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Vad är WPL fil?

En fil med filtillägget .wpl innehåller spellistan med låtar som ska köras på Microsoft Windows Media Player. Dessa filer skapas vanligtvis av användare för deras video- och ljudsamlingar. Innehållet som är skrivet i en WPL-fil är bara katalogsökvägar eller platser för multimediafilerna som har valts av skaparen av .wpl-filen, så att mediaspelarapplikationen snabbt kan hitta och spela upp multimediainnehållet från deras katalogplatser.

## WPL filformat

WPL (Windows Media Player Playlist) är ett proprietärt filformat som används i Microsoft Windows Media Player version 9 eller senare. Det är ett datorfilformat som lagrar multimediaspellistor. Som standard sparas spellistan med tillägget .wpl (Windows Media Player Spellista). Du kan använda tillägget [.m3u](/sv/audio/m3u/) istället, om du vill spela dina dataskivor på en enhet som inte stöder detta tillägg. Elementen i en WPL-fil representeras i XML-format.

Toppnivåelementet "smil" anger att filens element följer SMIL-strukturen (Synchronized Multimedia Integration Language). Filen skapas och sparas med filtillägget .wpl och dess MIME-typ är application/vnd.ms-wpl.

### WPL exempel

Här är ett exempel på en wpl-fil:
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




## Referenser ##

* [MPEG-1 Audio Layer II - Av Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

