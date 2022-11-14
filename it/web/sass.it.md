---
date: 2019-10-11
keywords: sass, .sass, formato file sass, come aprire file sass, foglio di stile sintatticamente fantastico, preprocessore CSS, sass
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file Sass
linktitle: Sass
description: "Scopri il formato di file Sass e le API che possono creare e aprire file Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Che cos'è un file SASS? ##

Sass (fogli di stile sintatticamente fantastici) è un linguaggio di scripting del preprocessore. Viene compilato in [CSS](/it/web/css/) ed è archiviato con l'estensione .sass. Sass è costituito da due sintassi, l'originale basata su indentazioni che utilizza l'estensione .sass e la più recente SCSS con formattazione a blocchi come CSS che utilizza l'estensione .scss.

## Perché usare Sass ##

Sass è davvero utile nel mantenimento degli stili in quanto fornisce molte funzionalità come l'introduzione di variabili, il nesting, i mixin, le importazioni e l'ereditarietà del selettore che rendono divertente il lavoro con gli stili.

## Come utilizzare i file SASS ##

I file SASS non sono inclusi direttamente nel documento [HTML](/it/web/html/) ma sono piuttosto convertiti in file CSS inclusi nei file HTML. È possibile installare Sass del proprio sistema seguendo le istruzioni fornite sul [Sito Ufficiale Sass](https://sass-lang.com/install).

Sass può essere convertito in CSS convertendo un file SASS già salvato o controllando le modifiche e convertendo mentre il file viene salvato. I comandi per entrambi sono riportati di seguito.

### Converti una volta ###

Il primo parametro del comando è il file SASS di origine e il secondo parametro è il file CSS di output.

```cmd
sass main.sass main.css
```

### Fai attenzione alle modifiche ###

Il comando sopra può essere eseguito con un flag *watch* aggiuntivo che mantiene il comando in esecuzione e non appena il file Sass viene salvato, viene generato il CSS di output.

```cmd
sass --watch main.sass main.css
```

## Sintassi Sass ##

Sass supporta variabili, annidamento, mixin, importazioni, ereditarietà del selettore, ecc. Di seguito sono riportati esempi di queste funzionalità.

### Variabili ###

Le variabili possono essere utilizzate per impostare informazioni riutilizzabili come il colore primario o il riempimento per un pulsante. Questo può rivelarsi utile se in futuro è necessario modificare tali informazioni, basta cambiarle in una posizione e si aggiorna ovunque.

**Sasso**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

I selettori CSS possono essere nidificati in modo simile alla gerarchia dell'HTML. Nell'esempio seguente, l'estensione è nidificata all'interno del blocco h1.

**Sasso**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

I mixin vengono utilizzati per raggruppare proprietà simili che vengono utilizzate in più posizioni. I mixin supportano anche i parametri.

**Sasso**

**Dichiarazione di un mixin**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Usare un mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

Estendi/Ereditarietà può rivelarsi utile nei casi in cui le proprietà di un selettore devono essere condivise con un altro selettore. Nell'esempio seguente, il selettore *.error-notice* prende tutte le proprietà del selettore *.error-text* e aggiunge le proprietà del bordo e del riempimento.

**Sasso**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

L'importazione può essere utile se strutturi i tuoi stili in file diversi in base alla funzionalità o a qualsiasi altra struttura che segui. Puoi importare tutti questi file in un file SASS primario che viene successivamente convertito in CSS. Durante l'importazione, non è necessario specificare l'estensione del file nell'istruzione di importazione. Sass compila direttamente tutti i file SASS. Per evitare che i file di importazione vengano compilati direttamente, puoi renderli parziali aggiungendo underscore(_) all'inizio del loro nome. I parziali vengono importati in modo simile ai normali file Sass.

**Sasso**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Il CSS di output avrà gli stili di tutti i file importati.

## Riferimenti ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

