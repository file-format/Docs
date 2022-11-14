
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADS - Formato file delle specifiche Ada",
  "description":"Scopri cos'è il formato di file ADS con esempi e API che possono creare e aprire file ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Che cos'è un file ADS?

Un file ADS è un file di specifiche per un progetto di programmazione Ada. È simile a una classe per Java o alla coppia di intestazione e implementazione in caso di C++. Le specifiche pubbliche e private del pacchetto Ada sono archiviate nel file .ads. Il file, .adb, invece, contiene l'implementazione, o corpi Ada. Come [C++](/it/programming/cpp/), Ada offre separazione tra specifiche e implementazioni indipendentemente dall'OOP.

I file ADS possono essere aperti in qualsiasi editor di testo come Microsoft Notepad, Notepad++ e Atom.

## Formato file ADS

I file ADS sono in un semplice formato di file di testo e possono essere aperti/modificati con qualsiasi editor di testo. I pacchetti Ada possono essere organizzati in gerarchie. Un'unità figlio può essere dichiarata nel modo seguente:

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

## Riferimenti

* [Pacchetti Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

