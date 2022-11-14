---
date: 2021-07-05
keywords: ssp, .ssp, formato di file ssp, come aprire i file ssp, Scala Server Page
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Formato file delle pagine del server Scala
linktitle: SSP
description: "Scopri cos'è un formato di file SSP e le API che possono creare e aprire file SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Che cos'è un file SSP?

Un file con estensione .ssp è una pagina web creata con il codice Scala per le espressioni invece del semplice HTML. Agisce come uno script lato server utilizzando la combinazione di HTML e Scala. Questi file risiedono sul server e vengono utilizzati per creare pagine Web statiche da servire agli utenti. Scala stesso è un linguaggio di programmazione generico la cui sintassi è familiare agli utenti che hanno lavorato con Velocity, JSP o Erb. I file SSP possono essere analizzati e valutati utilizzando [Scalate](https://scalate.github.io/scalate/) che è un motore di modelli basato su Scala per la generazione di testo e markup.

## Formato file SSP - Ulteriori informazioni

I file SSP vengono salvati in un file di testo normale e possono essere valutati utilizzando Scalate. Un modello Ssp è costituito da testo normale che è più spesso il documento HTML. Dispone di tag Ssp incorporati che fanno sì che i motori di rendering visualizzino in modo dinamico diverse porzioni del documento. I tag iniziano e finiscono con la sequenza <% ... %> e ${ ... } e qualsiasi cosa al di fuori di questi viene considerata come testo letterale.

### Esempio di SSP

L'esempio seguente mostra il codice SSP e il relativo output quando viene eseguito il rendering dal motore di rendering.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
L'output è il seguente.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Riferimenti

- [Riferimento SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

