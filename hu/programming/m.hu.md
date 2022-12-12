{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab forráskód fájl",
  "description":"További információ a Matlab .m forráskód fájlról és az API-król, amelyek MF fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab forráskód fájlok

## Mi az M (Matlab) fájl?

Az .m kiterjesztésű fájl egy forráskódfájl, amelyet a Matlab, egy programozási és numerikus számítási platform használ elemzésre, algoritmusok fejlesztésére és szimulációs modellezésre. Más programozási fájlformátumokhoz hasonlóan az M fájl is tartalmaz olyan forráskódot, amely Matlab parancsokat hajt végre grafikonok ábrázolásához, szimulációk futtatásához és egyéb matematikai műveletekhez. Egyetlen Matlab szimuláció több ilyen .m fájlra is kiterjedhet, amelyek szkriptek, osztályok, függvények vagy deklarációk szerint osztályozhatják az alkalmazást. A Matlab M fájlok bármely szövegszerkesztővel megnyithatók.

## Matlab M fájlformátum - További információ

A Matlab .m fájlok olyan szöveges fájlok, amelyek Matlab programozási nyelvű programozási kódot tartalmaznak. Ezek bármely szövegszerkesztőben megnyithatók és szerkeszthetők, majd visszamenthetők a Matlab szoftverbe történő végrehajtáshoz. Maga a Matlab tartalmaz egy Live Editor-t, amelyet kód, kimenet és formázott szöveg kombinációjából álló szkriptek létrehozására használnak.

### Matlab függvényfájlok

Más programozási nyelvekhez hasonlóan létrehozhat olyan .m fájlt, amely csak egy adott feladatot végrehajtó függvény definícióját tartalmazza. Az ilyen fájlok szintén .m kiterjesztéssel kerülnek mentésre, és csak az ehhez a funkcióhoz kapcsolódó funkciókat valósítják meg.

### .M fájl példa

Az alábbiakban egy Matlab függvényfájl példája látható, amely kiszámítja a h magasságból leejtett objektum idejét.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Ennek a függvénynek a Matlab szerkesztőből vagy egy másik .m fájlból történő meghívásához a következő kód használható.
```C++
TimeToGround(100)
```

## Hivatkozások

* [Matlab – Támogatott fájlformátumok](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [A Matlab használata](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C megvalósítási fájl

## Mi az az M (Objective-C) fájl?

Az M fájlt implementációs fájlnak is nevezik, amely egy Objective-C nyelven írt osztály forráskódját tartalmazza, amely programozási nyelv az OS X és iOS rendszerekhez készült szoftveralkalmazások írásához. Az Objective-C a fő programozási nyelv, amelyet az Apple fő API-i, a Cocoa és a Cocoa Touch használnak ezekhez a platformokhoz. Egy ezen a nyelven kifejlesztett szoftveralkalmazás több .m fájlt is tartalmazhat, amelyek a programosztályok megvalósítását tartalmazzák. Ezeket Apple XCode, jEdit és más általános szövegszerkesztők segítségével lehet megnyitni.

## Objective-C M fájlformátum - További információ

Az M fájlok egyszerű szöveges formátumban vannak megírva az Objective-C programozási szintaxisával. Egy osztály minden metódusát meg kell határozni az összes szükséges kóddal ezekben a megvalósítási fájlokban. Ezek a megvalósítási M-fájlok a követelményeknek megfelelően egy vagy több .h fejlécfájlt importálhatnak. Az import utasítás megmondja a fordítónak, hogy hol találja meg a megvalósítási fájlhoz tartozó fejlécfájlt. Az import nyilatkozat a következőképpen van megírva.

```C++
#import "network.h"
```

Ezután minden M-fájl megvalósítása a "@implementation" direktívával kezdődik, amelyet a megvalósítási osztály fájlneve követ. Ezt követi a fejlécfájlban deklarált metódusok megvalósítása.

### M fájlformátum példa

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Hivatkozások
* [A C célkitűzésről](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C útmutató](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

