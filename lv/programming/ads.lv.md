
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADS fails — Ada specifikācijas faila formāts",
  "description":"Uzziniet, kas ir ADS faila formāts, izmantojot piemēru un API, kas var izveidot un atvērt ADS failus.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-lv",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas ir ADS fails?

ADS fails ir Ada programmēšanas projekta specifikācijas fails. Tas ir līdzīgs Java klasei vai galvenes un ieviešanas pārim C++ gadījumā. Ada pakotnes publiskās un privātās specifikācijas tiek glabātas .ads failā. Turpretim .adb fails satur ieviešanu jeb Ada korpusus. Tāpat kā [C++](/programming/cpp/), arī Ada piedāvā specifikāciju un ieviešanas nošķiršanu neatkarīgi no OOP.

ADS failus var atvērt jebkurā teksta redaktorā, piemēram, Microsoft Notepad, Notepad++ un Atom.

## ADS faila formāts

ADS faili ir vienkārša teksta faila formātā, un tos var atvērt/rediģēt ar jebkuru teksta redaktoru. Ada pakotnes var sakārtot hierarhijās. Bērnu vienību var deklarēt šādi:

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

## Atsauces

 * [Ada pakotnes](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

