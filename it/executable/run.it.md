{
  "date" : "2023-01-31",
  "keywords" :["file di esecuzione", "cos'è un file di esecuzione", "file", "come aprire il file di esecuzione", "estensione del file di esecuzione", "estensione"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Informazioni sul formato file RUN e sulle API che possono creare e aprire file RUN.",
  "title" :"Formato file RUN - File eseguibile Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Cos'è un file RUN?

Il formato file .run viene comunemente utilizzato per la distribuzione di software o programmi di installazione di applicazioni nell'ambiente Linux. Per installare il software, sarà necessario rendere eseguibile il file, operazione che può essere eseguita utilizzando il seguente comando:

```bash
chmod +x file_name.run 
```

Quindi, puoi eseguire il file utilizzando il seguente comando:

```bash
./file_name.run 
```

Il processo di installazione può variare a seconda del file e del programma specifici che stai tentando di installare.

Il formato file .run è un tipo di script shell utilizzato per distribuire software o programmi di installazione di applicazioni nell'ambiente Linux. È un pacchetto autonomo che include tutto il necessario per installare il software, inclusi file binari, librerie e file di configurazione.

È importante notare che i file .run possono contenere anche codice dannoso, quindi è sempre una buona idea verificare l'origine del file ed eseguirne la scansione antivirus prima di eseguirlo.

Inoltre, alcuni file .run potrebbero richiedere i privilegi di root per essere eseguiti e installati, quindi potrebbe essere necessario utilizzare il comando "sudo" per eseguire il file con autorizzazioni elevate:

```bash
sudo ./filename.run
```

## Come aprire il file RUN?

Per aprire un file .run è necessario renderlo eseguibile, cosa che può essere fatta con il comando "chmod":

```bash
chmod +x filename.run 
```

Una volta reso eseguibile il file, è possibile eseguirlo digitando:

```bash
./filename.run
```

Eseguire un file .run non equivale ad aprirlo in un editor di testo. L'esecuzione di un file .run eseguirà le sue istruzioni, che potrebbero essere qualsiasi cosa, dall'installazione di un programma all'esecuzione di uno script. Per visualizzare il contenuto di un file .run, è necessario aprirlo in un editor di testo, come nano o vim:

```
nano filename.run
```
O
```
vim filename.run
```

## Riferimenti
* [Come eseguire file .bin e .run in Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


