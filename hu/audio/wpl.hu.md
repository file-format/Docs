{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl fájl", "kiterjesztés", "formátum", "mi a wpl fájl", "zene", "wpl fájlformátum"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tudjon meg többet a WPL fájlformátumról és az API-król, amelyek WPL fájlokat hozhatnak létre, konvertálhatnak és megnyithatnak.",
  "title" :"WPL - Windows Media Player lejátszási lista fájl",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Mi az a WPL fájl?

A .wpl kiterjesztésű fájl tartalmazza a Microsoft Windows Media Playeren futtatandó zeneszámok lejátszási listáját. Ezeket a fájlokat általában a felhasználók hozzák létre video- és hanggyűjteményükhöz. A WPL fájlba írt tartalom csak a .wpl fájl létrehozója által kiválasztott multimédiás fájlok könyvtárútvonalai vagy helyei, így a médialejátszó alkalmazás azonnal meg tudja találni és le tudja játszani a multimédiás tartalmat a könyvtárak helyéről.

## WPL fájlformátum

A WPL (Windows Media Player Playlist) egy védett fájlformátum, amelyet a Microsoft Windows Media Player 9-es vagy újabb verziói használnak. Ez egy számítógépes fájlformátum, amely multimédiás lejátszási listákat tárol. Alapértelmezés szerint a lejátszási lista .wpl (Windows Media Player Playlist) kiterjesztéssel kerül mentésre. Ehelyett használhatja a [.m3u](/hu/audio/m3u) kiterjesztést, ha olyan eszközön szeretné lejátszani adatlemezeit, amely nem támogatja ezt a bővítményt. A WPL fájl elemei XML formátumban vannak ábrázolva.

A "smil" legfelső szintű elem azt határozza meg, hogy a fájl elemei a Synchronized Multimedia Integration Language (SMIL) struktúrát követik. A fájl létrehozása és mentése .wpl kiterjesztéssel történik, MIME-típusa pedig application/vnd.ms-wpl.

### WPL példa

Íme egy példa egy wpl fájlra:
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




## Hivatkozások ##

* [MPEG-1 Audio Layer II – Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

