{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DDL e le API che possono creare e aprire file DDL.",
  "title" :"Formato file DDL - Un file del linguaggio di definizione dei dati",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Che cos'è un file DDL?

Un file con estensione .ddl è un file Data Definition Language che viene utilizzato per definire lo schema di un database. Contiene istruzioni/comandi per lavorare con strutture di database come tabelle, colonne, record e altri campi. I comandi in un file DDL sono scritti in [SQL](/it/database/sql/) e possono eseguire operazioni come la creazione di tabelle nel database, l'eliminazione e l'aggiornamento. Uno schema di database è di proprietà di chi è stato creato e tutte le operazioni CRUD possono essere eseguite su di esso. Le applicazioni più diffuse in grado di creare e aprire file DDL sono Windows Text Editor, Jetbrains Intellij Idea ed EclipseLink.

## Comandi DDL

Un singolo file DDL può contenere diversi comandi che, grazie alla sintassi corretta, verranno eseguiti in sequenza e apporteranno modifiche allo schema come la creazione di set di caratteri e tabelle, l'eliminazione di tabelle, la ridenominazione e la modifica delle tabelle. I seguenti comandi DDL sono comunemente usati mentre si lavora con lo schema del database.

`CREATE` - Utilizzato per creare il database oi suoi oggetti (come tabella, indice, funzione, viste, procedura di archiviazione e trigger).

`DROP` – Usato per eliminare oggetti dal database.

`ALTER` - Usato per alterare la struttura del database.

`TRUNCATE` – Utilizzato per rimuovere tutti i record da una tabella, inclusi tutti gli spazi allocati per i record vengono rimossi.

`COMMENT` – Aggiunge commenti al dizionario dei dati.

`RENAME` – Rinomina un oggetto esistente nel database.

## Esempio DDL

L'esempio seguente mostra l'istruzione DDL per il comando CREATE che crea una tabella e ne definisce i campi.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Riferimenti ##

* [DDL di Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

