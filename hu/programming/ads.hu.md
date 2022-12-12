
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS fájl – Ada specifikációs fájlformátum",
  "description":"Ismerje meg, mi az ADS-fájlformátum, példákkal és API-kkal, amelyek ADS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mi az ADS fájl?

Az ADS fájl egy Ada programozási projekt specifikációs fájlja. Hasonló a Java osztályához, vagy a fejléc és a megvalósítás párjához C++ esetén. Az Ada csomag nyilvános és privát specifikációi az .ads fájlban tárolódnak. Ezzel szemben az .adb fájl tartalmazza a megvalósítást, vagyis az Ada törzseket. A [C++](/hu/programing/cpp/)-hez hasonlóan az Ada is az OOP-tól független elkülönítést kínál a specifikációk és a megvalósítások között.

Az ADS fájlok bármely szövegszerkesztőben megnyithatók, például a Microsoft Notepad, Notepad++ és Atom segítségével.

## ADS fájlformátum

Az ADS fájlok egyszerű szöveges fájlformátumúak, és bármilyen szövegszerkesztővel megnyithatók/szerkeszthetők. Az Ada csomagok hierarchiákba rendezhetők. A gyermekegységet a következő módon lehet deklarálni:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Hivatkozások

* [Ada-csomagok](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

