{
  "date" : "2019-10-11",
  "keywords" :[ "file tgs", "formato file tgs", "cos'è un file tgs", "file", "esempio tgs", "estensione file tgs", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Formato file adesivo animato Telegram",
  "description":"Scopri il formato di file TGS e le API che possono creare e aprire file TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Che cos'è un file TGS?

Un file con estensione .tgs è un file adesivo animato introdotto dal servizio di messaggistica multipiattaforma [Telegram](https://core.telegram.org/stickers#animated-stickers). Gli adesivi animati vengono utilizzati dagli utenti delle app di messaggistica per inviare contenuti più avanzati e vivaci nei messaggi, a differenza della grafica statica che sono immagini fisse. Telegram inizialmente utilizzava il formato di file [WEBP](/it/image/webp/) per gli adesivi di immagini fisse. Il formato file TGS può memorizzare dati di animazione a risoluzioni più elevate e dimensioni file inferiori rispetto agli adesivi WEBP statici. I file TGS possono essere aperti utilizzando applicazioni come Telegram, 7-zip, Apple Archive Utility e Corel WinZip.

## Formato file TGS

Telegram ha introdotto il formato di file TGS a luglio 2019 basato sulla libreria Lottie. Un file TGS è costituito da testo [JSON](/it/web/json/) esportato da un'animazione in Adobe After Effects. Il testo JSON esportato viene compresso utilizzando la compressione gzip che riduce le dimensioni del file. Le informazioni JSON sul file di testo vengono archiviate in un file di testo che diventa la base di elevati tassi di compressione.

### Specifiche degli adesivi TGS

Il formato file TGS impone alcune limitazioni alla creazione di adesivi animati TGS. Un file animato TGS:

* La dimensione dell'adesivo/tela deve essere di 512x512 pixel.
* Gli oggetti adesivi non devono lasciare la tela.
* La durata dell'animazione non deve superare i 3 secondi.
* Tutte le animazioni devono essere ripetute.
* La dimensione dell'adesivo non deve superare i 64 KB dopo il rendering in Bodymovin.
* Tutte le animazioni devono essere eseguite a 60 fotogrammi al secondo.

### Esempio di testo JSON TGS

Un esempio di adesivo animato, una volta decompresso, contiene il seguente contenuto di testo JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Riferimenti ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

