{
  "date" : "2019-12-10",
  "keywords" :[ "DIF", "file", "estensione", "formato file", "File di scambio dati", "Foglio di calcolo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"La tua guida al formato di file per sapere cos'è un'estensione di file DIF e le API in grado di creare e aprire file DIF.",
  "title" :"DIF - Formato file di scambio dati",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Che cos'è un file DIF?

DIF sta per Data Interchange Format che viene utilizzato per importare/esportare dati di fogli di calcolo tra diverse applicazioni. Questi includono Microsoft Excel, OpenOffice Calc, StarCalc e molti altri. Memorizza i dati contenuti in un unico foglio di calcolo che è l'unica limitazione di questo formato di file.

## Breve storia del formato file DIF ##

Il formato di file DIF è stato sviluppato da Software Arts, Inc. all'inizio degli anni '80. Le specifiche del formato file per DIF sono state incluse in VisiCalc, il primo programma di fogli di calcolo per personal computer. Queste specifiche erano protette da copyright nel 1981 ed erano un marchio registrato di Software Arts Products Corp.

## Formato file DIF ##

DIF memorizza i contenuti del foglio di calcolo in un file di testo ASCII che ne consente la visualizzazione e la modifica con un editor di testo. Il formato occupa il suo posto nell'elenco dei formati di serializzazione dei dati per le sue caratteristiche di scambio di dati. Un file DIF è composto da 2 sezioni; un'intestazione e dati.

Tutto in DIF è rappresentato da un blocco di 2 o 3 righe. Le intestazioni ottengono un blocco di 3 righe; dati, 2.

* I blocchi di intestazione iniziano con un identificatore di testo che è tutto maiuscolo, solo caratteri alfabetici e meno di 32 lettere. La riga successiva deve essere una coppia di numeri e la terza riga deve essere una stringa tra virgolette.
* I blocchi di dati iniziano con una coppia di numeri e la riga successiva è una stringa tra virgolette o una parola chiave.

### I valori ###

Un valore occupa due righe, la prima una coppia di numeri e la seconda una stringa o una parola chiave. Il primo numero della coppia indica il tipo:

* −1 – tipo di direttiva, il secondo numero viene ignorato, la riga seguente è una di queste parole chiave:
** BOT – inizio tupla (inizio riga)
** EOD – fine dei dati
* 0 – tipo numerico, valore è il secondo numero, la riga seguente è una di queste parole chiave:
** V – valido
** NA – non disponibile
** ERRORE – errore
** TRUE – vero valore booleano
** FALSO – valore booleano falso
* 1 – tipo stringa, il secondo numero viene ignorato, la riga seguente è la stringa tra virgolette

### Pezzo di intestazione DIF ###

Il pezzo di intestazione di un file DIF comprende una riga identificativa seguita dalle due righe di un valore. I valori numerici nei blocchi di intestazione utilizzano solo una stringa vuota invece delle parole chiave di validità. I dettagli di questi blocchi di intestazione sono i seguenti.

* TABLE - alla versione segue un valore numerico, la seconda riga inutilizzata del valore contiene un commento del generatore
* VETTORI - il numero di colonne segue come valore numerico
* TUPLE - il numero di righe segue come valore numerico
* DATA - dopo un valore numerico fittizio 0, i dati della tabella seguono, ogni riga preceduta da un valore BOT, l'intera tabella terminata da un valore EOD

### Esempio DIF ###

L'esempio seguente mostra il contenuto di un semplice foglio di lavoro e la sua rappresentazione DIF equivalente.


|Nome|Età
---|---|
|Bob|34
|Foglio|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Riferimenti ##

* [ DIF - Di Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)

