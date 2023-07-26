{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl-bestand", "extensie", "format", "wat is een wpl-bestand", "muziek", "wpl-bestandsformaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over WPL-bestandsindeling en API's die WPL-bestanden kunnen maken, converteren en openen.",
  "title" :"WPL - Windows Media Player-afspeellijstbestand",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Wat is een WPL-bestand?

Een bestand met de extensie .wpl bevat de afspeellijst met nummers die op Microsoft Windows Media Player moeten worden uitgevoerd. Deze bestanden worden meestal door gebruikers gemaakt voor hun video- en audiocollecties. De inhoud die in een WPL-bestand is geschreven, is slechts mappaden of locaties voor de multimediabestanden die zijn geselecteerd door de maker van het .wpl-bestand, zodat de mediaspelertoepassing de multimedia-inhoud direct kan vinden en afspelen vanaf hun maplocaties.

## WPL-bestandsindeling

WPL (Windows Media Player Playlist) is een eigen bestandsindeling die wordt gebruikt in Microsoft Windows Media Player versie 9 of hoger. Het is een computerbestandsformaat waarin multimedia-afspeellijsten worden opgeslagen. Standaard wordt de afspeellijst opgeslagen met de extensie .wpl (Windows Media Player Playlist). U kunt in plaats daarvan de extensie [.m3u](/nl/audio/m3u/) gebruiken als u uw gegevensschijven wilt afspelen op een apparaat dat deze extensie niet ondersteunt. De elementen van een WPL-bestand worden weergegeven in XML-formaat.

Het element op het hoogste niveau "smil" geeft aan dat de elementen van het bestand de structuur van de Synchronized Multimedia Integration Language (SMIL) volgen. Het bestand wordt gemaakt en opgeslagen met de extensie .wpl en het MIME-type is application/vnd.ms-wpl.

### WPL-voorbeeld

Hier is een voorbeeld van een wpl-bestand:
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




## Referenties ##

* [MPEG-1 Audio Layer II - Door Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

