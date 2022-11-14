{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - File di script della shell Bash",
  "description":"Scopri il formato di file SH e le API che possono creare e aprire file SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Che cos'è un file SH?

Un file con estensione .sh è un file di comandi del linguaggio di scripting che contiene un programma per computer che deve essere eseguito dalla shell Unix. Può contenere una serie di comandi che vengono eseguiti in sequenza per eseguire operazioni come l'elaborazione di file, l'esecuzione di programmi e altre attività simili. Questi vengono eseguiti dall'interfaccia della riga di comando dall'utente o in batch per eseguire più operazioni contemporaneamente. I file di script possono essere aperti in editor di testo come Notepad, Notepad++, Vim, Apple Terminal e altre applicazioni simili su Windows, MacOS e Linux OS.

## Formato file SH

I file SH vengono scritti in testo normale seguendo la sintassi definita. Questi file di script supportano:

* `Commenti` - I commenti iniziano con un # e vengono ignorati dalla shell.
* `Scorciatoie` - Questi possono essere usati per rinominare un comando per un'esecuzione breve e facile.
* `Lavori in batch` - È possibile eseguire automaticamente diversi comandi che altrimenti dovrebbero essere inseriti manualmente. Ciò elimina la necessità di attendere che un utente attivi ogni fase della sequenza.
* `Generalizzazione` - Usando semplici loop, si ottiene una generalizzazione molto maggiore per operazioni come la conversione di immagini da un luogo all'altro.

## Esempio di file SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Come eseguire il file SH?
I file SH di solito vengono eseguiti su Linux, anche in Windows è necessario connettersi con un terminale Linux utilizzando software come Putty per eseguire i file sh. Di seguito sono riportati i passaggi per eseguire un file SH su un terminale Linux.

1. Apri il terminale Linux e vai alla directory in cui si trova il file SH.
2. Usando il comando `chmod`, imposta il permesso di esecuzione sul tuo script (se non è già impostato).
3. Eseguire lo script utilizzando uno dei seguenti
1. `./nomefile.sh`
2. `sh nomefile.sh`
3. `bash nome-script-qui.sh`

## Riferimenti

* [Bashscripting per principianti](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

