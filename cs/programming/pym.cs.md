---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formát souboru PYM - Preprocesorový soubor maker PYM
linktitle: PYM
description: "Přečtěte si o formátu souboru PYM a rozhraních API, která mohou vytvářet a otevírat soubory PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Co je soubor PYM?

Soubor PYM je soubor makro preprocesoru založený na programovacím jazyce Python. Byl vyvinut společností VRVis Research a ukládá zkratky maker. Když je soubor PYM interpretován fází předběžného zpracování tlumočníka Pythonu, jsou tyto zkratky rozšířeny jako náhrady za jejich plný text. Kromě toho je třetí, volitelnou operací, kterou může provádět makropreprocesor, zahrnutí souboru. Soubory PYM lze otevřít v textových editorech, jako je Notepad, Notepad++, Apple TextEdit a VI na Linuxu.

## Formát souboru PYM

Soubory PYM se ukládají na disk jako soubory ve formátu prostého textu. Soubor PYM může také obsahovat další soubory pomocí direktivy `#include`.

### Syntaxe PYM

Příkazy PYM jsou zahrnuty mezi značky "#begin python" a "#end python", jak je uvedeno níže.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Rozšíření makra PYM

Rozšíření makra PYM je reprezentováno dvěma sekvencemi, tj. <[ a ]>. Jedná se o speciální html značky a mohou se objevit kdekoli v řádku. Malý příklad PYM je následující.

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

Výstup spuštění přes PYM je následující:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Reference ##

* [PYM – Makro preprocesor založený na Pythonu](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [tlumočníci PYM](https://github.com/interpreters/pym)

