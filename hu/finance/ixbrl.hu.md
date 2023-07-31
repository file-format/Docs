{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl", "ixbrl fájl", "ixbrl fájlformátum", "ixbrl fájl típusa", "fájl", "típus", "mi az ixbrl fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL – Üzleti és pénzügyi jelentési fájlformátum",
  "description":"További információ az IXBRL fájlformátumról és az API-król, amelyek IXBRL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Mi az iXBRL fájl?

Az iXBRL (ilnine XBRL) fájlformátum lehetővé teszi az [XBRL](/hu/finance/xbrl/) adatok HTML-fájlba ágyazását, hogy azok gépi és ember által is olvashatóvá váljanak. Ez valójában egy [xHTML](/hu/web/xhtml/) fájl, amely XBRL címkéket használ, és az XBRL International fejlesztette ki, hogy megfeleljen az Egyesült Királyság HMRC követelményeinek. Az iXBRL használatával pénzügyi kimutatások készíthetők úgy, hogy az eredeti dokumentum elrendezése érintetlen marad. Az iXBRL fájlok bármely szövegszerkesztőben megnyithatók, például a Notepad Windows operációs rendszeren és a TextEdit MacOS rendszeren.

## iXBRL fájlformátum

Az iXBRL-en belül az XBRL tartalma xHTML-fájlformátumba van csomagolva, amely XML-címkéket használ. Mint az XBRL,<xbrl> az iXBRL fájlok gyökéreleme. Az XHTML formátum a tartalmát különböző dokumentumtípusok és modulok gyűjteményeként jeleníti meg. Az XHTML összes fájlja XML fájlformátumon alapul, és megfelel az XML dokumentumszabványoknak. Az XHTML a függő [HTML](/hu/web/html/) dokumentumobjektum-modell (DOM) vagy az [XML](/hu/web/xml/) dokumentumobjektum-modell operatív felhasználásának alapvető formátuma. A külvilág számára az iXBRL az [xHTML](/hu/web/xhtml/) fájlformátum specifikációit követi.

### iXBRL vs XBRL

Az XBRL az iXBRL-hez hasonlítható a következő tényezők alapján:

* Összetettség
* Formázási lehetőségek
* Fájltípusok/kiterjesztések
* Rendering opció
* Bejelentési folyamat

Az alábbi táblázat szemlélteti ezeket a különbségeket.

|Paraméter|XBRL|iXBRL|
---|---|---|
|Bonyolultság|Bonyolultabb, mint az iXBRL|Kevésbé bonyolult az XHTML meglévő szervezeti sémája miatt|
|Formázási lehetőségek|Korlátozott rugalmasság|Nagy rugalmasság a tartalomformázáshoz|
|Fájltípusok/Kiterjesztés|Formálisan mentve .xml kiterjesztéssel|Általában .html vagy .xhtml kiterjesztéssel mentve|
|Megjelenítési beállítások|XBRL-nézők szükségesek ezek megtekintéséhez|Ember által olvasható, böngészőben megtekinthető tartalom|
|Iktatási folyamat| Az XBRL (géppel olvasható) és a HTML (ember által olvasható) példánydokumentumokat külön kell iktatni.|Ember által olvasható és géppel olvasható formátumok is elérhetők egyetlen példány dokumentumban|

## Hivatkozások

* [XBRL – a Wikipedia által](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

