{
  "date" : "2019-10-11",
  "keywords" :[ "mht", "mht fájl", "mht fájlformátum", "mht fájltípus", "fájl", "típus", "mi az mht fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML fájlformátum",
  "description" :"További információ az MHT-fájlformátumról és az MHT-fájlok létrehozásához és megnyitásához szükséges API-król.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Mi az MHT fájl?

Az .mht kiterjesztésű fájl egy MIME-kompatibilis archiválási fájlformátum, amely különböző típusú adatokat tartalmaz egyetlen fájlban. Beágyazott erőforrásként képes tárolni olyan adatokat, mint például szöveg, képek, oldalstílus [CSS](/hu/web/css/) fájlok, JavaScript és egyéb erőforrások formájában. Az üzenet/rfc822 MIME-típusú MHT-fájlok egyetlen archív fájlba foglalják a HTML-fájl teljes tartalmát, amelyet a tárolóeszközökön tárolnak archiválásra. Az olyan szoftveralkalmazások, mint például a Microsoft Word, lehetővé teszik a WORD-dokumentumok MHT-formátumba való konvertálását MHT-fájlként történő exportálással. Az MHT fájlok megnyithatók olyan népszerű böngészőkkel, mint a Microsoft Internet Explore és a Google Chrome.

## MHT fájlformátum

Az [MHTML](/hu/web/mhtml/)-hez hasonlóan az MHT is az összesített HTML-dokumentumok MIME-beágyazása. Az MHT-dokumentumokon belüli dokumentumtartalmak, például soron belüli képek, stíluslapok, kisalkalmazások stb. MIME-kódolásúak, ahol ezek URI-kon keresztül egy gyökérerőforráshoz kapcsolódnak. Az e-mail kliensek, például a Microsoft Outlook, az e-maileket (általában [EML](/hu/email/eml/)) MHT-fájlformátumban tárolják. Az MHT-fájlformátum teljes specifikációi az [RFC 822]-ben (https://tools.ietf.org/html/rfc822) érhetők el, és az MHT-fájlok feldolgozására alkalmas szoftveralkalmazások fejlesztése során használhatók.

## Az MHT és az MHTML közötti különbség

Az online oldal mentése során a felhasználónak meg kell határoznia azt a fájlformátumot, amelyen belül az online oldalt el kell mentenie a natív rendszeren. Leggyakrabban a felhasználó összezavarodik a jelölőnyelv és az MHTML fájlformátumok között. Azt veszik észre, hogy zavaró látni, hogy a fájlformátum egészségesebb ezek között.

Ha a felhasználó úgy dönt, hogy nem pazarolja el az online oldalt jelölőnyelvként, akkor létrejön egy mappa, amely több fájlt tartalmaz az oldal különböző tartalmához, azaz teljesen különböző fájlterület-egységet hoz létre szöveghez, grafikákhoz, kisalkalmazásokhoz stb. Ezzel szemben a mentés. az online oldal, mivel az MHTML egy fájlt hoz létre a teljes online oldalhoz. Az oldal összes eleme grafikákkal, hivatkozásokkal és alternatív fájlokkal együtt egy fájlba ágyazva.

Természetesen egyszerű kezelni az MHT vagy MHTML fájlokat, mivel a fájl védett és megosztható egyszerűen e-mailben. Azonban a jelölőnyelvi fájlok területegysége az információvesztés esélye alatt, mivel akár egy fájl elvesztése vagy törlése is a teljes jelölőnyelvi mappát használhatatlanná teheti a felhasználó számára.

## Hivatkozások

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

