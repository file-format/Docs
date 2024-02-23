{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File ZST: formato di file compresso Zstandard",
  "description":"Scopri il formato file ZST e le API che possono creare e aprire file ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-it",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Cos'è un file ZST?

Un file ZST è un file compresso generato con l'algoritmo di compressione Zstandard (zstd). È un file compresso creato con compressione senza perdita di dati dall'algoritmo. I file ZST possono essere utilizzati per comprimere diversi tipi di file come database, file system, reti e giochi. Lo Zstandard è governato da [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) che descrive il meccanismo di compressione generale, il tipo di media e la codifica del contenuto.

## Formato file ZST

I file ZST vengono archiviati in formato file compresso su disco. Il meccanismo di compressione è quello descritto dalla RFC 8878 che rende obsoleta la RFC 8478.

## Cornici ZST

Un file ZST è costituito da uno o più fotogrammi. Ogni frame può essere un frame Zstandard o un frame ignorabile. Un frame Zstandard contiene dati compressi, mentre un frame ignorabile contiene metadati utente personalizzati.

### Cornice Zstandard

Un frame Zstandard ha la seguente struttura.

|Campo|Dimensione in byte|
---|---|
|Magic_Number |4 byte|
|Frame_Header |2-14 byte|
|Blocco_dati |n byte|
|[Altri Data_Blocks] ||
|[Contenuto_Checksum] |4 byte|

### Frame ignorabile

Un frame ignorabile consente l'inserimento di metadati definiti dall'utente in un flusso di frame concatenati. La struttura di un frame ignorabile è la seguente.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 byte |4 byte |n byte|

## Riferimenti ##

* [Compressione Zstandard RFC 8878](https://www.rfc-editor.org/rfc/rfc8878)


