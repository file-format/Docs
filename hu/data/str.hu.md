{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR File - dBASE Structure List Object File - Mi az .str fájl és hogyan nyitható meg?",
  "description" : "További információ az STR dBASE szerkezetlista objektumfájlról és a megnyitásáról.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-hu",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mi az STR fájl?

Az STR fájlformátumot általában a dBASE adatbázis-kezelő rendszerhez társítják. A dBASE rendszerben az .str fájl általában egy struktúralista objektumfájlt jelent. Ez a fájl egy adatbázistábla szerkezetét tartalmazza, beleértve a mezőkre (oszlopokra) és tulajdonságaikra vonatkozó információkat.

A struktúralista objektumfájlja (.str) olyan metaadatokat tartalmaz, mint a mezőnevek, adattípusok, mezőhosszak és az adatbázistábla egyes mezőihez társított egyéb tulajdonságok. Az adatbázistábla szerkezetének meghatározására szolgál anélkül, hogy tényleges adatrekordokat tartalmazna.

Az olyan programok, mint a dBASE vagy más adatbázis-kezelő eszközök használhatják ezt a fájlt az adatbázistábla elrendezésének megértéséhez, és olyan műveleteket hajthatnak végre, mint a lekérdezés, frissítés vagy új rekordok létrehozása ezen a struktúra alapján.

Íme egy alapvető példa arra, hogy mit tartalmazhat egy STR fájl:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Ez a példa egy négy mezőt tartalmazó táblázatot ír le: ID, Name, Age és DOB, valamint ezek megfelelő adattípusait és hosszát.

## STR fájl - Mivel nyitható meg egy STR fájl?

Az .str fájlok megnyitásának elsődleges módja magának a dBASE-nak a használata, különösen Windows operációs rendszereken. A dBASE képes elolvasni és értelmezni ezeknek a fájloknak a tartalmát, lehetővé téve a felhasználók számára, hogy megtekintsék és dolgozhassanak az adatbázis-struktúrával.

Mivel az .str fájlok alapvetően egyszerű szöveges fájlok, amelyek információkat tartalmaznak az adatbázis szerkezetéről, ezeket szövegszerkesztővel is megnyithatja. Szövegszerkesztők például a Microsoft Notepad Windows rendszeren és az Apple TextEdit Mac rendszeren. Szövegszerkesztőben megnyitva megtekintheti a fájl tartalmát, beleértve a mezőneveket, adattípusokat és egyéb szerkezeti információkat, ember által olvasható formátumban.

## Hivatkozások
* [dBase](https://en.wikipedia.org/wiki/DBase)


