{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "che cos'è il file ah", "come aprire il file h", "estensione", "file", "file h", "formato file h", "estensione file h", "Esempio di file H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Formato file di intestazione C/C++",
  "description":"Scopri il formato di file H e le API che possono creare e aprire file H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Che cos'è un file H?

Un file salvato con **h estensione file** è un file di intestazione utilizzato nei file C/C++ per includere la dichiarazione di variabili, costanti e funzioni. Questi sono indicati dai file di implementazione [C++](/it/programming/cpp/) che contengono l'effettiva implementazione di queste funzioni. Un file di intestazione .h può anche includere informazioni aggiuntive come le definizioni delle macro. Questi file di intestazione sono referenziati nei file C/C++ usando la direttiva `#include`.

Un nuovo progetto C++ di solito contiene uno speciale file di intestazione con il nome **stdafx.h** file che è il punto di partenza per tutte le catene di compilazione e tutti i file di intestazione possono essere inclusi in questo singolo file. Un file .h può essere aperto con qualsiasi editor di testo, Eclipse IDE, Microsoft Visual Studio IDE, compilatore Borland C++ e molte altre applicazioni.

## Formato file .H

Un file .h è un file di testo normale che ha le proprie regole per definire la sintassi. I file di intestazione possono contenere le seguenti informazioni.

**`Variabili`** - In caso di programmazione orientata agli oggetti (OOP), un file di intestazione di classe contiene le definizioni di tutte le variabili a livello di classe accessibili attraverso i file di codice sorgente dell'implementazione
**`Dichiarazione dei metodi`** - Tutte le dichiarazioni dei metodi sono incluse nei file di intestazione .h per essere accessibili in più file di implementazione.
**`Definizioni di funzioni non in linea`** - I file di intestazione possono anche contenere definizioni di metodi non in linea.
**`Mappe dei messaggi`** - Un file di intestazione può anche contenere mappe dei messaggi in caso di implementazione del codice sorgente MFC. In tal caso, le mappe dei messaggi sono collegate all'implementazione della funzionalità che è collegata agli elementi dell'interfaccia utente come pulsante, casella di controllo, pulsanti di opzione, ecc.


### Guardie di testata

I file di intestazione possono generare errori complessi in cui più dichiarazioni sono incluse nello stesso file a seguito dell'aggiunta di altri file di intestazione. Queste definizioni duplicate generano errori del compilatore. Questa situazione problematica può essere evitata tramite un meccanismo chiamato header guard che sono direttive di compilazione condizionale come mostrato di seguito.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Con questa intestazione, il preprocessore controlla se `ANY_UNIQUE_NAME_HERE` è già stato definito. Se l'intestazione viene inclusa ripetutamente nello stesso file, il contenuto dell'intestazione verrà ignorato.

## Esempio di file H

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

## Riferimenti

* [File di intestazione - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

