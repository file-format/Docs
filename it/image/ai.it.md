{
  "date" : "2021-01-21",
  "keywords" :[ "file ai", "formato file ai", "che cos'è un file ai", "file", "esempio ai", "estensione file ai", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - File grafico di Adobe Illustrator",
  "description":"Scopri il formato di file AI e le API che possono creare e aprire file AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Che cos'è un file AI?

Un file con estensione .ai è un file Adobe Illustrator Artwork che contiene grafica vettoriale in una singola pagina. utilizza i punti per creare percorsi per la visualizzazione dei dati dell'immagine, evitando così di perdere la qualità dell'immagine se viene ingrandita. Il formato file AI è di base sul formato file PGF che è simile ai file AI. Il formato AI trova il suo principale utilizzo per loghi e supporti di stampa e le sue versioni iniziali erano considerate simili a quelle dei file [EPS](/it/image/eps/). I file AI possono essere aperti con gli strumenti di Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro e CorelDraw Graphics.

## Formato file AI

AI è il formato di file proprietario di Adobe Illustrator e utilizza l'approccio a doppio percorso simile a PGF per il salvataggio di file compatibili con EPS. Le [Specifiche del formato file di Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) forniscono informazioni dettagliate riferimento dello sviluppatore per i dettagli interni di questo formato di file. Tutti I documenti (file) creati da Adobe Illustrator sono documenti in linguaggio PostScript e hanno due parti principali conformi alle Convenzioni di Strutturazione del Documento: un `prologo` e uno `script`.

### Prologo

La sezione prologo incapsula le informazioni richieste per l'interpretazione del file. Un esempio potrebbe essere il riquadro di delimitazione che contiene tutti i segni sulla pagina. Contiene anche informazioni sulle risorse come font e definizioni di procedure. Queste risorse sono raggruppate logicamente in insiemi chiamati procset e contengono metodi espliciti per inizializzare e terminare le loro procedure.

### Sceneggiatura

Gli elementi grafici sulla pagina sono descritti dallo script. Uno script contiene riferimenti agli operatori e alle procedure nel prologo, insieme a operandi e dati. Le tre sezioni logiche di uno script includono:

* Sequenza di installazione - che inizializza e attiva le risorse definite nel prologo
* Sequenza di operatori descrittivi
* Trailer che disattiva le risorse

Gli operatori nello script sono sequenze di elementi grafici scritti nel linguaggio definito dai procset nel prologo. Queste sequenze consistono in raccolte di elementi di dati, definizioni di attributi grafici e chiamate alle procedure definite nei procset.

### Tag oggetto

I tag oggetto vengono utilizzati per allegare informazioni personalizzate a un oggetto artistico di Adobe Illustrator. I tag sono costituiti da:

* Identificatore di tag
* Tipo di etichetta
* Dati

## Riferimenti
* [Specifiche del formato file di Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Formato file AI di PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

