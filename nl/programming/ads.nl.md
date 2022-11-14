
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS-bestand - Ada-specificatiebestandsformaat",
  "description":"Meer informatie over wat het ADS-bestandsformaat is met voorbeelden en API's die ADS-bestanden kunnen maken en openen.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Wat is een ADS-bestand?

Een ADS-bestand is een specificatiebestand voor een Ada-programmeerproject. Het is vergelijkbaar met een klasse voor Java, of het kop- en implementatiepaar in het geval van C++. De publieke en private specificaties van het Ada-pakket worden opgeslagen in het .ads-bestand. Het .adb-bestand daarentegen bevat de implementatie- of Ada-instanties. Net als [C++](/nl/programming/cpp/), biedt Ada een scheiding tussen specificaties en implementaties onafhankelijk van OOP.

ADS-bestanden kunnen worden geopend in elke teksteditor, zoals Microsoft Notepad, Notepad++ en Atom.

## ADS-bestandsindeling

ADS-bestanden hebben een eenvoudig tekstbestandsformaat en kunnen met elke teksteditor worden geopend/bewerkt. Ada-pakketten kunnen in hiërarchieën worden georganiseerd. Een kindeenheid kan op de volgende manier worden aangegeven:

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

## Referenties

* [Ada-pakketten](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

