
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADS failas – Ada specifikacijos failo formatas",
  "description":"Sužinokite, kas yra ADS failo formatas, naudodamiesi pavyzdžiu ir API, kurios gali kurti ir atidaryti ADS failus.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-lt",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Kas yra ADS failas?

ADS failas yra Ada programavimo projekto specifikacijos failas. Tai panašu į Java klasę arba antraštės ir įgyvendinimo porą C++ atveju. Viešosios ir privačios Ada paketo specifikacijos saugomos .ads faile. Priešingai, .adb faile yra įgyvendinimas arba Ada korpusai. Kaip ir [C++](/programming/cpp/), Ada siūlo specifikacijų ir diegimų atskyrimą nepriklausomai nuo OOP.

ADS failus galima atidaryti bet kuriame teksto rengyklėje, pvz., Microsoft Notepad, Notepad++ ir Atom.

## ADS failo formatas

ADS failai yra paprasto teksto failo formato ir gali būti atidaryti / redaguoti naudojant bet kurį teksto rengyklę. Ada paketai gali būti suskirstyti į hierarchijas. Vaikų vienetas gali būti deklaruojamas tokiu būdu:

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

## Nuorodos

 * [Ada paketai](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

