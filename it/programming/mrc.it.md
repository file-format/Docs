{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "file", "estensione", "formato file", "implementazione mrc", "Guida alla programmazione", "esempio mrc", "mIRC", "linguaggio di script mIRC", "file di INI", " linguaggio di scripting mSL", "linguaggio mIRC", "script mIRC", "linguaggio di scripting" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - File del linguaggio di script mIRC",
  "description":"Scopri il formato di file MRC e le API che possono creare e aprire file MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Che cos'è un file MRC?

mIRC è un linguaggio di scripting integrato come client IRC (Internet Relay Chat) nel sistema operativo Windows. Fornisce una funzione di protezione dallo spamming per uso personale e del canale. Per fornire una migliore esperienza di compatibilità con l'utente, questo linguaggio di scripting mIRC consente la creazione di finestre di dialogo. I file che contengono script, per lo più in un formato di testo normale, vengono archiviati con l'estensione di MRC o come file di [INI](/it/system/ini/). Le funzioni di questo linguaggio sono note come comandi e identificatori (quando restituiscono valore).

Il linguaggio mIRC fornisce il caricamento di più file di script contemporaneamente. D'altra parte, un file può far sì che l'altro non venga più utilizzato se caricato contemporaneamente. I comandi vengono salvati e possono esistere automaticamente in IRC. I comandi e gli alias utilizzati in questa lingua non prevedono la precedenza di nessuno dei caratteri.

mIRC è ampiamente utilizzato per fare in modo che i bot gestiscano un canale automaticamente, ma può anche essere modificato dal linguaggio di scripting msL. Può introdurre molte nuove funzionalità come macro, capacità di riproduzione musicale, piccole macro e funzioni, giochi di base o gestione di piccole applicazioni.


## Breve storia ##

Questo linguaggio di scripting è stato sviluppato per la prima volta nel 1995 da Khaled Adam Bey. Anche il design del linguaggio di scripting è stato creato da Khalid. L'obiettivo di questo linguaggio era la programmazione basata sugli eventi. Inizialmente, l'estensione di file utilizzata per i file di questo linguaggio di programmazione era .mrc e .ini. Inoltre, è stato sviluppato sotto licenza di software proprietario.

## Specifiche tecniche ##

Alcune funzioni sono personalizzate tramite script tramite questo linguaggio mIRC e sono note come alias. Quando questi alias restituiscono valori, sono noti come identificatori personalizzati. Tutte le variabili contenute in questo linguaggio mIRC sono tipizzate dinamicamente. I sigilli sono usati dagli script mIRC. Un'altra caratteristica di questo linguaggio di scripting sono i popup. Gli utenti possono chiamare i popup semplicemente selezionandoli. I telecomandi sono specificati per determinati eventi. I telecomandi vengono chiamati quando si verifica l'evento relativo.

I token delimitati da spazi vengono utilizzati per interrompere ogni riga di codice di questo linguaggio. Esistono altre estensioni popolari utilizzate per i file mIRC come MDX (mIRC Dialog Extension) e DCX (Dialog Control Extension). Entrambi sono estensioni di dialogo e sono relativamente più popolari. I costrutti linguistici sono indicati dalla nomenclatura di questo linguaggio di scripting. Il linguaggio mIRC coinvolge diversi aspetti di un linguaggio di scripting come variabili locali e globali, variabili binarie, tabelle hash e gestione dei file.


## Esempio di formato file MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/it/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Riferimento ##

* [MIRC - di Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)



