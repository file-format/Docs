{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "was ist eine ah-Datei", "wie man eine h-Datei öffnet", "Erweiterung", "Datei", "h-Datei", "h-Dateiformat", "h-Dateierweiterung", "Beispiel für H-Datei"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ Header-Dateiformat",
  "description":"Erfahren Sie mehr über das H-Dateiformat und APIs, die H-Dateien erstellen und öffnen können.",
  "linktitle" :"H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Was ist eine H-Datei?

Eine mit der Dateierweiterung **h** gespeicherte Datei ist eine Header-Datei, die in C/C++-Dateien verwendet wird, um die Deklaration von Variablen, Konstanten und Funktionen aufzunehmen. Diese werden von den [C++](/de/programming/cpp/)-Implementierungsdateien referenziert, die die eigentliche Implementierung dieser Funktionen enthalten. Eine .h-Header-Datei kann auch zusätzliche Informationen wie Makrodefinitionen enthalten. Auf diese Header-Dateien wird in den C/C++-Dateien mit der Direktive „#include“ verwiesen.

Ein neues C++-Projekt enthält normalerweise eine spezielle Header-Datei mit dem Namen **stdafx.h**-Datei, die der Ausgangspunkt für alle Kompilierungsketten ist, und alle Header-Dateien können in dieser einzigen Datei enthalten sein. Eine .h-Datei kann mit jedem Texteditor, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ Compiler und vielen anderen Anwendungen geöffnet werden.

## .H-Dateiformat

Eine .h-Datei ist eine einfache Textdatei, die ihre eigenen Regeln zum Definieren der Syntax hat. Header-Dateien können die folgenden Informationen enthalten.

**`Variablen`** - Im Fall von objektorientierter Programmierung (OOP) enthält eine Klassenheaderdatei Definitionen aller Variablen auf Klassenebene, auf die über die Quellcodedateien der Implementierung zugegriffen werden kann
**`Methods Declaration`** - Alle Methodendeklarationen sind in den .h-Headerdateien enthalten, damit sie über mehrere Implementierungsdateien zugänglich sind.
**`Nicht-Inline-Funktionsdefinitionen`** - Header-Dateien können auch Definitionen von Nicht-Inline-Methoden enthalten.
**`Message Maps`** – Eine Headerdatei kann im Falle einer MFC-Quellcodeimplementierung auch Message Maps enthalten. In diesem Fall sind die Message Maps mit der Funktionalitätsimplementierung verknüpft, die mit UI-Elementen wie Schaltflächen, Kontrollkästchen, Optionsfeldern usw. verknüpft ist.


### Kopfschutz

Header-Dateien können zu komplexen Fehlern führen, wenn mehrere Deklarationen in derselben Datei enthalten sind, weil andere Header-Dateien hinzugefügt wurden. Diese doppelten Definitionen führen zu Compilerfehlern. Diese problematische Situation kann durch einen Mechanismus namens Header Guard vermieden werden, bei dem es sich um bedingte Kompilierungsdirektiven handelt, wie unten gezeigt.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Mit diesem Header prüft der Präprozessor, ob der `ANY_UNIQUE_NAME_HERE` bereits definiert wurde. Wenn der Header wiederholt in dieselbe Datei eingefügt wird, wird der Inhalt des Headers ignoriert.

## Beispiel einer H-Datei

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Verweise

* [Header Filer – Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

