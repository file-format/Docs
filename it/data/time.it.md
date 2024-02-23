{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "File TIME: cos'è il file .time? Ora in cui il file è stato creato in Linux",
  "description" : "Scopri il file TIME e scopri l'ora in cui il file è stato creato in Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-it",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Cos'è un file TIME?

Il formato file TIME è stato utilizzato da un sistema web chiamato LIGHT, che ha aiutato gli utenti a registrare, organizzare e condividere le proprie vite. Essenzialmente, memorizzava una raccolta di post e rappresentava una cartella sulla pagina della vita dell'utente all'interno del sistema.

## Come scoprire quando è stato creato un file in Linux

In Linux, puoi utilizzare il comando `stat` per scoprire quando è stato creato un file. Ecco come puoi farlo:

Apri un terminale e digita il seguente comando:

```
stat <file_path>
```

Sostituisci `<file_path> ` con il percorso del file che ti interessa. Ad esempio:

```
stat /path/to/your/file.txt
```

Questo comando visualizzerà varie informazioni sul file, inclusa l'ora di creazione. Cerca la riga che inizia con Nascita o File:. L'ora di Nascita indica quando il file è stato creato sul filesystem.

Ecco un esempio di come potrebbe apparire l'output:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

In questo esempio, l'ora di Nascita indica quando è stato creato il file.

