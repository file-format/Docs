
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4° file - Formato file della quarta lingua",
  "description":"Scopri cos'è il formato file .4 con esempi e API in grado di creare e aprire file 4.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Cos'è un quarto file?

Un file con estensione .4th è un file di programmazione creato per il **Forth Programming Language**. Contiene il codice sorgente per programmi scritti nel linguaggio di programmazione Forth e genera l'output quando il programma viene eseguito. È semplicemente un altro file del linguaggio di programmazione simile al file sorgente [C](/it/programming/c/) e [C++](/it/programming/cpp/).

## Quarto formato file: ulteriori informazioni


### Quarto esempio di codice del linguaggio di programmazione

Ecco un esempio di un semplice programma scritto in Forth che calcola il fattoriale di un dato numero:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In questo esempio, la parola fattoriale accetta un singolo argomento n e restituisce il suo fattoriale. La parola dup duplica il valore in cima allo stack, drop scarta il valore in cima allo stack e * moltiplica i due valori in cima allo stack. I costrutti if e Begin/until controllano il flusso del programma.

Per utilizzare questo programma, dovresti inserire la definizione nell'interprete Forth, quindi chiamare la parola fattoriale con il numero di cui vuoi trovare il fattoriale:

```
10 factorial .
```
Ciò comporterebbe l'output 3628800, che è il fattoriale di 10.

## Riferimenti

* [Linguaggio di programmazione Forth](https://en.wikipedia.org/wiki/Forth_(programming_lingual))

