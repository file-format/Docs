
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADS-fil - Ada-specifikationsfilformat",
  "description":"Lær om, hvad ADS-filformat er med eksempler og API'er, der kan oprette og åbne ADS-filer.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-da",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Hvad er en ADS fil?

En ADS-fil er en specifikationsfil for et Ada-programmeringsprojekt. Det ligner en klasse til Java, eller header- og implementeringsparret i tilfælde af C++. Ada-pakkens offentlige og private specifikationer er gemt i .ads-filen. .adb-filen indeholder derimod implementeringen eller Ada-kroppe. Ligesom [C++](/programming/cpp/) tilbyder Ada adskillelse mellem specifikationer og implementeringer uafhængigt af OOP.

ADS-filer kan åbnes i enhver teksteditor, såsom Microsoft Notepad, Notepad++ og Atom.

## ADS filformat

ADS-filer er i simpelt tekstfilformat og kan åbnes/redigeres med enhver teksteditor. Ada-pakker kan organiseres i hierarkier. En underenhed kan deklareres på følgende måde:

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

## Referencer

 * [Ada-pakker](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

