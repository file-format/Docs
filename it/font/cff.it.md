{
  "date" : "2020-08-20",
  "keywords" :[ "file cff", "formato file cff", "cos'è un file cff", "file", "esempio cff", "estensione file cff", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Formato file font compatto",
  "description":"Scopri il formato file CFF e le API per creare e aprire file CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Che cos'è un file CFF?

Un file con estensione .cff è un Compact Font Format ed è anche noto come PostScript Type 1 o CIDFont. CFF funge da contenitore per archiviare più caratteri insieme in un'unica unità nota come FontSet. Il design dei caratteri CFF consente di incorporare codice in linguaggio PostScript che consente ulteriore flessibilità ed estensibilità del formato per l'utilizzo con ambienti di stampa. I file dei font CFF possono essere aperti e convertiti utilizzando API come [Aspose.Font](https://products.aspose.com/font).

## Formato file CFF

I file CFF sono file binari che contengono un layout di dati strutturato, hanno tipi di dati definiti, un'intestazione, un'organizzazione dei glifi e dizionari di tabelle. Maggiori dettagli su questi possono essere trovati nelle [specifiche del formato dei caratteri compatti](https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Disposizione dei dati
Il layout dei dati del formato file CFF è come mostrato di seguito.

|Voce|Commenti|
---|---|
|Intestazione|–|
|NomeINDICE|–|
|INDICE DICT superiore|–|
|INDICE stringa|–|
|INDICE SOTTOSCRITTO Globale|–|
|Codifiche–Charset|–|
|FDSelect|Solo CIDFonts|
|CharStrings INDEX|per-carattere|
|INDICE DICT font|per font, solo font CID|
|DICT privato|per-carattere|
|INDEX Subr locale|per-font o per-DICT privato per CIDFonts|
|Avvisi sui diritti d'autore e sui marchi|–|

### Tipi di dati

I tipi di dati CFF sono mostrati nella tabella seguente.

|Nome|Intervallo|Descrizione|
---|---|---|
|Card8|0 –255|Numero senza segno a 1 byte|
|Card16|0 – 65535|Numero senza segno a 2 byte|
|Offset|varia|Offset di 1, 2, 3 o 4 byte (specificato dal campo OffSize)|
|OffSize|1–4|Il numero senza segno a 1 byte specifica la dimensione di uno o più campi Offset|
|SID|0 – 64999|identificatore di stringa a 2 byte|

### Intestazione

I dati binari iniziano con un'intestazione con il formato mostrato nella tabella seguente.

|Tipo|Nome|Descrizione|
---|---|---|
|Card8|principale|Formatta la versione principale (a partire da 1)|
|Card8|minore|Formatta versione minore (a partire da 0)|
|Card8|HDrSize| Dimensione intestazione (byte)|
|OffSize|offSize|Taglia offset assoluto (0)|

## Riferimenti

* [Tabella del formato dei caratteri compatto](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Formato file CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Set di grafici CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

