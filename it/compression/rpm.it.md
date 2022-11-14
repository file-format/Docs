{
  "date" : "2021-04-08",
  "keywords" :["file rpm", "formato file rpm", "cos'è un file rpm", "file", "esempio rpm", "estensione file rpm","estensione", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - File di gestione dei pacchetti di Red Hat",
  "description":"Scopri il formato di file RPM e le API che possono creare e aprire file RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Che cos'è un file RPM?

Un file con estensione .rpm è un pacchetto del sistema operativo Red Hat Linux per l'installazione di programmi su sistemi Linux. Red Hat Package Manager utilizza il formato file RPM ed è un sistema di gestione dei pacchetti gratuito e open source. Sebbene i file RPM possano essere usati così come sono per l'installazione di programmi, questi possono essere convertiti in altri formati di pacchetto come [DEB](/it/compression/deb/) usando il programma Debian chiamato Alien.

## Formato file RPM

Un file RPM è un binario che può contenere un insieme di file. Il più delle volte, i file RPM sono "RPM binari" che sono gli eseguibili compilati del software. Il file RPM può contenere RPM di origine (SRPM) che possono essere utilizzati per creare il pacchetto dal codice sorgente. Il formato del file RPM è composto da quattro sezioni.

* Lead - Identifica il file come un file RPM
* Firma: può essere utilizzata per garantire l'integrità e/o l'autenticità
* Intestazione: contiene i metadati inclusi il nome del pacchetto, la versione, l'architettura, l'elenco dei file, ecc.
* Archivio file - Conosciuto anche come payload, che di solito è in formato cpio, compresso con [GZIP](/it/compression/gz/)

## Riferimenti

* [RPM - Wikipedia](https://rpm.org)
* [Documentazione RPM](https://rpm.org/documentation.html)

