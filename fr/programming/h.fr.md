{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","qu'est-ce qu'un fichier ah","comment ouvrir un fichier h", "extension", "fichier", "fichier h","format de fichier h", "extension de fichier h", "Exemple de fichier H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Format de fichier d'en-tête C/C++",
  "description":"En savoir plus sur le format de fichier H et les API qui peuvent créer et ouvrir un fichier H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Qu'est-ce qu'un fichier H ?

Un fichier enregistré avec l'**extension de fichier h** est un fichier d'en-tête utilisé dans les fichiers C/C++ pour inclure la déclaration des variables, des constantes et des fonctions. Ceux-ci sont référencés par les fichiers d'implémentation [C++](/fr/programming/cpp/) qui contiennent l'implémentation réelle de ces fonctions. Un fichier d'en-tête .h peut également inclure des informations supplémentaires telles que les définitions de macro. Ces fichiers d'en-tête sont référencés dans les fichiers C/C++ à l'aide de la directive `#include`.

Un nouveau projet C++ contient généralement un fichier d'en-tête spécial nommé fichier **stdafx.h** qui est le point de départ de toutes les chaînes de compilation et tous les fichiers d'en-tête peuvent être inclus dans ce fichier unique. Un fichier .h peut être ouvert avec n'importe quel éditeur de texte, Eclipse IDE, Microsoft Visual Studio IDE, le compilateur Borland C++ et beaucoup d'autres applications.

## Format de fichier .H

Un fichier .h est un fichier texte brut qui a ses propres règles pour définir la syntaxe. Les fichiers d'en-tête peuvent contenir les informations suivantes.

**`Variables`** - Dans le cas de la programmation orientée objet (POO), un fichier d'en-tête de classe contient les définitions de toutes les variables de niveau de classe accessibles dans les fichiers de code source d'implémentation
**`Déclaration de méthodes`** - Toutes les déclarations de méthodes sont incluses dans les fichiers d'en-tête .h pour être accessibles dans plusieurs fichiers d'implémentation.
**`Définitions de fonctions non en ligne`** - Les fichiers d'en-tête peuvent également contenir des définitions de méthodes non en ligne.
**`Message Maps`** - Un fichier d'en-tête peut également contenir des cartes de messages dans le cas d'une implémentation de code source MFC. Dans ce cas, les cartes de message sont liées à l'implémentation de la fonctionnalité qui est liée aux éléments de l'interface utilisateur tels que le bouton, la case à cocher, les boutons radio, etc.


### Gardes d'en-tête

Les fichiers d'en-tête peuvent générer des erreurs complexes lorsque plusieurs déclarations sont incluses dans le même fichier à la suite de l'ajout d'autres fichiers d'en-tête. Ces définitions en double génèrent des erreurs de compilation. Cette situation problématique peut être évitée via un mécanisme appelé garde d'en-tête qui sont des directives de compilation conditionnelle comme indiqué ci-dessous.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Avec cet en-tête, le préprocesseur vérifie si `ANY_UNIQUE_NAME_HERE` a déjà été défini. Si l'en-tête est inclus à plusieurs reprises dans le même fichier, le contenu de l'en-tête sera ignoré.

## Exemple de fichier H

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

## Références

* [Fichiers d'en-tête - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

