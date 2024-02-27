---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM-filformat - PYM Macro Preprocessor File
linktitle: PYM
description: Ltjene om PYM filformat og API'er, der kan oprette og åbne PYM fils.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Hvad er en PYM fil?

En PYM-fil er en makro-forbehandlerfil baseret på Python-programmeringssproget. Det blev udviklet af VRVis Research og store makro-genveje. Når PYM-filen fortolkes af Python-fortolkerens forbehandlingstrin, udvides disse genveje som erstatninger for deres fulde tekst. Derudover er en tredje, valgfri operation, der kan udføres af en makro-forbehandler, filinkludering. PYM-filer kan åbnes i teksteditorer som Notepad, Notepad++, Apple TextEdit og VI på Linux.

## PYM filformat

PYM-filer gemmes som almindelige tekstfiler på disken. En PYM-fil kan også inkludere andre filer ved at bruge `#include`-direktivet.

### PYM-syntaks

PYM-udsagn er inkluderet mellem #begin python- og #end python-markører som vist nedenfor.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM makroudvidelse

PYM makroudvidelsen er repræsenteret af to sekvenser, dvs. <[ og ]>. Disse er specielle html-tags og kan vises hvor som helst på en linje. Et lille PYM-eksempel er som følger.

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

Outputtet af at køre dette gennem PYM er som følger:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referencer ##

 * [PYM - En makro-forprocessor baseret på Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM-tolke](https://github.com/interpreters/pym)

