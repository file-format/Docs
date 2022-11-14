{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "file", "formato file", "Lingua descrizione pagina", "Scalare" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file SVG e le API che possono creare e aprire file SVG.",
  "title" :"Cos'è un file SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Che cos'è un file SVG? ##

Un file SVG è un file di grafica vettoriale scalare che utilizza un formato di testo basato su XML per descrivere l'aspetto di un'immagine. La parola Scalable si riferisce al fatto che l'SVG può essere ridimensionato a diverse dimensioni senza perdere la qualità. La descrizione testuale di tali file li rende indipendenti dalla risoluzione. È uno dei formati più utilizzati per la creazione di un sito Web e la stampa grafica al fine di ottenere scalabilità. Tuttavia, il formato può essere utilizzato solo per la grafica bidimensionale. I file SVG possono essere visualizzati/aperti in quasi tutti i browser moderni, inclusi Chrome, Internet Explorer, Firefox e Safari.

## Breve storia ##

Le specifiche SVG sono disponibili come standard aperto dal World Wide Web Consortium (W3C) dal 1999. Prima di questo, specifiche di formato di file simili in sei diversi formati sono state inviate al W3C fino al 1998. Un aggiornamento è stato applicato alle specifiche nel 2011 ed è stato aggiornato alla versione 1.1 . Nel 2016, SVG 2 è stato pubblicato come versione più recente includendo funzionalità in aggiunta a quelle in SVG 1.1.

## Specifiche del formato file ##

L'SVG Document Object Model (DOM) pone le basi per tutte le specifiche e le interfacce che corrispondono alle sezioni particolari delle specifiche. I visualizzatori SVG devono implementare le interfacce SVG DOM come definito nelle specifiche W3C. Il suo DOM espone diverse interfacce per diversi tipi di dati ed elementi.

### Forme SVG ###

SVG ha alcuni elementi di forma predefiniti che possono essere utilizzati dagli sviluppatori:

* Rettangolo<rect>
* Cerchio<circle>
* Ellisse<ellipse>
* Linea<line>
* Polilinea<polyline>
* Poligono<polygon>
* Sentiero<path>

Sulla base di queste forme e specifiche, le aree funzionali di SVG sono le seguenti.

**Percorsi** - I percorsi vengono utilizzati per rappresentare contorni di forme semplici e composti. I codici vengono utilizzati per definire la natura dell'operazione. Ad esempio, M viene utilizzato per Sposta a, L viene utilizzato per Linea a, Z viene utilizzato per chiudere un percorso e così via.

**Forme di base** - È possibile disegnare percorsi rettilinei e percorsi costituiti da una serie di segmenti di linea retta collegati (polilinee), nonché poligoni chiusi, cerchi ed ellissi. Anche i rettangoli e i rettangoli con angoli arrotondati sono elementi standard.

**Testo** - La rappresentazione del testo è espressa come dati di caratteri XML in cui è possibile applicare molti effetti visivi al testo. Le specifiche consentono di gestire testo bidirezionale, testo verticale e caratteri lungo un percorso curvo.

**Pittura** - Le forme possono essere riempite e/o delineate con un colore, una sfumatura o un motivo, consentendo la possibilità di renderle opache o avere qualsiasi grado di trasparenza. Gli elementi di fine linea come le punte di freccia oi simboli che appaiono ai vertici di un poligono sono rappresentati da Marker.

**Colore** - Le specifiche SVG consentono di applicare i colori a tutti gli elementi SVG visibili, direttamente o tramite riempimento, tratto e altre proprietà. È possibile utilizzare diversi codici colore per specificare come nero o blu, rappresentazione esadecimale, decimale o come percentuali della forma RGB.

**Sfumature e motivi** - Le forme in un file SVG possono essere riempite o delineate con colori a tinta unita, sfumature o motivi ripetuti.

**Effetti filtro** - Si tratta in realtà di una serie di operazioni grafiche che vengono applicate a una determinata grafica vettoriale di origine per produrre un risultato modificato.

**Interattività** - Gli utenti possono interagire con i file SVG modificando la messa a fuoco, i clic del mouse, lo scorrimento o lo zoom dell'immagine. L'interattività consente alle immagini SVG di interagire con gli utenti in molti modi diversi, come sopra menzionato.

**Collegamento** - È possibile che le immagini SVG abbiano collegamenti ipertestuali ad altri documenti. Ciò si ottiene tramite XML Linking Language o XLink. Ciò consente di creare stati di visualizzazione specifici che vengono utilizzati per ingrandire/ridurre un'area specifica o per limitare la visualizzazione a un elemento specifico.

**Scripting** - Simile all'HTML, tutti gli aspetti di un documento SVG sono accessibili per la manipolazione tramite script. Gli oggetti SVG DOM forniscono la guida per raggiungere questo obiettivo utilizzando l'elemento e l'attributo SVG. Gli script sono racchiusi negli elementi di tag `script` e possono essere eseguiti in risposta a eventi di puntatore, tastiera o documento come richiesto.

**Animazione** - Gli elementi DOM<animate> ,<animateMotion> e<animateColor> ti consente di includere l'animazione per i contenuti SVG. Naturalmente, questo non è realizzabile senza l'utilizzo di script e timer integrati. Queste animazioni possono essere continue e possono essere messe in loop e ripetute mentre allo stesso tempo rispondono agli eventi dell'utente.

**Caratteri** - Il testo in SVG può fare riferimento a file di caratteri esterni come i caratteri di sistema. In assenza di tali caratteri, il testo in SVG non verrà visualizzato nell'output. Questo può essere superato incorporando i glifi richiesti in un file come un carattere che viene quindi renderizzato utilizzando il file<text> elemento.

## Esempi ##
Le righe seguenti mostrano come viene rappresentato un cerchio utilizzando lo script SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Le seguenti righe di codice mostrano come utilizzare il<text> blocco per il rendering del testo in SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Riferimenti ##

* [Specifiche SVG W3C](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

