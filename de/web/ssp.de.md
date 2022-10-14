---
date: 2021-07-05
keywords: "ssp, .ssp, ssp-Dateiformat, Öffnen von ssp-Dateien, Scala-Serverseite"
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "SSP - Dateiformat für Scala-Serverseiten"
linktitle: "SSP"
description: "Erfahren Sie, was ein SSP-Dateiformat und APIs sind, die SSP-Dateien erstellen und öffnen können."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Was ist eine SSP-Datei?

Eine Datei mit der Erweiterung .ssp ist eine Webseite, die mit Scala-Code für Ausdrücke anstelle von reinem HTML erstellt wurde. Es fungiert als serverseitiges Skript, das eine Kombination aus HTML und Scala verwendet. Diese Dateien befinden sich auf dem Server und werden verwendet, um statische Webseiten zu erstellen, die Benutzern bereitgestellt werden. Scala selbst ist eine universelle Programmiersprache, deren Syntax Benutzern vertraut ist, die mit Velocity, JSP oder Erb gearbeitet haben. SSP-Dateien können mit [Scalate](https://scalate.github.io/scalate/) analysiert und ausgewertet werden, einer Scala-basierten Vorlagen-Engine zum Generieren von Text und Markup.

## SSP-Dateiformat – Weitere Informationen

SSP-Dateien werden als reine Textdatei gespeichert und können mit Scalate ausgewertet werden. Eine SSP-Vorlage besteht aus einfachem Text, der häufiger das HTML-Dokument ist. Es hat darin eingebettete Ssp-Tags, die bewirken, dass die Rendering-Engines verschiedene Teile des Dokuments dynamisch rendern. Die Tags beginnen und enden mit der Sequenz <% ... %> und ${ ... }, und alles außerhalb davon wird als wörtlicher Text betrachtet.

### SSP-Beispiel

Das folgende Beispiel zeigt SSP-Code und seine Ausgabe, wenn er von der Rendering-Engine gerendert wird.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Die Ausgabe ist wie folgt.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Verweise

- [SSP-Referenz](https://scalate.github.io/scalate/documentation/ssp-reference.html)

