{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Crea file - File script Xcode Makefile",
  "description":"Scopri il formato XCode MakeFile e le API che possono creare e aprire file MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Che cos'è un file MAKE?

Un file MAKE è un file di script XCode che organizza la compilazione del codice. Viene utilizzato per compilare e collegare programmi da più file di codice sorgente. Questo aiuta a decidere quali parti di un'applicazione di grandi dimensioni devono essere ricompilate quando l'applicazione deve essere aggiornata. Fare in modo che i file utilizzino una serie di istruzioni per l'esecuzione a seconda dei file modificati.

## Esempio di formato file MAKE

Il contenuto seguente viene eseguito utilizzando l'utilità Make e gli output sono i seguenti.

```
hello:
	echo "hello world"
```
**Crea output**

```
$ make
echo "hello world"
hello world
```

## Riferimenti
* [XCode e Make - Forum Apple](https://developer.apple.com/forums/thread/657458)
* [Guida all'oggetto C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

