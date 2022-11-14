{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "estensione", "file cdb", "formato file cdb", "Tipo file database", "Formato file database", "che cos'è un file cdb" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file CDB e le API che possono creare e aprire file CDB.",
  "title" :"CDB - File di database costante",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Che cos'è un file CDB?
I file CDB vengono utilizzati in applicazioni mission-critical come la posta elettronica. Il CDB sta per "database costante", un pacchetto veloce, affidabile e semplice per la creazione o la lettura di database costanti. La sostituzione del database è sicura contro gli arresti anomali del sistema. Gli utenti non devono fermarsi durante una riscrittura. CDB funziona come un array associativo (su disco), associa le chiavi ai valori e consente di memorizzare più valori in un'unica chiave.

## Formato file CDB
Il formato di file CDB memorizza numeri, offset, lunghezze e valori hash in formato little endian come interi a 32 bit senza segno. Si ritiene che chiavi e dati siano stringhe di byte opache senza alcun trattamento speciale. All'inizio del database, l'intestazione a dimensione fissa rappresenta 256 tabelle hash elencando la loro posizione all'interno del file e la loro lunghezza negli slot. Di solito i dati vengono archiviati come una sequenza di record, ogni record memorizza la lunghezza della chiave, la lunghezza dei dati, la chiave e i dati. Non ci sono regole di ordinamento o allineamento. I record sono seguiti da una serie di 256 tabelle hash di varia lunghezza. Poiché zero è una lunghezza valida, potrebbero esserci meno di 256 tabelle hash archiviate fisicamente nel database, ma non ci sono 256 tabelle considerate. Le tabelle hash sono costituite da una serie di slot, ognuno dei quali contiene un valore hash e un record offset. Gli "slot vuoti" hanno un offset pari a zero.

### Struttura
Il database CDB è costituito da un intero set di dati in un unico file del computer. Contiene tre parti:
- Un'intestazione di dimensioni fisse
- Dati
- Una serie di tabelle hash.

Le ricerche sono disponibili solo per chiavi esatte. Le ricerche agiscono utilizzando il seguente algoritmo:

- Pulisci la chiave.
- Determina in quale tabella hash e slot deve trovarsi questo record.
- Testare lo slot indicato nella tabella hash.

Per le ricerche di chiavi con più di un valore, è possibile trovare valori aggiuntivi semplicemente riprendendo la ricerca allo slot successivo.

#### Caratteristiche

La struttura del database CDB offre diverse funzionalità:

##### Ricerche veloci
Una ricerca riuscita in un database enorme richiede normalmente solo due accessi al disco e una ricerca non riuscita ne richiede solo uno.
##### Basso sovraccarico
Un database utilizza 2048 byte, 24 byte per record e lo spazio per chiavi e dati.
##### Nessun limite casuale
CDB può gestire qualsiasi database fino a 4 gigabyte. Poiché non ci sono altre restrizioni, i record non devono nemmeno essere inseriti nella memoria. I database sono archiviati in un formato indipendente dalla macchina.
##### Sostituzione rapida del database atomico
Il comando **cdbmake** può riscrivere un intero database in due ordini di grandezza, più velocemente di altri pacchetti di hashing.
##### Dump veloci del database
**cdbdump** può stampare il contenuto di un database in un formato compatibile con cdbmake.


## Riferimenti ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [Specifica CDB](http://cr.yp.to/cdb.html)

