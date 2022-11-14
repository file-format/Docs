{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - File del pacchetto di installazione multipiattaforma",
  "description":"Scopri il formato di file XPI e le API che possono creare e aprire file XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Che cos'è un file XPI?

Un file XPI è un archivio di installazione compresso per ridurre le dimensioni del file. Viene utilizzato dalle applicazioni Mozilla per l'installazione di plugin e file aggiuntivi. Contiene uno script di installazione o un manifest nella radice del file insieme a una serie di file di dati. Un file XPI può contenere temi, toolkit o plugin di Firefox che l'utente può installare per diventare parte del browser Firefox, Thunderbird o SeaMonkey.

## Formato file XPI - Ulteriori informazioni

I file XPI vengono salvati su disco come archivi [ZIP](/it/compression/zip/) che combinano più file in un unico file compresso. I file all'interno di un file XPI possono includere file di script di installazione come JS e file Web come [CSS](/it/web/css/), [HTML](/it/web/html/) e [JSON](/it/web/json/ ). A volte, può contenere anche file di immagine [PNG](/it/image/png/) da utilizzare come icone per il componente aggiuntivo.

### Come visualizzare il contenuto del file XPI?

Un file XPI è praticamente un archivio ZIP il cui contenuto può essere visualizzato utilizzando i seguenti passaggi.

* Modificare l'estensione del file da XPI a ZIP
* Estrai il contenuto del file utilizzando qualsiasi utilità di decompressione standard come WinZip (Windows, Mac), 7-Zip (Windows) o Apple Archive Utility (Mac).

### Installa il file XPI su Firefox Android

Per lo più le persone sono curiose di sapere se i file XPI possono essere installati in Firefox su dispositivi Android. Su Android, puoi installare il componente aggiuntivo da un file XPI individuando il file e aprendolo con Firefox.

## Riferimenti

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Come posso aprire un'estensione file XPI?](https://support.mozilla.org/en-US/questions/1009049)

