{
  "date" : "2019-12-09",
  "keywords" :[ "file zl", "formato file zl", "cos'è un file zl", "file", "esempio zl", "estensione file zl", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Formato file compresso ZLIP",
  "description":"Scopri il formato di file ZL e le API che possono creare e aprire file ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Che cos'è un file ZL?

Un file con estensione .zl è un formato di file compresso ZLIP che utilizza una variante dell'algoritmo di compressione DEFLATE per la compressione dei file. È indipendente dal tipo di CPU, dal sistema operativo, dal file system e dal set di caratteri e quindi può essere utilizzato per lo scambio di informazioni. Le specifiche tecniche della compressione ZLIP sono disponibili sul [sito IETF](https://tools.ietf.org/html/rfc1950) e possono essere referenziate dal punto di vista dello sviluppatore.

## Formato file ZL

Un flusso zlib ha la seguente struttura:

* `CMF (Metodo di compressione e flag)` - Questo byte è suddiviso in un metodo di compressione a 4 bit e un campo di informazioni a 4 bit a seconda del metodo di compressione.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Metodo di compressione)` - Identifica il metodo di compressione utilizzato nel file. I suoi valori e il metodo di compressione corrispondente sono i seguenti.

| Valore CM| Compressione|
|---|---|
|CM = 8|DEFLATE con una dimensione della finestra fino a 32K|
|CM = 15|Riservato|

* `CINFO (Informazioni sulla compressione)` - Per CM = 8, CINFO è il logaritmo in base 2 della dimensione della finestra LZ77, meno otto (CINFO=7 indica una dimensione della finestra di 32K).

* `FLG (FLaGs)` - Questo byte di flag è suddiviso come segue:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Riferimenti ##

* [Specifiche del formato file Zlib](https://tools.ietf.org/html/rfc1950)

