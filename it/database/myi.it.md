---
date: 2020-11-11
keywords: myi, .myi, formato di file myi, come aprire i file myi, estensione .myi, estensione myi
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file MYI
linktitle: MYI
description: "Scopri il formato di file MYI e le API che possono creare e aprire file MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## Che cos'è un file MYI? ##

MYI è anche conosciuto come il file MySQL MyISAM Index. Viene utilizzato per memorizzare gli indici per la tabella MyISAM da MySQL. L'indice del database MySQL definisce la struttura della tabella e contiene il meccanismo di controllo per verificare l'integrità delle tabelle.

## Formato file MYI ##

Il file MYI ha due parti, l'intestazione e i valori chiave.

### Intestazione MYI ###

L'intestazione contiene informazioni su opzioni, dimensioni file e chiavi. Le chiavi in MySQL vengono create con un comando come

```sql
CREATE [UNIQUE] INDEX.
```

I file che leggono e scrivono i file MYI si trovano nella directory ./myisam. Ha i seguenti file:

- mi_open.c: questo file contiene le routine che scrivono ogni sezione dell'intestazione.
- mi_create.c: questo file ha le routine che chiamano le routine mi_open.c.
- myisamdef.h: questo file contiene le definizioni della struttura.

L'intestazione ha le seguenti sezioni:

- state: lo stato è scritto da mi_open.c, mi_state_info_write(). Questa struttura si verifica una volta nel file.
- base: la base è scritta da mi_open.c, mi_base_info_write(). MI_BASE_INFO è la struttura corrispondente per la base in myisamdef.h. Questa struttura si verifica una volta nel file.
- keydef: il keydef è scritto da mi_open.c, mi_keydef_write(). MI_KEYDEF è la struttura corrispondente per il keydef in myisamdef.h. È una struttura a ricorrenza multipla che appare per ogni indice.
- recinfo: Il recinfo è scritto da mi_open.c, mi_recinfo_write(). MI_COLUMNDEF è la struttura corrispondente per recinfo in myisamdef.h. È una struttura a più occorrenze che appare una volta per ogni campo che appare in una chiave.

### Valori chiave ###

Le pagine in MySQL sono chiamate blocchi. I valori chiave sono in blocchi. Un blocco contiene informazioni da un solo indice. Ogni chiave contiene l'intero contenuto di tutte le colonne. La normale lunghezza del blocco è 0x0400 (1024) byte. Il puntatore ha un numero di dimensione fissa (4 byte) per le tabelle a riga fissa che contiene un numero di riga ordinale. Se la chiave è null, il byte è 0x00. Un blocco normale è pieno almeno per il 65% e in genere è pieno per l'80%.

Il file myisamdef.h contiene le seguenti informazioni espresse in costanti. Il numero massimo di chiavi è 32 (MI_MAX_KEY) e il numero massimo di segmenti in una chiave è 16 (MI_MAX_KEY_SEG). La lunghezza massima della chiave è 500 (MI_MAX_KEY_LENGTH). La lunghezza massima del blocco è 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Riferimenti ##

- [Il file .MYI](https://dev.mysql.com/doc/dev/mysql-server/latest/)

