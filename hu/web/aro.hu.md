{
  "date" : "2021-12-09",
  "keywords" :[ "aro", "aro fájl", "aro fájlformátum", "fájltípus", "fájl", "típus", "mi az .aro fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO fájlformátum - SteelArrow webes alkalmazásfájl",
  "description" :"További információ az ARO-fájlokról és az API-król, amelyek ARO-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Mi az ARO fájl?

Az ARO-fájl egy szerveroldali weblapfájl, amelyet a SteelArrow webalkalmazással generálnak. Tartalmaz [HTML](/hu/web/html/) és SteelArrow címkéket és szkripteket. Ezek végrehajtása a szerveren teljes válaszoldalt generál, mielőtt elküldi őket a felhasználó böngészőjének. Az ARO fájlok a HTML tartalom csaknem 95%-át tartalmazzák, míg a többi SteelArrow kódot tartalmaz. Ahhoz, hogy az ARO-fájlok működjenek, a SteelArrow Web Applications kiszolgálót telepíteni kell és futni kell a webkiszolgáló gépen.

## ARO fájlformátum

Az ARO fájlok HTML jelölőnyelvi fájlban vannak írva, beágyazott JavaScript kóddal és Java kisalkalmazásokkal. A [SteelArrow címkék](http://www.steelarrow.com/docs/basics1.aro) a weboldalak fejlesztésének alapvető építőkövei. Ezek ugyan nem változtatják meg az oldal megjelenítését, de az oldal adatokkal való feltöltésére szolgálnak. Ezenkívül a kimenet feltételes utasításokkal történő vezérlésére is használhatók.

### ARO címke példa

Az<SAOUTPUT> Az ARO címke lehetővé teszi a fejlesztők számára, hogy a szkripten belül bárhol adatértékeket adjanak ki. Használható például a PARAM tábla kimenetének lekérésére<SAOUTPUT VALUE=PARAM[]> amelyek a HTML-ben jeleníthetők meg<BODY> címke.

## Hivatkozások

* [SteelArrow címkék](http://www.steelarrow.com/docs/basics.aro)

