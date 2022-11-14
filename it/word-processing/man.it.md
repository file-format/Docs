{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Manuale Unix",
  "description":"Scopri il formato di file FODT e le API che possono creare e aprire file MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Che cos'è un file MAN?

Un file con estensione .man sta per pagina man che è un manuale utente di programmazione Unix sotto forma di documentazione software. Viene utilizzato dall'utilità `Man`, inclusa in Unix, che viene utilizzata per visualizzare la documentazione. La documentazione del software contiene informazioni in sezioni e pagine che possono essere recuperate utilizzando l'utilità Man dal terminale di comando emettendo comandi. Essendo disponibile nel computer come copia cartacea della documentazione, non richiede alcuna copia stampata o connessione a Internet per accedervi.

## Formato file manuale Unix - Ulteriori informazioni

Le pagine man sono memorizzate in formato testo normale e possono essere create e aperte in qualsiasi editor di testo per la visualizzazione o la modifica. In UNIX, le informazioni dalle pagine Man vengono recuperate emettendo comandi dal terminale che includono riferimenti alla sezione e ai numeri di pagina del manuale.

### Sezioni e pagine

Unix man è il manuale di sistema in cui ogni argomento di pagina del comando fa riferimento al nome di un programma, un'utilità o una funzione. il comando, se fornito con le informazioni sulla sezione, cercherà la pagina in quella specifica sezione. Tuttavia, il comportamento predefinito consiste nel cercare la pagina in tutte le sezioni e visualizzare la prima pagina indipendentemente dal fatto che esista in più sezioni.

### Numeri di sezione

Di seguito sono riportate le informazioni sui numeri di sezione del manuale seguiti dai tipi di pagine in essi contenuti.

|Numero sezione|Tipo di pagine|
---|---|
|1|Programmi eseguibili o comandi della shell|
|2|Chiamate di sistema (funzioni fornite dal kernel)|
|3|Chiamate di librerie (funzioni all'interno delle librerie di programmi)|
|4|File speciali (di solito trovati in /dev)|
|5|Formati di file e convenzioni, es. /etc/passwd|
|6|Giochi|
|7|Varie (inclusi pacchetti di macro e convenzioni), ad es. man(7), groff(7)|
|8|Comandi di amministrazione del sistema (solitamente solo per root)|
|9|Routine del kernel [non standard]|

## Esempio - Come leggere le pagine MAN?

Ecco un esempio di come recuperare informazioni sul comando MkDir usando il comando Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Riferimenti

* [Specifiche tecniche di OpenDocument - di Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Pagina manuale di Linux](https://man7.org/linux/man-pages/man1/man.1.html)

