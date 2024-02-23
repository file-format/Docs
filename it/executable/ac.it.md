{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Scopri il formato file AC e le API in grado di creare e aprire file ACCDB.",
  "title" : "Formato file AC: file di script Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-it",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Cos'è un file AC?

Il file AC è il file di script Autoconf. **Autoconf** è un pacchetto estensibile di macro M4 che produce script di shell per configurare automaticamente i pacchetti di codice sorgente del software. Questi script possono adattare i pacchetti a molti tipi di sistemi simili a UNIX senza l'intervento manuale dell'utente. Autoconf crea uno script di configurazione per un pacchetto da un file modello che elenca le funzionalità del sistema operativo che il pacchetto può utilizzare, sotto forma di chiamate macro M4.

Producing configuration scripts using Autoconf requires GNU M4. Dovresti installare GNU M4 (almeno la versione 1.4.6, anche se è consigliata la 1.4.13 o successiva) prima di configurare Autoconf, in modo che lo script di configurazione di Autoconf possa trovarlo. Gli script di configurazione prodotti da Autoconf sono autonomi, quindi i loro utenti non hanno bisogno di avere Autoconf (o GNU M4).

## Come aprire il file AC?

AC sta per Configurazione Automatica. È uno script generato da GNU Autoconf che consente di adattare il codice sorgente del software a vari sistemi simili a Posix testando le funzionalità necessarie nel pacchetto. Lo script è chiamato file AC.

## Principali componenti degli strumenti automatici

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools è una raccolta di pacchetti correlati che, se utilizzati insieme, eliminano gran parte delle difficoltà legate alla creazione di software portatile. Questi strumenti, insieme ad alcuni file di input relativamente semplici forniti a monte, vengono utilizzati per creare il sistema di compilazione per un pacchetto.

**Una panoramica di base su come i principali componenti degli strumenti automatici si incastrano.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

In una configurazione semplice:

- Il programma `autoconf` produce uno script di configurazione da `configure.in` o `configure.ac`.
- Il programma `automake` produce un Makefile.in da un Makefile.am.
- Lo script `configure` viene eseguito per produrre uno o più file Makefile dai file Makefile.in.
- Il programma `make` utilizza il Makefile per compilare il programma.

## Riferimenti
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Le basi degli Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



