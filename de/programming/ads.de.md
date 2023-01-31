
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS-Datei - Ada-Spezifikationsdateiformat",
  "description":"Erfahren Sie anhand von Beispielen und APIs, mit denen ADS-Dateien erstellt und geöffnet werden können, was das ADS-Dateiformat ist.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Was ist eine ADS-Datei?

Eine ADS-Datei ist eine Spezifikationsdatei für ein Ada-Programmierprojekt. Es ähnelt einer Klasse für Java oder dem Header- und Implementierungspaar im Fall von C++. Die öffentlichen und privaten Spezifikationen des Ada-Pakets sind in der .ads-Datei gespeichert. Die .adb-Datei hingegen enthält die Implementierung oder Ada-Bodys. Wie [C++](/de/programming/cpp/) bietet Ada eine von OOP unabhängige Trennung zwischen Spezifikationen und Implementierungen.

ADS-Dateien können in jedem Texteditor wie Microsoft Notepad, Notepad++ und Atom geöffnet werden.

## ADS-Dateiformat

ADS-Dateien haben ein einfaches Nur-Text-Dateiformat und können mit jedem Texteditor geöffnet/bearbeitet werden. Ada-Pakete können in Hierarchien organisiert werden. Eine untergeordnete Einheit kann auf folgende Weise deklariert werden:

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

## Verweise

* [Ada-Pakete](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

