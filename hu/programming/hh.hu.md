{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "mi az a .hh fájl", ".hh fájl megnyitása", "kiterjesztés", "fájl", ".hh fájl", ".hh fájlformátum", " .hh fájlkiterjesztés",".HH fájl példa"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ fejlécfájl formátum",
  "description":"További információ a HH fájlformátumról és az API-król, amelyek HH fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Mi az a HH fájl?

A .hh kiterjesztésű fájl egy C++ fejlécfájl, amely változók, konstansok és függvények deklarációját tartalmazza. Ezeket a deklarációkat a megfelelő C++ implementációs fájlok használják, általában [.cpp](/hu/programming/cpp/) fájlként mentve, amelyek a felhasználói logika tényleges megvalósítását tartalmazzák. A .hh fejlécfájlok a megvalósítási CPP-fájlokban az "#include" direktíva használatával hivatkoznak. A lehető legtöbb fejlécfájlt hozzáadhatja C++ projektjéhez, hogy projektszintű deklarációkat is tartalmazzon.

## .HH fájlformátum

A .hh fájl egy egyszerű szöveges fájl, amely a fejlécfájl-definíciós szabályok figyelembevételével jön létre. A .hh fájlokban deklarált leggyakoribb információk a következők.

**`Változók`** – Objektumorientált programozás (OOP) esetén az osztályfejléc fájl tartalmazza az összes olyan osztályszintű változó definícióját, amely elérhető a megvalósítási forráskódfájlokon keresztül.
**`Methods Declaration`** – Az összes metódusdeklaráció megtalálható a .h fejlécfájlokban, hogy több megvalósítási fájlon keresztül is elérhető legyen.
**`Non-line Function Definitions`** - A fejlécfájlok nem soron belüli metódusok definícióit is tartalmazhatják.
**`Üzenetleképezések`** - A fejlécfájl üzenetleképezéseket is tartalmazhat MFC forráskód megvalósítása esetén. Ebben az esetben az üzenettérképek a funkcionalitás megvalósításához kapcsolódnak, amely olyan UI-elemekhez kapcsolódik, mint a gomb, jelölőnégyzet, rádiógombok stb.

## Különbség a .H és a .HH fájlok között

Úgy tűnik, nincs ilyen különbség a .h és .hh fejlécfájlok között, kivéve a megfelelő nyelvekhez javasolt használati módot, pl. [C](/hu/programming/c/) vagy C++. A fejlécfájlok e nyelvek szerinti elnevezése segít megkülönböztetni őket egy nagy projektben, amely C és C++ implementációkat is tartalmazhat.

Ezenkívül, ha a fejlécek kiterjesztéssel vannak elválasztva, a szerkesztő automatikusan alkalmazhatja a megfelelő formázást.

Összességében e két fájlformátum megkülönböztetése nem okoz kárt, de előnyös lesz, ezért érdemes követni a C és C++ megkülönböztetést.

### Fejlécvédők

A fejlécfájlok összetett hibákat okozhatnak, ha több deklaráció is szerepel ugyanabban a fájlban más fejlécfájlok hozzáadása következtében. Ezek az ismétlődő definíciók fordítóhibákat okoznak. Ez a problémás helyzet elkerülhető egy fejlécvédő mechanizmussal, amelyek feltételes fordítási direktívák, amint az alább látható.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Ezzel a fejléccel az előfeldolgozó ellenőrzi, hogy az `ANY_UNIQUE_NAME_HERE_HPP` már meghatározásra került-e. Ha a fejléc többször is szerepel ugyanabban a fájlban, a fejléc tartalma figyelmen kívül marad.

## Hivatkozások

* [Header Filers – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Különbség a .h és a .hh fájlformátumok között](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

