---
date: 2019-10-11
keywords: css, .css, formato file css, come aprire file css, fogli di stile a cascata
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file CSS
linktitle: CSS
description: "Scopri il formato di file CSS e le API che possono creare e aprire file CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Che cos'è un file CSS? ##

I CSS (Cascading Style Sheets) sono file che descrivono come gli elementi HTML vengono visualizzati sullo schermo, sulla carta, ecc. Con l'HTML, puoi avere stili incorporati o definire gli stili in un foglio di stile esterno. Per incorporare gli stili, il \ <style>\</style> vengono utilizzati i tag. I fogli di stile esterni sono archiviati in file con estensione .css. Con il CSS esterno, puoi includerlo in più pagine HTML per aggiornare lo stile di quelle pagine. Anche un singolo file CSS può essere utilizzato per lo stile di un sito Web completo.

## Breve storia ##

CSS1 è stato rilasciato nel 1996 con Bert Bos come coautore. Il CSS Working Group ha iniziato a lavorare sulle questioni che non erano state affrontate nei CSS1. Ciò ha portato alla creazione di CSS2 nel novembre 1997, che è stato pubblicato come raccomandazione del W3C il 12 maggio 1998. Questa versione ha aggiunto il supporto per dispositivi specifici dei media come stampanti, font scaricabili, tabelle e posizionamento degli elementi. Nel giugno 1999, CSS3 è diventata la raccomandazione del W3C. Questo ha diviso la documentazione in moduli in cui ogni modulo aveva caratteristiche di estensione definite in CSS2.

## Come utilizzare i file CSS ##

Per utilizzare un file CSS, lo includi nella sezione head del documento HTML. Utilizzare il tag di collegamento per includere il file come mostrato di seguito.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

l'attributo *href* del tag link contiene il percorso del file CSS. In questo modo, gli stili applicabili contenuti nel file CSS incluso vengono applicati al documento HTML.

## Sintassi CSS ##

Una regola CSS comprende due componenti, un selettore e una dichiarazione. Un selettore punta a un elemento nel documento HTML. Può essere un tag di elemento, un nome di classe, un nome id, più tag che mostrano la gerarchia, ecc. Una dichiarazione contiene la definizione di stile che comprende proprietà e valore. La proprietà identifica la proprietà dell'elemento che si desidera modificare e il valore ne definisce il nuovo valore. Ogni regola CSS può avere più dichiarazioni. Quello che segue è un esempio di una regola CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Nell'esempio sopra, abbiamo **h1** come selettore che seleziona tutti i tag h1 nel documento HTML. La regola ha due dichiarazioni, una per il peso del carattere e l'altra per il colore. *font-weight* e *color* sono proprietà e *700* e *forestgreen* sono rispettivamente i loro valori.

## Esempio di utilizzo CSS ##

Quanto segue mostra il documento HTML di esempio e il foglio di stile utilizzato per modellarlo. L'immagine di confronto viene aggiunta anche per confrontare i documenti HTML in stile e semplici

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Foglio di stile CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Confronto output ###

Il lato sinistro dell'immagine mostra il documento HTML senza gli stili applicati e il lato destro mostra il documento HTML con gli stili applicati.

{{< figure src="../CssExample.jpg" alt="Esempio di immagine" >}}

## Riferimenti ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

