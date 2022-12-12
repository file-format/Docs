{
  "date" : "2021-03-10",
  "keywords" :[ "VP8", "File", "Extension", "File Format", "Video Format", "TrueMotion Video", "WebRTC", "WebM"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP8 - TrueMotion Video File",
  "description":"További információ a VP8 fájlformátumról és az API-król, amelyek VP8 fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VP8",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Mi az a VP8 fájl?

A Google bejelentette, hogy a VP8 az egyik legjobb videóformátum, amely a legjobb képminőségű adatátviteli sebességgel és kódolási sebességgel rendelkezik. A VP8 legjobb előnye, hogy jogdíjmentesen helyettesíti a H.264-et. Ez egy speciális formátum a kiváló minőségű videók fájlként vagy bitfolyamként történő kódolására és dekódolására. Ingyenes, mert a Google jogdíjmentes nyilvános licenc alatt kiadta az összes VP8 szabadalmat. Az összes WebRTC videomunka majdnem 90%-a vagy több VP8-at használ.

## VP8 fájlformátum

A VP8-at az On2 Technologies fejlesztette ki 2008-ban, majd 2010-ben a Google tulajdonába került. A VP8 videokodek fő előnye, hogy ingyenes licenc alapján jogdíjmentes. Úgy tervezték, hogy kiváló minőségű videókat biztosítson az interneten és a mobileszközökön. A VP8 első audio-video tárolója a WebM volt, és ezt a kodeket választották 2011-ben WebRTC videokodekként. Ezt a formátumot számos ipari alkalmazás elismeri, mint például a HTML5, a webes valós idejű kommunikáció és a videolejátszás különböző böngészőkben. Teljes piaci igény mutatkozik ennek a formátumnak a teljes HD felbontású támogatására. Különböző célokra használják, például videokonferenciákhoz, videoközvetítéshez és mobileszközökről történő rögzítéshez.

## Műszaki adatok ##

### A VP8 jellemzői
 



* Ingyenes videokodek
* A legprogresszívebb videofájl formátum
* Fokozott ellenállás a keret elvesztésével szemben
* Nagy sebességű videó dekódolás
* Könnyen kitalálható hardverplatformokon
* Tiszta bevezető móddal rendelkezik, azaz csak egyénileg kódolt képkockákat használ szekvenciális előrejelzés nélkül, így lehetővé teszi a véletlenszerű hozzáférést olyan alkalmazásokban, mint a videószerkesztés
* A libvpx az egyetlen szoftverkönyvtár, amely jártas a VP8 videó folyamok kódolásában
* A VP8-at kifejezetten arra tervezték, hogy főként minőségi tartományban működjön

* A kliens hardverek széles skálája csatlakozik az internethez, az alacsony fogyasztású mobil- és beültetett eszközöktől a legfejlettebb asztali számítógépekig sok processzormaggal.
* 420 színmintavétel, csatornánként 8 bites színmélység, progresszív pásztázás és a képméretek akár a legmagasabb, 16383x16383 pixeles képformátumig egyszerűen kezelhetők a VP8 segítségével
* A tömörítési képességre és a dekóder egyszerűségére irányuló impulzus ezekben a tervezési megoldásokban számos egyedi műszaki jellemzőt eredményezett a VP8-ban a többi elismert videótömörítési formátumhoz képest.
* A VP8 három referenciakockát használ a számos referencia mozgáskompenzációs sémából, amelyek más formátumokban is megtalálhatók
* A VP8 nem korlátozódik a képkockasebességre vagy adatsebességre. 14 bitet használ a szélességhez és a magassághoz is, így a legnagyobb felbontás 16384x16384 pixel

### A VP8 korlátai

A VP8 korlátai a felbontás, az adatsebesség és a képkocka sebesség tekintetében a következők:

* A VP8 14 bites szélességet és magasságot alkalmaz, a maximális felbontás 16384x16384 pixel
* A VP9 16 bitet használ a szélességhez és magassághoz, a maximális felbontás 65536x65536 pixel
* Nincs korlátozás a képkocka- vagy adatsebességgel kapcsolatban
 



 



## Hivatkozások

* [VP8 Wikipedia](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20was%20first%20released%20by,%2C%20replacing%20its%20prececessor%2C%20VP7.&text= %20május%2019%2C%20at%20its,an%20visszavonhatatlan%20free%20patent%20licenc)
* [Springer Link](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)

