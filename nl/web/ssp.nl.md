---
date: 2021-07-05
keywords: ssp, .ssp, ssp-bestandsindeling, hoe ssp-bestanden te openen, Scala Server Page
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages-bestandsindeling
linktitle: SSP
description: "Meer informatie over wat een SSP-bestandsindeling is en API's die SSP-bestanden kunnen maken en openen."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Wat is een SSP-bestand?

Een bestand met de extensie .ssp is een webpagina die is gemaakt met Scala-code voor expressies in plaats van alleen HTML. Het fungeert als een server-side script met behulp van de combinatie van HTML en Scala. Deze bestanden bevinden zich op de server en worden gebruikt om statische webpagina's te maken die aan gebruikers worden aangeboden. Scala zelf is een programmeertaal voor algemene doeleinden waarvan de syntaxis bekend is bij gebruikers die met Velocity, JSP of Erb hebben gewerkt. SSP-bestanden kunnen worden geanalyseerd en geëvalueerd met [Scalate](https://scalate.github.io/scalate/), een op Scala gebaseerde sjabloonengine voor het genereren van tekst en opmaak.

## SSP-bestandsindeling - Meer informatie

SSP-bestanden worden opgeslagen in een tekstbestand zonder opmaak en kunnen worden geëvalueerd met Scalate. Een Ssp-sjabloon bestaat uit platte tekst, wat vaker het HTML-document is. Het bevat Ssp-tags die ervoor zorgen dat de rendering-engines verschillende delen van het document dynamisch weergeven. De tags beginnen en eindigen met <% ... %> en ${ ... } sequentie en alles daarbuiten wordt beschouwd als letterlijke tekst.

### SSP Voorbeeld

Het volgende voorbeeld toont SSP-code en de uitvoer ervan wanneer deze wordt weergegeven door de rendering-engine.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
De uitvoer is als volgt.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referenties

- [SSP-referentie](https://scalate.github.io/scalate/documentation/ssp-reference.html)

