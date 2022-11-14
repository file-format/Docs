{
  "date" : "2019-12-09",
  "keywords" :[ "file zip", "formato file zip", "cos'è un file zip", "file", "esempio zip", "estensione file zip", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CERNIERA LAMPO",
  "description":"Cos'è un file ZIP e le API che possono creare e aprire file ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Che cos'è un file ZIP? ##

Un file con estensione .zip è un archivio che può contenere uno o più file o directory. L'archivio può avere una compressione applicata ai file inclusi per ridurre le dimensioni del file ZIP. Il formato di file ZIP è stato reso pubblico nel febbraio 1989 da Phil Katz per aver ottenuto l'archiviazione di file e cartelle. Il formato è stato inserito nell'utilità [PKZIP](https://www.pkware.com/pkzip), creata da PKWARE, Inc. Subito dopo la disponibilità di [specifiche disponibili](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), molte aziende hanno inserito il formato di file ZIP nelle loro utilità software, tra cui Microsoft (da Windows 7), Apple (Mac OS X) e molti altri.

## Breve storia del formato di file ZIP

La storia del formato del file ZIP risale all'evento legale intentato da System Enhancement Associates (SEA) contro PKWARE per aver utilizzato la sua utility ARC senza autorizzazioni per il suo marchio e i diritti d'autore dell'aspetto del prodotto e dell'interfaccia utente. In precedenza, Phil Katz, aveva riscritto il codice sorgente di SEA e rilasciato PKXARC, un estrattore ARC, e PKARC, un compressore di file, come freeware per sistemi basati su MS-DOS. Perdendo nella causa, PKWARE non poteva più usare tutto ciò che riguardava ARC. È qui che è nata la creazione di una nuova compressione di file, denominata ZIP, che è stata resa parte dell'utilità PKZIP presso PKWARE, Inc.

Katz ha rilasciato le specifiche del formato del file ZIP nel pubblico dominio, pur mantenendo i diritti di proprietà sulla sua utility di compressione ed estrazione, ad esempio PKZIP. Il sistema di compressione ZIP era (ed è) in grado di archiviare i file in una cartella per mezzo di un algoritmo di controllo di ridondanza ciclico a 32 bit ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) per comprimere i file taglie. A differenza di ARC, le cartelle .ZIP includevano un file di directory che svolgeva il ruolo di libro di codici di un crittografo, contenente le informazioni necessarie per il rendering dei file compressi.

## Metodi di compressione supportati in ZIP

In base alle specifiche del formato file .ZIP, sono supportati i seguenti metodi di compressione.

* Store - non implica alcuna compressione
* Restringersi
* Riduzione (Ciò implica fattori di compressione che vanno dal livello 1 al livello 4)
* Implodere
* Sgonfia
* Sgonfia64
* BZIP2
* LZMA (EFS)
* Pacchetto Wav
* PPMd versione I, Rev 1

DEFLATE è il metodo di compressione comunemente usato che è un algoritmo di compressione della data senza perdita di dati che utilizza una combinazione della codifica LZ77 e Huffman ed è dettagliato in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specifiche del formato file ZIP

I file ZIP hanno la capacità di archiviare più file utilizzando diverse tecniche di compressione mentre allo stesso tempo supportano la memorizzazione di un file senza alcuna compressione. Ogni file viene archiviato/compresso individualmente, il che aiuta a estrarli o aggiungerne di nuovi, senza applicare compressione o decompressione all'intero archivio.

### Formato file ZIP complessivo

Ogni file Zip è strutturato nel modo seguente:


|ZIP Formato file
---|
|Intestazione file locale 1
|Dati file 1
|Descrittore dati 1
|Intestazione file locale 2
|Dati file 2
|Descrittore dati 2
| ....
| ....
|Intestazione file locale N
|Dati file n
|Descrittore dati N
|Intestazione di decrittografia dell'archivio
|Archivia record di dati aggiuntivi
|Direttorio centrale

Il formato di file ZIP utilizza l'algoritmo CRC a 32 bit a scopo di archiviazione. Per eseguire il rendering dei file compressi, un archivio ZIP contiene una directory alla sua estremità che conserva la voce dei file contenuti e la loro posizione nel file di archivio. Pertanto, svolge il ruolo di codifica per incapsulare le informazioni necessarie per il rendering dei file compressi. I lettori ZIP utilizzano la directory per caricare l'elenco dei file senza leggere l'intero archivio ZIP. Il formato mantiene doppie copie della struttura della directory per fornire una maggiore protezione contro la perdita di dati.

Ogni file in un archivio ZIP è rappresentato come una singola voce in cui ogni voce è costituita da un'intestazione del file locale seguita dai dati del file compresso. La directory alla fine dell'archivio contiene i riferimenti a tutte queste voci di file. I lettori di file ZIP dovrebbero evitare di leggere le intestazioni dei file locali e tutti i tipi di elenchi di file dovrebbero essere letti dalla directory. Questa directory è l'unica fonte di voci di file valide nell'archivio poiché i file possono essere aggiunti anche verso la fine dell'archivio. Ecco perché se un lettore legge le intestazioni locali di un archivio ZIP dall'inizio, può leggere voci non valide (cancellate) e anche quelle non fanno parte della Directory che viene eliminata dall'archivio.

L'ordine delle voci dei file nella directory centrale non deve necessariamente coincidere con l'ordine delle voci dei file nell'archivio.

### Voci di file ZIP

Le voci nel file ZIP sono disposte una dopo l'altra in cui ciascuna voce è composta da:

* Intestazione del file locale
* Campi dati aggiuntivi opzionali
* Dati utente (opzionalmente compressi/opzionalmente crittografati)

L'intestazione del file locale di ogni voce rappresenta le informazioni sul file come il commento, la dimensione del file e il nome del file. I campi dati aggiuntivi (opzionali) possono contenere informazioni per le opzioni di estensibilità del formato ZIP.

#### Intestazione del file locale

L'intestazione del file locale ha una struttura di campo specifica composta da valori multibyte. Tutti i valori vengono archiviati in ordine di byte little-endian in cui la lunghezza del campo conta la lunghezza in byte. Tutte le strutture in un file ZIP utilizzano firme a 4 byte per ciascuna voce del file. La fine della firma della directory centrale è 0x06054b50 e può essere distinta utilizzando la propria firma univoca. Di seguito è riportato l'ordine delle informazioni memorizzate nell'intestazione del file locale.


|Offset|Byte|Descrizione
---|---|---|
|0|4|Firma dell'intestazione del file locale # 0x04034b50 (letto come numero little-endian)
|4|2|Versione necessaria per estrarre (minimo)
|6|2|Segnale bit per uso generico
|8|2|Metodo di compressione
|10|2|Ora dell'ultima modifica del file
|12|2|Data dell'ultima modifica del file
|14|4|CRC-32
|18|4|Formato compresso
|22|4|Dimensioni non compresse
|26|2|Lunghezza nome file (n)
|28|2|Lunghezza campo extra (m)
|30|n|Nome file
|30+n|m|Campo extra

#### Intestazione del file della directory centrale


|Offset|Byte|Descrizione
---|---|---|
|0|4|Firma dell'intestazione del file della directory centrale # 0x02014b50
|4|2|Versione realizzata da
|6|2|Versione necessaria per estrarre (minimo)
|8|2|Blocco di bit per uso generico
|10|2|Metodo di compressione
|12|2|Ora dell'ultima modifica del file
|14|2|Data dell'ultima modifica del file
|16|4|CRC-32
|20|4|Formato compresso
|24|4|Dimensioni non compresse
|28|2|Lunghezza nome file (n)
|30|2|Lunghezza campo extra (m)
|32|2|Lunghezza commento file (k)
|34|2|Numero del disco in cui inizia il file
|36|2|Attributi del file interno
|38|4|Attributi del file esterno
|42|4|Offset relativo dell'intestazione del file locale. Questo è il numero di byte tra l'inizio del primo disco su cui si trova il file e l'inizio dell'intestazione del file locale. Ciò consente al software che legge la directory centrale di individuare la posizione del file all'interno del file ZIP.
|46|n|Nome del file
|46+n|m|Campo extra
|46+n+m|k|Commento file

#### Fine del record della directory centrale


|Offset|Byte|Descrizione
---|---|---|
|0|4|Fine firma della directory centrale # 0x06054b50
|4|2|Numero di questo disco
|6|2|Disco dove inizia la directory centrale
|8|2|Numero di record della directory centrale su questo disco
|10|2|Numero totale di record della directory centrale
|12|4|Dimensione della directory centrale (byte)
|16|4|Offset dell'inizio della directory centrale, relativo all'inizio dell'archivio
|20|2|Lunghezza commento (n)
|22|n|Commento

## Riferimenti

* [Specifiche del formato file ZIP PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struttura del file PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

