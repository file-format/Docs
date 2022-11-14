{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AGI - Formato file interfaccia gateway Asterisk",
  "description":"Scopri cos'è il formato di file AGI con esempi e API che possono creare e aprire file AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Che cos'è un file AGI?

Un file AGI è un file di script utilizzato dal sistema di telefonia open source, Asterisk. Contiene informazioni che possono essere utilizzate per automatizzare i processi e il dialplan Asterisk. Utilizzando i file di script AGI, è possibile stabilire connessioni con database relazionali come PostgreSQL o MySQL. Inoltre, gli script AGI possono essere utilizzati anche per accedere ad altre risorse esterne. Gli script AGI possono trasferire il controllo del dialplan a uno script AGI esterno, consentendo ad Asterisk di eseguire attività complesse.

## Formato file AGI - Ulteriori informazioni

I file di script AGI vengono salvati come file di testo e possono essere aperti in qualsiasi editor di testo per apportare modifiche.

### Modello standard di comunicazione AGI

Lo script AGI carica le variabili ei loro valori inviati da Asterisk. Un aspetto comune di queste variabili è il seguente.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Queste variabili sono seguite da una riga vuota inviata da Asterisk, che mostra che lo script AGI può ora assumere il controllo del dialplan.

### Linguaggio di programmazione per file di script AGI

Gli script AGI possono in genere essere scritti in Perl, [PHP](/it/programming/php/), [C](/it/programming/c/), Pascal o Bourne Shell.

## Riferimenti

* [Script AGI Asterisk](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

