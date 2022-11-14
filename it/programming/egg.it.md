{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file EGG - File di distribuzione Python",
  "description":"Scopri il formato di file EGG e le API che possono creare e aprire file EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Che cos'è un file EGG?

Un file EGG, noto anche come Python eggs, è un formato di distribuzione Python precedente. È un archivio compresso [ZIP](/it/compression/zip/) con estensione .egg e contiene i file sorgente dell'applicazione Python insieme a meta informazioni sulla distribuzione. I file EGG sono un'alternativa a un file eseguibile di Windows [EXE](/it/executable/exe/) ma è multipiattaforma. Questo vecchio formato per le distribuzioni Python è stato sostituito con il nuovo formato di file Wheel (WHL) all'inizio del 2010.

## Formato file UOVO

I file EGG vengono salvati come archivi ZIP compressi. Significa che se sostituisci l'estensione .egg con .zip, sarai in grado di aprirla con utilità di decompressione standard come Corel WinZIP, Microsoft Explorer o RARLAB WinRAR.

I file EGG possono essere creati utilizzando il pacchetto **distutils** disponibile da Python. Un altro strumento in grado di creare e aprire file EGG è **SetupTools**. I file EGG possono essere installati come pacchetto utilizzando **easy_install**.

`NOTA - Il formato file EGG è stato obsoleto a favore del nuovo formato file WHL della ruota.`

## Riferimento ##

* [UOVA Python](https://python101.pythonlibrary.org/chapter38_eggs.html)

