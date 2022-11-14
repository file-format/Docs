{
  "date" : "2021-07-29",
  "keywords" :[ "file md5", "formato file md5", "cos'è un file md5", "file", "esempio md5", "estensione file md5", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - File di checksum MD5",
  "description":"Ulteriori informazioni sul file MD5 e sulle API che possono creare e aprire file MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Che cos'è un file MD5?

Un file MD5 è un file di checksum utilizzato per la verifica dell'integrità di un file. È simile a un'impronta digitale per il file associato ed è generata in modo univoco utilizzando un algoritmo che utilizza il numero di bit nel file. Viene utilizzato per verificare il file con software come [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Un vantaggio dell'utilizzo dei file MD5 è verificare che i file scaricati non siano danneggiati.

## Formato file MD5 - Ulteriori informazioni

Solitamente un file MD5 viene salvato con lo stesso nome del file originale ma con estensione .md5. Ad esempio, se il nome del file associato è `abc_987_123456.grb`, il nome del file MD5 corrispondente sarà `abc_987_123456.grb.md5`. I file MD5 consentono di identificare che un file ricevuto o scaricato non è danneggiato o interessato da contenuti dannosi. In breve, i file MD5 garantiscono la completezza di un file.


## Come controllare il checksum MD5?

Un singolo file può essere controllato/verificato per MD5 utilizzando lo strumento [md5sum](https://en.wikipedia.org/wiki/Md5sum) come segue.

```
md5sum -c abc_987_123456.grb.md5
```

## Riferimenti

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

