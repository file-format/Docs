{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "che cos'è un file jar", "come aprire un file jar", "estensione", "file", "file jar", "formato di file jar", "estensione .jar "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Formato file di archivio Java",
  "description":"Scopri il formato di file JAR e le API che possono creare e aprire file JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file JAR?

Un file con estensione .jar è un file di archivio Java che contiene molti diversi file relativi all'applicazione come un unico file. Questo formato di file è stato creato per ridurre la velocità di caricamento di un'applet Java scaricata nel browser tramite transazione HTTP, evitando di creare connessioni HTTP multiple. Un singolo file JAR può contenere file di classe Java ([.class](/it/programming/class/)), [images](/it/image/) e [suoni](/it/audio/). I singoli elementi all'interno di un file JAR possono essere firmati digitalmente dallo sviluppatore dell'applicazione per autenticarne l'origine. I file JAR vengono regolarmente utilizzati per creare API funzionali che contengono funzionalità specifiche relative a tale API.

## Formato file JAR

I file JAR si basano sul popolare [formato file ZIP](/it/compression/zip/) che archivia i suoi singoli file di contenuto in un unico file. Il formato di file JAR supporta le compressioni, risultando in una dimensione del file più piccola per il download e quindi migliora ulteriormente il tempo di download. [Specifiche del file JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce di Oracle fornisce dettagli completi sulle specifiche interne dei file JAR.

### Il file manifesto

Quando viene creato un file JAR, al suo interno viene creato automaticamente un file manifest che contiene le informazioni sui metadati sul contenuto del file JAR. Questo file mostra i contenuti che sono impacchettati all'interno del file JAR. Un tipico file Manifest ha il seguente aspetto che mostra le cartelle e le classi incluse nel file JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Specifiche del manifesto

Le specifiche manifest sono definite da Oracle come segue.

`file-manifest`: newline della sezione principale \*sezione-individuale

`sezione-principale`: info-versione nuova riga \*attributo-principale

`info-versione`: Versione-manifest: numero-versione

`numero-versione` : digit+{.digit+}*

`main-attribute`: (qualsiasi attributo principale legittimo) newline

`sezione-individuale`: Nome : valore newline \*perentry-attribute

`perentry-attribute`: (qualsiasi attributo perentry legittimo) newline

`nuova riga` : CR LF | LF | CR (non seguito da LF)

`digit`: {0-9}

### JAR eseguibile

I file JAR possono anche comprendere un'applicazione che può essere eseguita da Java Virtual Machine (JVM) simile a qualsiasi altra applicazione sul sistema operativo Microsoft Windows. In questo caso, la JVM deve conoscere il punto di ingresso dell'applicazione che è qualsiasi classe con un metodo main void statico pubblico. Il file manifest identifica tale classe con l'intestazione `Main-Class` nel seguente formato:

```
Main-Class: com.example.MyClassName
```



## Riferimenti

* [Panoramica del file JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Formato file JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

