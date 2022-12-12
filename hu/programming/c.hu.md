{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "mi az ac fájl", "c fájl megnyitása", "kiterjesztés", "fájl", "c fájl", "c fájl formátum", "c fájl kiterjesztése"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C nyelvű programozási fájl",
  "description":"További információ a C fájlformátumról és az API-król, amelyek C-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Mi az a C fájl?

A c fájlkiterjesztéssel mentett fájl egy C programozási nyelven írt forráskódfájl. A **C fájl** tartalmazza az alkalmazás összes funkciójának megvalósítását forráskód formájában. A forráskód deklarációja a [.h](/hu/programming/h/) kiterjesztéssel mentett fejlécfájlokba van beírva. A C++ a C nyelv modern formája, és manapság a legtöbb szoftver fejlesztésére használják.

## Rövid története

A C nyelv a UNIX operációs rendszerhez való különböző segédprogramok létrehozásának eredményeként jött létre. Denis Ritchie, a programozási nyelv megalkotása mögött álló ember, a munka eredetileg az 1960-as években és az 1970-es évek elején kezdődött.

## C Fájlformátum

A C fájlok egyszerű szöveges fájlformátumban vannak írva, a programozási nyelv szintaxisát követve. Egy tipikus C fájl a következőket tartalmazza:

* Import utasítás a fájl tetején a fejlécfájlok importálásához
* egy vagy több módszer a kívánt funkciók megvalósításához

### Fejlécek importálása

A .h kiterjesztésű fejlécfájlok tartalmazzák a szükséges include utasításokat az egyéb funkcionalitásfájlok projektbe való felvételéhez. Ezenkívül ezek tartalmazzák a megvalósítási fájlban meghatározott metódusok deklarációit. A fejlécfájlok az include utasítással szerepelnek az alábbiak szerint.

```
#include <filename.h>
```

### Forráskód megvalósítása

A funkcionális követelmények tényleges megvalósítása metódusként van kódolva a C fájlban. A C fájlban minden metódus rendelkezik visszatérési típussal, metódusnévvel, és tartalmazhat néhány bemeneti paramétert. Ha a visszatérési típus nem érvénytelen, akkor a metódus valamilyen értéket ad vissza.

### C Kódpélda
Itt van egy ac példaprogram:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Referenciák** ##

* [Osztálymegvalósítás – a Wikipédia által](https://en.wikipedia.org/wiki/Class_implementation_file)

