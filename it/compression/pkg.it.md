{
  "date" : "2021-04-08",
  "keywords" :[ "file pkg", "formato file pkg", "cos'è un file pkg", "file", "esempio pkg", "estensione file pkg", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - Formato file di archivio estensibile",
  "description":"Scopri il formato di file PKG e le API che possono creare e aprire file PKG.",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## Che cos'è un file PKG?

Un file con estensione .pkg è un file del pacchetto di installazione utilizzato per installare il software su macOS. Oltre ai computer Macintosh, viene utilizzato anche su iPhone. L'applicazione di installazione integrata di Apple può essere utilizzata per installare il contenuto di un file PKG. Un file PKG è simile a un file MSI utilizzato sul sistema operativo Windows per l'installazione del software. Durante l'installazione, questi file di pacchetto possono registrare messaggi che ti danno un'idea di quali cose extra sono installate da questo pacchetto.

## Formato file PKG

PKR sono file binari che vengono compressi per ridurre la dimensione complessiva del file. Da OSX 10.5, Apple ha introdotto pacchetti flat con file di installazione singoli. Questi sono diversi dai formati di confezionamento precedenti forniti come pacchetti anziché come file singoli. Questi pacchetti in bundle contenevano una gerarchia di directory strutturata che memorizzava i file in un modo che ne facilitava il recupero tramite alcuni file di indice. Il formato di file flat PKG è in realtà un archivio [XAR](/it/compression/xar/) che ha un:

* Intestazione - Definisce la dimensione, il checksum e le informazioni sulla versione
* Sommario: un documento XML che è (e deve) essere codificato come UTF-8 e viene archiviato all'inizio del file, semplificando la scansione dell'archivio per estrarre il singolo file
* Heap - heap non strutturato di dati a cui fa riferimento il TOC

## Riferimenti

* [Formato file pacchetto piatto](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - Wikipedia](https://en.wikipedia.org/wiki/.pkg)

