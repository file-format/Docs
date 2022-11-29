
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS-fil - Ada Specification File Format",
  "description":"Läs mer om vad ADS-filformat är med exempel och API:er som kan skapa och öppna ADS-filer.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Vad är en ADS-fil?

En ADS-fil är en specifikationsfil för ett Ada-programmeringsprojekt. Det liknar en klass för Java, eller header- och implementeringsparet i fallet med C++. De offentliga och privata specifikationerna för Ada-paketet lagras i .ads-filen. .adb-filen innehåller däremot implementeringen, eller Ada-kroppar. Liksom [C++](/sv/programming/cpp/) erbjuder Ada separation mellan specifikationer och implementeringar oberoende av OOP.

ADS-filer kan öppnas i vilken textredigerare som helst som Microsoft Notepad, Notepad++ och Atom.

## ADS-filformat

ADS-filer är i enkel textfilformat och kan öppnas/redigeras med vilken textredigerare som helst. Ada-paket kan organiseras i hierarkier. En barnenhet kan deklareras på följande sätt:

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

## Referenser

* [Ada-paket](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

