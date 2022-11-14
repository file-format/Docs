{
  "date" : "2019-10-11",
  "keywords" :[ "file rar", "formato file rar", "cos'è un file rar", "file", "esempio rar", "estensione file rar", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Che cos'è un'estensione di file RAR e API che possono creare e aprire file RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file RAR?

I file con estensione .rar sono file di archivio creati per archiviare informazioni in forma compressa o normale. RAR, che sta per Roshal ARchive file format, è un formato di file proprietario creato da Eugene Roshal nel 1995, un ingegnere di software russo. Il formato viene utilizzato per archiviare file con metodi diversi, comprese varie tecniche di compressione. Sono disponibili diversi software applicativi per Windows, Linux e MacOS per l'estrazione di file RAR. Il software WinRAR, di RARLab, è l'utilità di archiviazione file shareware (gratuita per 40 giorni) per piattaforma Microsoft Windows; il software è stato portato su Linux (solo come estrattore) dallo stesso Autore, Eugene Roshal.

## Versioni Cronologia del formato file RAR

* v1.3 (originale, non ha la firma "Rar!")
* v1.5
* v2.0 - rilasciato con WinRAR 2.0 e Rar per MS-DOS 2.0
* v2.9 - rilasciato in WinRAR versione 3.00
* v5.0 - supportato da WinRAR 5.0 e versioni successive

## Caratteristiche principali del formato RAR

RAR è sul campo da molto tempo ed è stato uno dei formati di file di archiviazione preferiti. Le caratteristiche principali del formato RAR sono:

**`Rapporto di compressione elevato:`** Superiore rispetto a [ZIP](/it/compression/zip/), paragonabile al formato 7z e zipx.

**`Forte crittografia dei file in base alla progettazione:`** Gli archivi RAR4 crittografati si basano sulla crittografia basata su AES-128 mentre gli archivi RAR5 crittografati si basano sulla crittografia AES-256 con una pianificazione delle chiavi migliorata

**`Funzionalità avanzate di correzione degli errori e recupero dati:`** record di ripristino opzionali durante la creazione dell'archivio

**`File Size:`** Minimo 20 byte e massimo 2^63 byte (8 exabyte di dimensione totale dell'archivio)

**`Archivi RAR multi-volume:`** Possibilità di dividere archivi di grandi dimensioni in diversi file più piccoli per facilitare il trasferimento sulla rete. In tal caso, le estensioni dei file vengono incrementate di 1 per rappresentare i volumi divisi

## Formato file RAR

Le specifiche complete del formato RAR non sono disponibili pubblicamente ed è per questo che i dettagli sul formato non possono essere formulati in modo conciso.

### Layout archivio generale

Il layout generale di un formato di file RAR introdotto nella versione 5.0 è il seguente:

|Formato file
---|
|Modulo autoestraente (opzionale)
|Firma RAR 5.0
|Intestazione crittografia archivio (opzionale)
|Intestazione archivio principale
|Intestazione servizio commenti archivio (facoltativo)
Intestazione del file 1
|Intestazioni di servizio (ACL NTFS, flussi, ecc.) per il file precedente (opzionale)
|...
|Intestazione file N
|Intestazioni di servizio (ACL NTFS, flussi, ecc.) per il file precedente (opzionale)
|Recupero record (facoltativo)
|Fine dell'intestazione dell'archivio

Le informazioni su ciascuna sezione del file RAR sopra menzionata sono disponibili nel documento [Specifiche del formato file RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Archivi RAR autoestraenti

Se il file RAR stesso è autoestraente, le informazioni autoestraenti sono contenute all'inizio del file che precede la firma dell'archivio. La sua dimensione e contenuto non sono definiti.

#### Firma RAR 5.0

La firma RAR è un'intestazione di 8 byte composta dal seguente numero magico:

0x 52 61 72 21 1A 07 00

dove

0x6152 - TESTA_CRC

0x72 - TIPO_TESTA

0x1A21 - HEAD_FLAGS

0x0007 - TESTA_DIMENSIONE

## Riferimenti

* [Formato archivio RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - Di Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))

