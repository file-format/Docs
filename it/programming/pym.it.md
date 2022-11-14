---
date: 2022-05-09
autore:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato file PYM - File del preprocessore macro PYM
linktitle: PYM
description: "Scopri il formato di file PYM e le API che possono creare e aprire file PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Che cos'è un file PYM?

Un file PYM è un file di preprocessore di macro basato sul linguaggio di programmazione Python. È stato sviluppato da VRVis Research e memorizza scorciatoie macro. Quando il file PYM viene interpretato dalla fase di preelaborazione dell'interprete Python, queste scorciatoie vengono espanse in sostituzione del testo completo. Inoltre, una terza operazione facoltativa che può essere eseguita da un preprocessore di macro è l'inclusione di file. I file PYM possono essere aperti in editor di testo come Notepad, Notepad++, Apple TextEdit e VI su Linux.

## Formato file PYM

I file PYM vengono salvati come file di testo normale su disco. Un file PYM può anche includere altri file usando la direttiva `#include`.

### Sintassi PYM

Le istruzioni PYM sono incluse tra i marcatori ""#begin python e "#end python", come mostrato di seguito.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Espansione della macro PYM

L'espansione della macro PYM è rappresentata da due sequenze cioè <[ e ]>. Questi sono tag html speciali e possono apparire ovunque in una riga. Un piccolo esempio PYM è il seguente.

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

L'output dell'esecuzione tramite PYM è il seguente:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Riferimenti ##

* [PYM - Un preprocessore di macro basato su Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Interpreti PYM](https://github.com/interpreters/pym)

