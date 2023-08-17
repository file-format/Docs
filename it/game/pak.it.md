{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "formato file", "cos'è un file pak", "file", "esempio pak", "File pacchetto videogiochi", "estensione"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ulteriori informazioni sul file .pak e sulle API che possono creare e aprire file PAK.",
  "title" :"Formato file PAK - File del pacchetto di videogiochi",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Che cos'è un file PAK?

Un file PAK è un file di pacchetto creato da diversi videogiochi per archiviare i dati di gioco. In sostanza, è un formato di file di gioco. Ciò può includere più elementi di gioco come grafica, trame, suoni, oggetti e altri dati di gioco. L'archivio viene salvato principalmente come file .zip e può essere estratto con software di decompressione popolari come WinZip e WinRAR. Esempi di videogiochi che utilizzano file PAK includono Quake, Hexen, Crysis e Half-Life.

## Formato file PAK - Ulteriori informazioni

Nella maggior parte dei casi, i file PAK vengono salvati in [formato file ZIP](/it/compression/zip/). Ma applicazioni diverse possono utilizzare formati di file diversi per archiviare questi file.


## Come aprire i file PAK?

È possibile aprire file PAK con applicazioni come [PakExplorer](https://www.quaketerminus.com/tools.shtml) e [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ------------------------**

## Formato file PAK - File oggetto Simutrans

Un file con estensione .pak è un formato di file di gioco di simulazione di trasporto [Simutrans](https://www.simutrans.com/en/). Contiene oggetti utilizzati nella simulazione come grafici creati dall'utente e contenuti di dati. Può avere diversi oggetti diversi come veicoli di gioco, edifici, terreno, ecc. I file PAK vengono generati utilizzando MakeObject, un'utilità che compila file .dat e immagini .png per creare questi oggetti di simulazione. Simutrans consente ai giocatori di gestire un sistema di trasporto di successo costruendo e gestendo sistemi di trasporto per passeggeri, posta e merci via terra

## Come creare file PAK?

Simutrans ha elencato esempi di esempio per la creazione di file PAK su sistemi operativi Windows e Linux.

### Sistema operativo Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Riferimenti

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)