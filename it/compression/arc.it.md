---
date: 2019-12-09
keywords: arc, .arc, formato file arco, come aprire file arco, estensione .arc, estensione arco
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file ARC
linktitle: ARC
description: "Scopri il formato di file ARC e le API che possono creare e aprire file ARC."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## Che cos'è un file ARC?

ARC è un formato di archiviazione e compressione dati senza perdita sviluppato da System Enhancement Associates (SEA). Il formato del file e l'applicazione che lo crea sono entrambi chiamati ARC. ARC era molto popolare durante i primi giorni del BBS dial-up in quanto combinava le funzionalità di compressione e archiviazione di più file nello stesso file. ARC è stato successivamente sostituito da [ZIP](/it/compression/zip/) che offriva rapporti di compressione migliori.

L'estensione del file .arc viene utilizzata da molti altri tipi di file di archivio non correlati come il formato ARC utilizzato da Internet Archive per archiviare più risorse Web, un formato ARC diverso utilizzato dall'archiviatore FreeArc, un formato diverso utilizzato da Nintendo per le risorse, ecc. .

## Breve storia del formato file ARC

Il programma ARC è stato scritto da Thom Henderson di System Enhancement Associates nel 1985. Questo programma raggruppava i file in un unico file di archivio e li comprimeva. I file generati dal programma ARC utilizzavano l'estensione .arc. SEA ha rilasciato il codice sorgente per ARC nel 1986 e ARC è stato portato su Unix e Atari ST da Howard Chu nel 1987.

Phil Katz ha sviluppato PKARC e PKXARC per l'archiviazione e l'estrazione di file. I file funzionavano con il formato di file ARC ed erano significativamente più veloci. A differenza di ARC, Katz ha diviso le funzioni di compressione e archiviazione tra due file diversi, riducendo il fabbisogno di memoria per eseguirli.

Dopo la causa tra SEA e Katz, SEA si è ritirata dal mercato shareware e ha sviluppato ARC+Plus con un'interfaccia utente a schermo intero. Il formato ARC non è più comune su PC.

## Formato file ARC

Il file ARC è costituito da una sequenza di intestazione e file di file seguiti dall'indicatore di fine archivio, come mostrato di seguito.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### Intestazione del file ARC ###

|Offset|Etichetta|Tipo|Valore|Descrizione|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|Metodo|
|02|ARCFNT|DS|12|nome file|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|Dimensione compressa|
|13|ARCDAT|DW|0000|Data file (MSDOS)|
|15|ARCTIM|DW|0000|Ora del file (MSDOS)|
|17|ARCCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|Dimensione non compressa|
|1D|ARCFIL|DS|ARCNSZ| |

### Metodi di compressione ###

Il byte del metodo di compressione indica il metodo di compressione utilizzato. Di seguito sono riportati i metodi di compressione utilizzati per il file ARC.

|Metodo|Nome|Descrizione|
|---|---|---|
|0|Memorizzata|Nessuna compressione utilizzata|
|1|Imballato|Codifica della lunghezza di esecuzione ripetuta (RLE)|
|2|Spremuto|Codifica di Huffman|
|3|Crunched|LZW con buffer 4K, codici a 12 bit|
|4|Crunched|Prima impacchettamento, poi buffer LZW 4K con 12 bit|
|5|Crunched|Imballaggio, LZW, buffer 4K, lunghezza variabile (9-12 bit)|
|6|Schiacciato|LZW, buffer 8K, lunghezza variabile (9-13 bit)|
|7|Crushed|Imballaggio, quindi buffer LZW 8K, 2-13 bit (PAK 1.0)|
|8|Distillare|Huffman dinamico con buffer 8K (PAK 2.0)|

## Riferimenti

- [ARC (formato file) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

