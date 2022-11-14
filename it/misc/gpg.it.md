{
  "date" : "2022-02-17",
  "keywords" :["file gpg", "formato file gpg", "cos'è un file gpg", "file", "esempio gpg", "estensione file gpg", "estensione", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File GPG - File portachiavi pubblico GNU Privacy Guard",
  "description":"Ulteriori informazioni sul file GPG e sulle API che possono creare e aprire file GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Che cos'è un file GPG?

Un file GPG è un file di chiave di crittografia/decrittografia utilizzato dal programma di crittografia GNU Privacy Guard (GnuPG). Il programma GnuPC stesso è basato sullo standard OpenPGP come definito RFC4880 ed è anche noto come PGP. La chiave per l'utilizzo di successo di GPG nel moderno sistema operativo è il suo versatile sistema di gestione delle chiavi. L'utilità della riga di comando di GPG consente di integrarsi facilmente con altre applicazioni.

## Formato file GPG

I file GPG vengono salvati come file binari crittografati e ovviamente non sono leggibili dall'uomo. Per decrittografare un file GPG crittografato, è necessario utilizzare la stessa chiave di sicurezza. Ed è per questo che il formato del file interno di questi file non è noto.

## Crittografa e decrittografa i file con GPG su Linux

L'utilità della riga di comando GPG può essere utilizzata per crittografare e decrittografare file su Linux.

### Crittografia di un file

Un file può essere crittografato utilizzando il comando gpg con l'opzione -c (create) come mostrato di seguito.

```
gpg -c file1.txt
```
L'esecuzione di questo comando richiede una frase chiave con cui crittografare il contenuto del file originale `file1.txt`. Ciò comporta la creazione del file crittografato file1.txt.gpg.

### Decrittografia ed estrazione di un file

Per decrittografare ed estrarre un file crittografato, è possibile utilizzare il comando seguente.

```
gpg cfile.txt.gpg
```

## Riferimenti

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

