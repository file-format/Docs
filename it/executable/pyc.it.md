{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file PYC e le API che possono creare e aprire file PYC.",
  "title" :"Formato file PYC - File compilato Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Che cos'è un file PYC?

Un file PYC è un file di output compilato generato dal codice sorgente scritto nel linguaggio di programmazione Python. Quando il file PY viene eseguito utilizzando l'interprete Python, viene convertito in bytecode per l'esecuzione. Allo stesso tempo, il bytecode compilato viene anche salvato come file .pyc in modo da riutilizzarlo dalla cache in un secondo momento, se applicabile.

## Struttura del formato file PYC

I file PYC sono in bytecode e le loro specifiche di formato file non sono disponibili pubblicamente. Tuttavia, l'indagine di alcune fonti mostra che la [struttura di un file PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) è composto da:

* `A quattro byte magic numbe`r - Semplicemente due byte che cambiano ad ogni modifica al codice di marshalling, e poi due byte di 0d0a.
* `Un timestamp di modifica a quattro byte` - Timestamp di modifica Unix del file sorgente che ha generato .pyc, in modo che possa essere ricompilato se il sorgente cambia.
* `Un oggetto di codice sottoposto a marshalling` - l'output di marshal.dump dell'oggetto di codice che è il risultato della compilazione del file sorgente.

## Riferimenti

* [La struttura dei file .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

