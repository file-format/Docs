{
"dátum": "2023-06-08",
  "keywords": [
"hpp fájl",
"mi az a hpp fájl",
"mit tartalmaz a hpp fájl",
"hpp fájl példa",
"mi a hpp fájl formátuma",
"fájl",
"hpp fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "HPP fájlformátum - C++ fejlécfájl",
  "description":"További információ a HPP-formátumról és az API-król, amelyek HPP-fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Mi az a HPP fájl?

A ".hpp" fájlformátumot általában a C++ programozási nyelv fejlécfájljaihoz használják. A fejlécfájlok jellemzően olyan függvények, osztályok, változók és konstansok deklarációit és definícióit tartalmazzák, amelyeket a C++ projekt más forráskódfájljai használnak.

A fejlécfájlok használatának célja, hogy lehetőséget biztosítson a közös kód megosztására több forráskódfájl között anélkül, hogy magát a kódot megkettőzné. Ha a C++ forrásfájlnak hozzá kell férnie a fejlécfájl deklarációihoz vagy definícióihoz, akkor tartalmazza a fejlécfájlt a „#include” előfeldolgozó direktíva használatával.

A ".hpp" fájlkiterjesztést gyakran használják annak jelzésére, hogy egy fájl C++ fejlécfájl. A fejlécfájlokhoz nem kötelező ezt a kiterjesztést használni, és előfordulhat, hogy ".h" vagy más kiterjesztésű fejlécfájlokkal is találkozhat. A bővítmény kiválasztása nagyrészt megegyezés és személyes preferencia kérdése.

Ha egy C++ forrásfájl fejlécfájlt tartalmaz az "#include" használatával, a fordító hatékonyan egyesíti a fejlécfájl tartalmát a forrásfájllal, mielőtt egységként fordítaná azt. Ez lehetővé teszi a forrásfájl számára, hogy hozzáférjen a fejlécfájlban található deklarációkhoz és definíciókhoz, biztosítva a fordító számára a típusellenőrzés és kódgenerálás elvégzéséhez szükséges információkat.

## Mit tartalmaz a HPP fájl?

Íme néhány gyakori tartalom, amelyet a ".hpp" fájlban találhat:

- **Funkciódeklarációk:** A fejlécfájlok gyakran tartalmaznak függvénydeklarációkat azok tényleges megvalósítása nélkül. Ezek a deklarációk információt nyújtanak a függvény nevéről, a visszatérési típusról és a paraméterekről, lehetővé téve a többi forráskód-fájlnak a függvény használatát anélkül, hogy ismerniük kellene a megvalósítás részleteit.
- **Osztálydeklarációk:** A fejlécfájlok osztálydeklarációkat tartalmazhatnak, beleértve az osztálynevet, a tagváltozókat, a tagfüggvényeket és a hozzáférési specifikációkat. Az osztálydeklaráció fejlécfájlba való belefoglalásával más forráskódfájlok létrehozhatják az adott osztály objektumait, és hozzáférhetnek annak tagjaihoz.
- **Állandó deklarációk:** A fejlécfájlok konstansokat, például globális változókat vagy enumértékeket határozhatnak meg, amelyeket több forráskódfájl között kell megosztani. Ezek a konstansok úgy érhetők el, hogy a fejlécfájlt más forrásfájlokba foglalják, lehetővé téve számukra a meghatározott konstansok használatát.
- **Típusdefiníciók:** A fejlécfájlok tartalmazhatnak "typedef" kulcsszót használó típusdefiníciókat vagy "using" kulcsszót használó típusálneveket. Ezek a meghatározások új neveket hoznak létre a meglévő típusokhoz, így a kód olvashatóbbá és karbantarthatóbbá válik.
- **Beépített függvénydefiníciók:** Bizonyos esetekben a fejlécfájlok soron belüli függvénydefiníciókat tartalmazhatnak. A beépített függvények kis függvények, amelyeket a hívás helyén kibővítenek, nem pedig külön függvényként hívják meg őket. A soron belüli függvénydefiníció beépítése a fejlécfájlba lehetővé teszi a fordító számára, hogy a függvényhívást közvetlenül függvénytörzsre cserélje, ami potenciálisan javítja a teljesítményt.

## HPP fájl példa

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Mi a HPP fájl formátuma?

A HPP egy egyszerű szöveges fájl, de követi a C++ programozási nyelv általános szabályait és szintaxisát. Íme a ".hpp" fájl általános formátumának és szerkezetének lebontása:

- **Fejlécvédők:** Általában a ".hpp" fájl fejlécvédőkkel kezdődik, hogy megakadályozza ugyanazon fájl többszöri beillesztését. Ez olyan előfeldolgozó direktívák használatával érhető el, mint az `#ifndef`, `#define` és `#endif`. A fejlécvédelem biztosítja, hogy a fájl tartalma csak egyszer kerüljön bele a fordítási folyamat során.
- **Kiállítások szerepeltetése:** A fejlécvédők után további szükséges fejlécfájlokat is felvehet az `#include` direktíva használatával. Ezek lehetnek szabványos könyvtárfejlécek vagy más, a kód által megkövetelt egyéni fejlécek.
- **Deklarációk és definíciók:** A ".hpp" fájl elsődleges tartalma az osztályok, függvények, konstansok, típusálnevek és egyéb elemek deklarációi és bizonyos esetekben definíciói. Például deklarálhat osztályokat a „class” kulcsszó használatával, a függvényeket a visszatérési típusuk, nevük és paraméterlistájuk használatával, a konstansokat pedig a „const” kulcsszóval, amelyet típusuk és nevük követ.
- **Beépített függvénydefiníciók:** Bizonyos esetekben a soron belüli függvénydefiníciókat közvetlenül a ".hpp" fájlba is belefoglalhatja. A beágyazott függvények általában az osztálytörzsben vannak definiálva, ami azt jelenti, hogy a függvénydefiníció a deklaráció mellett szerepel. Ezt úgy lehet megtenni, hogy a függvénydefiníciót a "inline" kulcsszó előtaggal rögzíti.
- **Névterek deklarációi:** Ha névtereket használ a kódban, deklarálhatja azokat a ".hpp" fájlban. Ez a `namespace` kulcsszó használatával történik, amelyet a névtér neve követ, és a megfelelő kódot a névtér blokkba zárja.

## Hivatkozások
* [Fejlécfájlok (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

