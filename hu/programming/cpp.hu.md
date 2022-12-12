{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "file", "extension", "file format", "C++", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ forráskód fájl",
  "description":"További információ a CPP fájlformátumról és az API-król, amelyek CPP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a C++ fájl?

A CPP kiterjesztésű fájlok forráskódfájlok a C++ programozási nyelven írt alkalmazásokhoz. Egy C++ projekt több CPP-fájlt is tartalmazhat alkalmazás forráskódjaként. Egy ilyen projekt különböző fájltípusokból áll, amelyek közül a CPP-fájlok implementációs fájlokként ismertek, mivel a fejlécfájlban (.h) deklarált metódusok összes definícióját tartalmazzák. A C++ projekt egésze egy végrehajtható alkalmazást eredményez, ha teljes egészében fordítjuk le.

## CPP fájlszerkezet

A CPP-fájl szerkezete egyszerű a fejlécfájlokhoz képest. Egy ilyen implementációs fájl fő célja az interfész és a megvalósítás szétválasztása. Ez azt eredményezi, hogy a fejlécfájlban található összes tagfüggvény deklarálódik, és a CPP-fájlban azok részletei is megjelennek. A CPP implementációs fájl egyszerű fájlként használható alkalmazás írásához, vagy osztálymegvalósításként.

### Független megvalósítás

A független alkalmazásként használt CPP-fájl az összes megvalósítást tartalmazhatja anélkül, hogy a fejlécfájlban metódus-deklarációra lenne szükség. Egy ilyen megvalósítás az implementációs fájlban meghatározott összes metódusból áll, ahol az alkalmazás bejegyzését egy fő metódus szabályozza, amely opcionális felhasználói bevitelt vesz argumentumként. Tartalmazhatja a C++ Standard Library bármely könyvtárát is, amelyeket a fájlban deklarált metódusok használhatnak.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Osztály megvalósítás

Az objektumorientált programozásban (OOP) egy CPP-fájlt használnak osztálydefinícióként. Ebben az esetben az összes osztályadattag és tagfüggvény deklarálva van a fejlécfájlban. Minden fejlécfájl hivatkozhat a szokásos könyvtári metódusokra is. Az osztálydefiníciós CPP fájl a fejlécfájlra hivatkozik egy include utasításban a fájl elején. A szoftverfejlesztők többnyire megjegyzéseket helyeznek el az ilyen osztálymegvalósítási fájl elején, amelyek információt adnak a fájl tényleges tartalmáról, a szerző adatairól és a megvalósítás dátumáról. Ilyen esetekben a fejléc-megvalósítási fájloknak azonos nevekkel kell rendelkezniük. A következő példa egy ilyen fejléc- és implementációs fájlra.

### Fejlécfájl

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP implementációs fájl

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Hivatkozások

* [Osztálymegvalósítás – a Wikipédia által](https://en.wikipedia.org/wiki/Class_implementation_file)

