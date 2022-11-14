{
  "date" : "2021-08-24",
  "keywords" :[ "file wdb", "formato file wdb", "cos'è un file wdb", "file", "esempio wdb", "estensione file wdb", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file WDB e le API che possono creare e aprire file WDB.",
  "title" :"WDB - File di traccia di SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Che cos'è un file WDB?
Un file con estensione .wdb è in realtà un file di database creato da Microsoft Works che è stato utilizzato per eseguire funzioni come un sistema di gestione di database. Il file WDB è simile al file di Access Database ([MDB](/it/database/mdb/)), ma meno efficiente e con maggiori limitazioni. I file WDB non possono essere aperti utilizzando Microsoft Access. Tuttavia, è possibile aprire il file WDB in Microsoft Works e quindi esportarlo in un file MDB per aprire un file WDB in MS Access.

## Formato file WDB
Il database di Microsoft Works è il formato di database nativo della suite per ufficio Microsoft Works. A causa della natura proprietaria del formato e di alcune limitazioni. I file WDB non possono essere aperti in nessun altro software diverso da Microsoft Works. Nel formato file è possibile trovare un'intestazione ricorrente di 10 byte prima di ciascuna delle stringhe di testo ASCII che rappresentano i valori dei campi terminati con un valore NULL. L'intestazione generalmente inizia con un **\x0f** byte e NULL, seguito da 4 byte di dati alternati a NULL.

### Struttura del file

La struttura del file WDB è riportata di seguito:
- **1a intestazione**: dall'inizio del file, che termina con \x25\x00\xf2 e 244 byte NULL
- **2a intestazione**: inizia con \xffT - cioè \xff\x54 e si estende per 4096 byte, che contiene nomi di colonne/campi e altre cose, e sembra iniziare alla posizione del byte 6144.
- **Campo**: il valore ha un'intestazione di 10 byte, con il seguente formato: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , parte 2} {db 4} \x00. il byte di dati 2 è il numero del campo, il byte di dati 3 è il numero del record (aggiungendo il byte di dati 3, parte 2 quando supera i 256 record).


## Riferimenti ##

* [Utente:JesseW/formato wdb](https://en.wikipedia.org/wiki/Utente:JesseW/wdb_format)

