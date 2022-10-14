---
date: 2022-05-09
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYM-Dateiformat - PYM-Makro-Präprozessordatei"
linktitle: "PYM"
description: "Erfahren Sie mehr über das PYM-Dateiformat und APIs, die PYM-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Was ist eine PYM-Datei?

Eine PYM-Datei ist eine Makro-Präprozessordatei, die auf der Programmiersprache Python basiert. Es wurde von VRVis Research entwickelt und speichert Makroverknüpfungen. Wenn die PYM-Datei von der Vorverarbeitungsphase des Python-Interpreters interpretiert wird, werden diese Verknüpfungen als Ersatz für ihren vollständigen Text erweitert. Darüber hinaus ist eine dritte optionale Operation, die von einem Makro-Präprozessor ausgeführt werden kann, die Dateiaufnahme. PYM-Dateien können in Texteditoren wie Notepad, Notepad++, Apple TextEdit und VI unter Linux geöffnet werden.

## PYM-Dateiformat

PYM-Dateien werden als reine Textdateien auf der Disc gespeichert. Eine PYM-Datei kann auch andere Dateien mit der Direktive "#include" enthalten.

### PYM-Syntax

PYM-Anweisungen sind zwischen den Markierungen "" #begin python und "#end python" enthalten, wie unten gezeigt.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM-Makroerweiterung

Die PYM-Makroerweiterung wird durch zwei Sequenzen dargestellt, dh <[ und ]>. Dies sind spezielle HTML-Tags und können überall in einer Zeile erscheinen. Ein kleines PYM-Beispiel ist wie folgt.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

Die Ausgabe, wenn Sie dies über PYM ausführen, lautet wie folgt:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Verweise ##

* [PYM - Ein auf Python basierender Makro-Präprozessor](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM-Interpreter](https://github.com/interpreters/pym)

