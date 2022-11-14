{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","file apkg", "formato di file apkg", "tipo di file apkg", "file", "tipo", "Cos'è un file APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Formato file mazzo Anki Flashcard",
  "description" :"Scopri cos'è un file APKG e le API che possono crearli e aprirli.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## Che cos'è un file APKG?

Un file con estensione .apkg è un mazzo di flashcard generato per essere utilizzato nell'applicazione software [Anki](https://ankiweb.net/about) che è un programma di apprendimento basato su flashcard. Contiene testo [HTML](/it/web/html/) da caricare e visualizzare nell'applicazione Anki e può avere inoltre immagini e suoni per l'apprendimento visivo e udibile. Anki consente agli utenti di creare i propri mazzi di flashcard Anki e di importare i mazzi di flashcard di altri utenti.

## Formato file APKG

I mazzi di carte Anki sono creati da modelli scritti in HTML, un linguaggio famoso e comune per la creazione di pagine web. Lo stile delle carte del mazzo viene eseguito utilizzando CSS, che è il linguaggio utilizzato per lo stile delle pagine Web. Lo stile include modifiche a:

* font-family - Il nome del font da utilizzare sulla scheda.
* font-size - La dimensione del carattere in pixel.
* text-align - Definisce se il testo deve essere allineato al centro, a sinistra oa destra.
* colore - Definisce il colore del testo che può essere un semplice nome di colore come "blu", "rosso", ecc. o codici colore HTML.
* background-color - Definisce il colore di sfondo della scheda

Le informazioni sullo stile sono condivise tra tutte le carte, influenzando tutte le carte quando viene apportata una modifica. L'esempio seguente utilizzerà uno sfondo giallo su tutte le carte tranne la prima:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Il ridimensionamento delle immagini in una scheda Anki può essere controllato come segue.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Incorporamento di Javascript nelle carte Anki

È possibile incorporare [Javascript](/it/web/js/) in una scheda Anki utilizzando i modelli di scheda. Tuttavia, a causa del livello avanzato di Javascript, il suo supporto non viene fornito. Inoltre, i dispositivi di rendering possono mostrare gli effetti dell'implementazione di Javascript nella scheda in modo diverso, risultando nella necessità di testare l'implementazione su tutti i dispositivi. Alcune funzionalità Javascript come window.alert, rendono difficile il debug del codice Javascript che hai scritto.

## Riferimenti ##

* [Documentazione Anki](https://docs.ankiweb.net/intro.html)

