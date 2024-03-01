{
  "date": "2021-06-11",
  "keywords": [
"wpl",
"wpl tiedosto",
"laajennus",
"muoto",
"mikä on wpl-tiedosto",
"musiikkia",
"wpl tiedostomuoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WPL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata WPL-tiedostoja.",
  "title": "WPL - Windows Media Playerin soittolistatiedosto",
  "linktitle": "WPL",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wp-fil"
}
},
  "lastmod": "2021-06-11"
}

## Mikä on WPL-tiedosto?

Tiedosto, jonka laajennus on .wpl, sisältää soittolistan kappaleista, jotka ajetaan Microsoft Windows Media Playerissa. Käyttäjät luovat yleensä nämä tiedostot video- ja äänikokoelmiaan varten. WPL-tiedostoon kirjoitettu sisältö on vain hakemistopolkuja tai paikkoja multimediatiedostoille, jotka .wpl-tiedoston luoja on valinnut, joten mediasoitinsovellus voi nopeasti löytää ja toistaa multimediasisällön niiden hakemistopaikoista.

## WPL tiedostomuoto

WPL (Windows Media Player Playlist) on patentoitu tiedostomuoto, jota käytetään Microsoft Windows Media Playerin versioissa 9 tai uudemmissa. Se on tietokonetiedostomuoto, joka tallentaa multimediasoittolistoja. Oletuksena soittolista tallennetaan .wpl (Windows Media Player Playlist) -laajennuksella. Voit käyttää sen sijaan laajennusta [.m3u](/audio/m3u/), jos haluat toistaa datalevyjäsi laitteella, joka ei tue tätä laajennusta. WPL-tiedoston elementit esitetään XML-muodossa.

Ylätason elementti smil määrittää, että tiedoston elementit noudattavat Synchronized Multimedia Integration Language (SMIL) -rakennetta. Tiedosto luodaan ja tallennetaan .wpl-tunnisteella ja sen MIME-tyyppi on application/vnd.ms-wpl.

### WPL esimerkki

Tässä on esimerkki wpl-tiedostosta:
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




## Viitteet ##

* [MPEG-1 Audio Layer II - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


