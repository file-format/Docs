{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file AWK - File script AWK",
  "description":"Scopri il formato di file AWK e le API che possono creare e aprire file AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Che cos'è un file AWK?

Un file AWK è un file di script creato per l'applicazione di elaborazione del testo **AWK** che viene fornita in bundle con i sistemi operativi Unix e Linux. Contiene istruzioni logiche per eseguire azioni sul testo o sul contenuto di un file come la corrispondenza, la sostituzione e la stampa del testo. Questo aiuta a generare report e testo formattato dal file di input. L'utilità awk si trova solitamente in /usr/bin/awk sulla maggior parte delle distribuzioni linux/unix.

## Come creare uno script AWK?

Un file AWK può essere creato o aperto in qualsiasi editor di testo su Linux/Unix OS. Un nuovo file di script AWK può essere creato come segue.

```
$ vi script.awk
```

Questo aprirà il file AWK nell'editor di testo. Immettere alcune affermazioni nell'editor di testo come segue.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
La prima riga di questo contenuto testuale è spiegata come segue.

* \#! – indicato come `Shebang`, che specifica un interprete per le istruzioni in uno script
* /usr/bin/awk – è l'interprete
* -f – opzione interprete, usata per leggere un file di programma

## Come eseguire lo script AWK?

Salva il file e rendi eseguibile lo script eseguendo il comando seguente:
```
$ chmod +x script.awk
```

Lo script può quindi essere eseguito come segue.

```
$ ./script.awk
```

che si traduce nel seguente output.

```
Writing my first Awk executable script!
```

## Riferimento ##

* [Scrivere script utilizzando il linguaggio di programmazione Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

