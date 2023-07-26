{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file SQLITE e le API che possono creare e aprire file SQLITE.",
  "title" :"Formato file SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Che cos'è un file SQLite?

Un file con estensione .sqlite è un file di database SQL leggero creato con il software [SQLite](https://www.sqlite.org/index.html). È un database in un file stesso e implementa un motore di database [SQL](/it/database/sql/) autonomo, completo e altamente affidabile. I file di database SQLite possono essere utilizzati per condividere contenuti avanzati tra i sistemi scambiando semplicemente questi file in rete. Quasi tutti i cellulari e i computer utilizzano SQLite per l'archiviazione e la condivisione dei dati ed è la scelta del formato file per le applicazioni multipiattaforma. Grazie al suo utilizzo compatto e alla sua facilità d'uso, viene fornito in bundle all'interno di altre applicazioni. Esistono collegamenti SQLite per linguaggi di programmazione come C, [C#](/it/programming/cs/), [C++](/it/programming/cpp/), [Java](/it/programming/java/), [PHP](/it/programming/php/ ), e molti altri.

## Formato file SQLite

SQLite in realtà è una libreria C-Language che implementa l'RDBMS SQLite utilizzando il formato file SQLite. Con l'evoluzione di nuovi dispositivi ogni singolo giorno, il suo formato di file è stato mantenuto compatibile con le versioni precedenti per adattarsi ai dispositivi più vecchi. Il formato di file SQLite è visto come un formato di archiviazione a lungo termine per i dati.

### Il file di database

Un database SQLite è completamente gestito tramite due file.
* File database principale - Contiene lo stato completo del database SQLite
* Rollback Journal - Memorizza informazioni aggiuntive in un secondo file e viene utilizzato durante l'esecuzione delle transazioni. Nel caso in cui SQLite sia in modalità WAL, viene mantenuto un file di registro della testina di scrittura.

#### File del diario

Questo file ha lo scopo di mantenere tutte le informazioni mantenute nel caso in cui l'ultima transazione non possa essere completata in casi come un crash del computer. Questo file viene utilizzato per ripristinare il file di database in uno stato coerente.

#### Pagine

Il file di database SQLite principale comprende una o più pagine. In qualsiasi momento, ogni pagina del database principale ha un unico utilizzo che è uno dei seguenti:

* La pagina del byte di blocco
* Una pagina di freelist
* Una pagina del tronco della freelist
* Una pagina foglia freelist
* Una pagina b-tree
* Una pagina interna del tavolo b-tree
* Una pagina della foglia del tavolo b-albero
* Una pagina interna dell'indice b-tree
* Una pagina foglia indice b-albero
* Una pagina di overflow del carico utile
* Una pagina della mappa del puntatore

La dimensione dei file di database SQLite può variare da pochi kilobyte a pochi gigabyte.

### Intestazione SQLite

L'intestazione del database SQLite si trova nei primi 100 byte del file di database. Ogni file di database SQLite valido inizia con 16 byte (in esadecimale):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. I dettagli dei campi di intestazione sono come nella tabella seguente.

|Offset|Dimensione|Descrizione|
---|---|---|
|0|16|La stringa di intestazione: "Formato SQLite 3\000"|
|16|2|La dimensione della pagina del database in byte. Deve essere una potenza di due tra 512 e 32768 inclusi, o il valore 1 che rappresenta una dimensione della pagina di 65536.|
|18|1|Versione scrittura formato file. 1 per eredità; 2 per WAL.|
|19|1|Versione letta formato file. 1 per eredità; 2 per WAL.|
|20|1|Byte di spazio "riservato" non utilizzato alla fine di ogni pagina. Di solito 0.|
|21|1|Frazione massima del carico utile incorporato. Deve essere 64.|
|22|1|Frazione minima del carico utile incorporato. Deve essere 32.|
|23|1|Frazione del carico utile foglia. Deve essere 32.|
|24|4|Contatore modifiche file.|
|28|4|Dimensione del file di database in pagine. La "dimensione del database nell'intestazione".|
|32|4|Numero di pagina della prima pagina del tronco della freelist.|
|36|4|Numero totale di pagine freelist.|
|40|4|Il cookie dello schema.|
|44|4|Il numero del formato dello schema. I formati di schema supportati sono 1, 2, 3 e 4.|
|48|4|Dimensione cache pagina predefinita.|
|52|4|Il numero di pagina della pagina b-tree radice più grande quando si è in modalità di vuoto automatico o di vuoto incrementale, altrimenti zero.|
|56|4|La codifica del testo del database. Un valore di 1 significa UTF-8. Un valore di 2 significa UTF-16le. Un valore di 3 significa UTF-16be.|
|60|4|La "versione utente" letta e impostata dal pragma user_version.|
|64|4|True (diverso da zero) per la modalità di vuoto incrementale. Falso (zero) altrimenti.|
|68|4|L'"ID applicazione" impostato da PRAGMA application_id.|
|72|20|Riservato per l'espansione. Deve essere zero.|
|92|4|La versione-valida per il numero.|
|96|4|SQLITE_VERSION_NUMBER|

## Riferimenti ##

* [Formato file SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Specifiche del linguaggio C](https://www.sqlite.org/c3ref/intro.html)

