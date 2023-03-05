---
date: 2022-05-09
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM fájlformátum - PYM makró előfeldolgozó fájl
linktitle: PYM
description: "Ismerje meg a PYM fájlformátumot és az API-kat, amelyek PYM fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Mi az a PYM fájl?

A PYM fájl egy makró előfeldolgozó fájl, amely a Python programozási nyelven alapul. A VRVis Research és a bolti makró parancsikonok fejlesztették ki. Amikor a PYM fájlt a Python interpreter előfeldolgozási szakasza értelmezi, ezek a parancsikonok kibővülnek a teljes szövegük helyettesítéseként. Ezenkívül egy harmadik, opcionális művelet, amelyet a makró-előfeldolgozó végrehajthat, a fájlbefoglalás. A PYM fájlok olyan szövegszerkesztőkkel nyithatók meg, mint a Notepad, Notepad++, Apple TextEdit és VI Linuxon.

## PYM fájlformátum

A PYM fájlok egyszerű szöveges fájlokként kerülnek a lemezre. A PYM-fájlok más fájlokat is tartalmazhatnak az "#include" direktíva használatával.

### PYM szintaxis

A PYM utasítások a "#begin python" és az "#end python" markerek között találhatók, az alábbiak szerint.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM makró bővítés

A PYM makró kiterjesztését két szekvencia képviseli, azaz a <[ és ]>. Ezek speciális html címkék, és bárhol megjelenhetnek egy sorban. Egy kis PYM példa a következő.

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

A PYM-en keresztüli futtatás kimenete a következő:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Hivatkozások ##

* [PYM – Python alapú makróelőfeldolgozó](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM Interpreters](https://github.com/interpreters/pym)

