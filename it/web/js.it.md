---
date: 2019-10-11
keywords: js, .js, formato di file js, come aprire file js, file javascript
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file JS
linktitle: JS
description: "Scopri il formato di file JS e le API che possono creare e aprire file JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Che cos'è un file JS? ##

JS (JavaScript) sono file che contengono codice JavaScript per l'esecuzione su pagine web. I file JavaScript vengono archiviati con l'estensione .js. All'interno del documento [HTML](/it/web/html/), puoi incorporare il codice JavaScript usando \ <script>\</script> tag o includere un file JS. Simile ai file [CSS](/it/web/css/), i file JS possono essere inclusi in più documenti HTML per il riutilizzo del codice. JavaScript può essere utilizzato per manipolare il DOM HTML.

## Breve storia ##

JavaScript è stato distribuito per la prima volta come parte del Navigator Browser nel settembre 1995 con il nome LiveScript da Netscape. È stato ribattezzato JavaScript tre mesi dopo. Nel 1996, Microsoft ha decodificato l'interprete di Navigator per creare JScript. JScript è stato rilasciato con Internet Explorer ed era molto diverso da JavaScript.

Netscape ha inviato JavaScript a ECMA International che ha portato al rilascio ufficiale della prima specifica ECMAScript nel 1997. ECMAScript 2 è stato rilasciato nel 1998, ECMAScript 3 nel 1999 e il lavoro su ECMAScript 4 è iniziato nel 2000 ma non è mai stato portato a termine.

Jesse James Garrett nel 2005 ha pubblicato un white paper in cui ha coniato il termine *Ajax*. Questo utilizzava JavaScript come spina dorsale per creare applicazioni Web che caricavano dati in background ed evitavano ricaricamenti di pagine intere. Ciò ha portato alla creazione di librerie come JQuery, Prototype, Dojo, ecc.

Google ha rilasciato il browser Chrome con il motore JavaScript V8 nel 2008. All'inizio del 2009 è stato stipulato un accordo per combinare tutto il lavoro pertinente e portare avanti JavaScript. Ciò ha portato al rilascio dello standard ECMAScript 5 nel dicembre 2009.

## Come usare i file JS ##

Per utilizzare un file JS, includerlo nel documento HTML. Utilizzare il tag di collegamento per includere il file come mostrato di seguito.

```html
<script src="site.js"></script>
```

L'attributo *src* del tag *script* contiene il percorso del file JS. In questo modo, la funzionalità JS viene aggiunta al documento HTML.

## Sintassi JS ##

I file JavaScript possono contenere variabili, operatori, funzioni, condizioni, cicli, array, oggetti, ecc. Di seguito viene fornita una breve panoramica della sintassi di JavaScript.

- Ogni comando termina con un punto e virgola(;).
- Utilizzare la parola chiave *var* per dichiarare le variabili.
- Supporta gli operatori aritmetici (+ - * / ) per calcolare i valori.
- I commenti a riga singola vengono aggiunti con // e i commenti a più righe sono circondati da /* e */.
- Tutti gli identificatori fanno distinzione tra maiuscole e minuscole, ovvero *modelNo* e *modelno* sono due variabili diverse.
- Le funzioni sono definite utilizzando la parola chiave *function*.
- Gli array possono essere definiti utilizzando parentesi quadre [].
- JS supporta operatori di confronto come ==, != , >=, !==, ecc.
- Le classi possono essere definite usando la parola chiave *class*.

## Esempio di utilizzo JS ##

Di seguito viene mostrato un semplice file JavaScript di esempio di utilizzo.

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Codice JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Riferimenti ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

