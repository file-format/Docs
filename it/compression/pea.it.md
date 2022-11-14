{
  "date" : "2021-04-21",
  "keywords" :[ "file pisello", "formato file pisello", "cos'è un file pisello", "file", "esempio pisello", "estensione file pisello", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Formato file archivio PeaZip",
  "description":"Scopri il formato di file PEA e le API che possono creare e aprire file PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Che cos'è un file PEA?

Un file con estensione .pea, acronimo di Pack, Encrypt e Authenticate, è un archivio [zip](/it/compression/zip/) creato con l'applicazione software di archiviazione [PeaZip](https://peazip.github.io/). È dotato di compressione e output a più volumi e offre un modello di sicurezza flessibile tramite crittografia e crittografia autenticate. Ciò fornisce sia la privacy che l'autenticazione dei dati. L'utilità PeaZip è disponibile come motore open source che può essere compilato per diversi sistemi operativi secondo i requisiti.

## Formato file PEA

Le [Specifiche del formato del file PEA](https://peazip.github.io/pea_help.pdf) sono disponibili pubblicamente come riferimento per gli sviluppatori. Gli archivi PEA sono file binari con un modello di sicurezza flessibile e controlli di integrità ridondanti che vanno dai checksum agli hash crittograficamente forti. Questo definisce tre diversi livelli di comunicazione da controllare:

* Streams - il flusso di dati di output effettivo che è formato da più file di input e può essere scritto su più volumi di output
* Oggetti: file e cartelle di input inviati all'archivio .pea
* Volumi - file di archivio di output che può essere esteso a dimensioni definite dall'utente

Ognuno di questi è opzionale e può essere incorporato secondo i requisiti dell'utente. Il formato di file PEA può memorizzare un singolo flusso contenente oggetti illimitati. Ogni flusso ha una dimensione massima di 2^64 byte.

I file PEA offrono un controllo dell'integrità opzionale e la crittografia autenticata utilizzando AES in modalità EAX o HMAC, in alternativa Twofish e Serpent in modalità EAX.

### Intestazione archivio PEA

L'intestazione dell'archivio è di 10 byte ed è strutturata come segue.

|Byte|Descrizione|
---|---|
|1 | Campo byte magico per la disambiguazione del formato file: $EA|
|1 | Numero di versione|
|1 | Numero di revisione|
|1 | Schema di controllo del volume|
|1 | Dichiarazione del sistema operativo in cui è stato creato lo stream|
|1 | Dichiarazione della codifica della data e dell'ora del sistema operativo|
|1 | Dichiarare la codifica dei caratteri del nome degli oggetti|
|1 | Dichiarazione del tipo di CPU (codificata in 7 bit) e dell'endianness (in msb)|
|1 | Riservato per usi futuri|

## Riferimenti

* [Specifiche del formato file PEA](https://peazip.github.io/pea_help.pdf)
* [Formato file PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

