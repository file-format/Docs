
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier ADS - Format fișier de specificații Ada",
  "description":"Aflați despre ce este formatul de fișier ADS cu exemple și API-uri care pot crea și deschide fișiere ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Ce este un fișier ADS?

Un fișier ADS este un fișier de specificații pentru un proiect de programare Ada. Este similar cu o clasă pentru Java sau cu perechea antet și implementare în cazul C++. Specificațiile publice și private ale pachetului Ada sunt stocate în fișierul .ads. În schimb, fișierul .adb conține implementarea sau corpurile Ada. La fel ca [C++](/ro/programming/cpp/), Ada oferă separare între specificații și implementări independent de OOP.

Fișierele ADS pot fi deschise în orice editor de text, cum ar fi Microsoft Notepad, Notepad++ și Atom.

## Format de fișier ADS

Fișierele ADS sunt în format simplu de fișier text simplu și pot fi deschise/editate cu orice editor de text. Pachetele Ada pot fi organizate în ierarhii. O unitate copil poate fi declarată în felul următor:

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

## Referințe

* [Pachete Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

