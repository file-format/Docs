{
  "date" : "2021-04-08",
  "keywords" :[ "file lz4", "formato file lz4", "cos'è un file lz4", "file", "esempio lz4", "estensione file lz4", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - Formato file compresso LZ4",
  "description":"Scopri il formato di file LBR e le API che possono creare e aprire file LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Che cos'è un file LZ4?

Un file con estensione .lz4 è un file di archivio compresso creato con applicazioni/utilità che supportano la compressione [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). L'algoritmo LZ4 si concentra sul compromesso tra velocità e rapporto di compressione. Gli archivi LZ4 compressi possono essere creati utilizzando l'utilità della riga di comando LZ4 e possono essere decompressi utilizzando la stessa.

## Formato file LZ4

Il formato file LZ4, basato sull'algoritmo di compressione LZ4, è indipendente dal tipo di CPU, dal sistema operativo, dal file system e dal set di caratteri. È adatto per la compressione di file e la compressione in streaming utilizzando l'algoritmo LZ4. L'implementazione iniziale del formato LZ4 è stata eseguita nel linguaggio [C](/it/programming/c/) da Yann Collet nel 2011 ed è disponibile come riferimento per gli sviluppatori su [Github](https://github.com/lz4/lz4) .

### Formato cornice LZ4

La struttura generale del formato di file LZ4 è quella mostrata di seguito.

|Magia Nb|F. Descrittore| Blocco|(...)|Segno di Fine |C. somma di controllo|
---|---|---|---|---|---|
|4 byte| 3-15 byte||| 4 byte| 0-4 byte|

#### Numero magico

4 byte, formato Little Endian. Valore: 0x184D2204

#### Descrittore di frame

Il descrittore di frame è composto da 3 t0 15 byte ed è la parte più importante delle specifiche. Insieme, i campi Magic_Number e Frame_Descriptor sono indicati come LZ4 Frame Header e la sua dimensione varia tra 7 e 19 byte. È come mostrato di seguito.

|FLG| BD| (dimensione del contenuto)| (ID dizionario)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 byte| 0 - 4 byte| 1 byte|

#### Blocchi di dati

Ciascun blocco di dati segue il seguente ordine.

|Dimensione blocco| dati| (Blocca checksum)|
---|---|---|
|4 byte| |0 - 4 byte|

#### Fine

Il flusso di blocchi termina quando l'ultimo blocco di dati è seguito dal valore a 32 bit 0x00000000.

#### Checksum del contenuto

Il Content_Checksum verifica la validità del contenuto decodificato correttamente e viene eseguito utilizzando il risultato dell'algoritmo xxHash-32. Convalida i risultati della trasmissione riuscita di tutti i blocchi nell'ordine corretto e senza alcun errore.

## Riferimenti

* [Formato frame LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algoritmo di compressione LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

