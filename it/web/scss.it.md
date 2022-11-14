---
date: 2019-10-11
keywords: scss, .scss, formato file scss, come aprire file scss, foglio di stile sintatticamente fantastico, preprocessore CSS, sass
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file SCSS - Foglio di stile a cascata Sass
linktitle: SCSS
description: "Scopri il formato di file SCSS e le API che possono creare e aprire file SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Che cos'è un file SCSS? ##

SCSS è la seconda sintassi di Sass (Syntacttically Awesome Stylesheet) che utilizza parentesi invece di rientri. SCSS è stato progettato in modo tale che un file CSS3 valido sia anche un file SCSS valido. I file SCSS vengono archiviati con l'estensione .scss.

## Perché usare SCSS ##

Poiché i design dei siti Web stanno diventando complessi, risultando in file [CSS](/it/web/css/) di grandi dimensioni. Tali file sono più difficili da mantenere. È qui che entra in gioco SCSS. SCSS introduce variabili, annidamento, mixin, importazioni e ereditarietà del selettore nello sviluppo CSS. Queste aggiunte rendono il lavoro con il design molto più divertente.

## Come utilizzare i file SCSS ##

I file SCSS non sono inclusi direttamente nel documento [HTML](/it/web/html/) come CSS. Al contrario, i file SCSS vengono convertiti in file CSS inclusi nei file HTML. Per installare SCSS sul tuo sistema, segui le istruzioni fornite sul [Sito ufficiale Sass](https://sass-lang.com/install).
Per convertire SCSS in CSS, puoi convertire un file SCSS già salvato o guardare le modifiche e convertire mentre il file viene salvato. I comandi per entrambi sono riportati di seguito.

### Converti una volta ###

Il primo parametro è il file SCSS di origine e il secondo parametro è il file CSS di output.

```cmd
sass main.scss main.css
```

### Fai attenzione alle modifiche ###

Il comando ha un flag aggiuntivo *watch** che mantiene il comando in esecuzione e non appena il file SCSS viene salvato, viene generato il CSS di output.

```cmd
sass --watch main.scss main.css
```

## Sintassi SCSS ##

SCSS supporta variabili, annidamento, mixin, importazioni, ereditarietà del selettore, ecc. Di seguito sono riportati esempi di queste funzionalità.

### Variabili ###

Utilizzando le variabili, puoi impostare informazioni riutilizzabili come il colore primario o il colore di sfondo per il pulsante di salvataggio. Questo è utile se è necessario modificare tali informazioni, basta modificarle in una posizione e si aggiorna ovunque venga utilizzato.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS generato**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Nidificazione ###

Puoi annidare i selettori CSS in modo simile alla gerarchia dell'HTML. Nell'esempio riportato di seguito, la campata è nidificata all'interno del blocco h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**CSS generato**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Mixin ###

I mixin possono essere utilizzati per raggruppare proprietà simili che vengono utilizzate insieme in più posizioni. Puoi anche passare i parametri ai mixin.

**SCSS**

**Dichiarazione di un mixin**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Usare un mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**CSS generato**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Estendi ###

Estendi/Ereditarietà è utile nei casi in cui le proprietà di un selettore devono essere condivise con un altro selettore. Nell'esempio seguente, il selettore *.error-notice* prende tutte le proprietà del selettore *.error-text* e aggiunge le proprietà del bordo e del riempimento.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**CSS generato**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Importa ###

L'importazione può essere utile nella separazione delle preoccupazioni. Puoi dividere gli stili in modo tale che gli stili di intestazione siano in un file separato, gli stili del piè di pagina siano in un file separato, tutte le variabili di colore utilizzate negli stili possano essere in un file separato, ecc. Usando questa tecnica, il gli stili rimangono organizzati. Importa semplicemente i file nel tuo file SCSS principale come mostrato nell'esempio seguente. Non è necessario specificare l'estensione del file nell'istruzione di importazione. Sass compila direttamente tutti i file SCSS. Per evitare che i file di importazione vengano compilati direttamente, puoi renderli parziali aggiungendo underscore(_) prima del loro nome. Puoi importare parziali simili ai normali file SCSS senza il carattere di sottolineatura.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Il CSS di output avrà gli stili di tutti i file importati.

## Riferimenti ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

