{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File STR - File oggetto elenco strutture dBASE - Cos'è il file .str e come aprirlo?",
  "description" : "Informazioni sul file oggetto dell'elenco di strutture STR dBASE e su come aprirlo.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-it",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Cos'è un file STR?

Il formato file STR è comunemente associato a dBASE, un sistema di gestione di database. In dBASE, un file .str rappresenta in genere un file oggetto elenco di strutture. Questo file contiene la struttura di una tabella di database, comprese le informazioni sui campi (colonne) e le loro proprietà.

Il file oggetto dell'elenco di strutture (.str) contiene metadati come nomi di campi, tipi di dati, lunghezze di campo e qualsiasi altra proprietà associata a ciascun campo nella tabella del database. Viene utilizzato per definire la struttura della tabella del database senza contenere record di dati effettivi.

Programmi come dBASE o altri strumenti di gestione del database possono utilizzare questo file per comprendere il layout della tabella del database ed eseguire operazioni come interrogazioni, aggiornamenti o creazione di nuovi record basati su questa struttura.

Ecco un esempio di base di cosa potrebbe contenere un file STR:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Questo esempio descrive una tabella con quattro campi: ID, Nome, Età e DOB, insieme ai rispettivi tipi di dati e lunghezze.

## Come aprire il file STR?

Il modo principale per aprire i file .str è utilizzare dBASE stesso, in particolare sui sistemi operativi Windows. dBASE è in grado di leggere e interpretare il contenuto di questi file, consentendo agli utenti di visualizzare e lavorare con la struttura del database.

Poiché i file .str sono essenzialmente file di testo semplice che contengono informazioni sulla struttura del database, puoi anche aprirli utilizzando un editor di testo. Esempi di editor di testo includono Microsoft Notepad su Windows e Apple TextEdit su Mac. Una volta aperto in un editor di testo, sarai in grado di vedere il contenuto del file, inclusi nomi di campi, tipi di dati e altre informazioni strutturali, in un formato leggibile dall'uomo.

## Riferimenti
* [dBase](https://en.wikipedia.org/wiki/DBase)


