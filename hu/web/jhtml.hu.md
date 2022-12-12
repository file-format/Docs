{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml", "jhtml fájl", "jhtml fájlformátum", "jhtml fájltípus", "fájl", "típus", "mi az a jhtml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Java HTML fájl",
  "description":"További információ a JHTML fájlformátumról és az API-król, amelyek JHTML fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Mi az a JHTML fájl?

A .jhtml kiterjesztésű fájl egy [HTML](/hu/web/html/) fájl [Java](/hu/programming/java/) kóddal, amely akkor fut le a szerveren, amikor egy kliens kéri ezt az oldalt a böngészőben. A szerver feldolgozza a kéréseket, végrehajtja a függvényben foglalt Java függvényeket, és visszaküldi az oldalt a kliens böngészőjének. A JHTML oldalakba beágyazott Java objektumok a szerveren futnak az ilyen típusú oldalakra vonatkozó kérések kezelésére. A JHTML-fájlok a JDBC (Java [Database](/hu/database/) Connectivity) kapcsolat segítségével is hozzáférhetnek az adatbázisból származó információkhoz. A JHTML-fájlok bármely szövegszerkesztőben megnyithatók, és olyan webböngészőkkel is megtekinthetők, mint a Google Chrome, a Firefox és a Safari.

## JHTML fájlformátum

A JHTML az ATG szabadalmaztatott technológiája, és az ATG (Art Technology Group) Dynamo Document Editor segítségével hozható létre. A JHTML fájlok egyszerű szöveges fájlformátumban íródnak a szabványos HTML és Java kód használatával. Ezek szabványos HTML-címkéket tartalmaznak a Java objektumokra hivatkozó, védett címkéken kívül. Amikor a felhasználó ilyen oldalt kér, a HTTP-kiszolgáló továbbítja a kérést egy Java-alkalmazásszervernek. A JHTML oldalt először .java fájllá alakítják, és lefordítják egy [.class](/hu/programing/class/) fájl létrehozására, amely servletként fut le. Ez szabványos HTTP- és HTML-adatfolyamot hoz létre, amelyet visszaküld a kérelmező böngészőnek a felhasználó számára történő megjelenítés céljából. Ez hasznos, ha adatbázissal kapcsolatos lekérdezéseket futtat a szerveren, és visszaküldi a véglegesített összesített eredményt a kliens böngészőjének.

## Hivatkozások

* [A HTML-dokumentum globális szerkezete](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

