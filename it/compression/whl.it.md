{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file WHL - File pacchetto Python Wheel",
  "description":"Scopri il formato di file WHL e le API che possono creare e aprire file WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Che cos'è un file WHL?

Un file WHL (Wheel) è un file del pacchetto di distribuzione salvato nel formato ruota di Python. È un'installazione in formato standard delle distribuzioni Python e contiene tutti i file e i metadati necessari per l'installazione. Il file WHL contiene anche informazioni sulle versioni e piattaforme Python supportate da questo file wheel. Simile a un file di installazione [MSI](/it/executable/msi/), il formato di file WHL è un formato pronto per l'installazione che consente di eseguire il pacchetto di installazione senza creare la distribuzione di origine.

## Formato file WHL

Il formato di file WHL è un archivio [ZIP](/it/compression/zip/) (.zip) che contiene tutti i file di installazione e i metadati richiesti dai programmi di installazione per l'installazione di un pacchetto. Questi file WHL possono essere estratti utilizzando l'opzione di decompressione o applicazioni software di decompressione standard come WinZIP e WinRAR.

### Convenzione del nome del file WHL

Un file WHL è denominato secondo la seguente convenzione.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Un esempio del nome del file WHL è il seguente.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `crittografia` è il nome del pacchetto.
* `2.9.2` è la versione del pacchetto della crittografia. Una versione è una stringa conforme a PEP 440 come 2.9.2, 3.4 o 3.9.0.a3.
* `cp35` è il tag Python e denota l'implementazione e la versione Python richiesta dalla ruota.
* `abi3` è il tag ABI. ABI sta per interfaccia binaria dell'applicazione.
* `macosx_10_9_x86_64` è il tag della piattaforma, che sembra essere un boccone.

## Riferimenti

* [Cosa sono le ruote Python e perché dovresti preoccuparti?](https://realpython.com/python-wheels/)
* [Ruota Python](https://pypi.org/project/wheel/)

