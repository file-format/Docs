---
date: 2022-05-09
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM-bestandsindeling - PYM Macro Preprocessor-bestand
linktitle: PYM
description: "Meer informatie over de PYM-bestandsindeling en API's die PYM-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Wat is een PYM-bestand?

Een PYM-bestand is een macro-preprocessorbestand op basis van de programmeertaal Python. Het is ontwikkeld door VRVis Research en slaat macro-snelkoppelingen op. Wanneer het PYM-bestand wordt geïnterpreteerd door de voorverwerkingsfase van de Python-interpreter, worden deze sneltoetsen uitgebreid als vervanging voor hun volledige tekst. Bovendien is een derde, optionele bewerking die kan worden uitgevoerd door een macro-preprocessor, het opnemen van bestanden. PYM-bestanden kunnen worden geopend in teksteditors zoals Notepad, Notepad++, Apple TextEdit en VI op Linux.

## PYM-bestandsindeling

PYM-bestanden worden als platte tekstbestanden op schijf opgeslagen. Een PYM-bestand kan ook andere bestanden bevatten met behulp van de `#include`-instructie.

### PYM-syntaxis

PYM-instructies zijn opgenomen tussen de markeringen ""#begin python en "#end python", zoals hieronder weergegeven.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM-macro-uitbreiding

De PYM-macro-uitbreiding wordt weergegeven door twee reeksen, namelijk <[ en ]>. Dit zijn speciale html-tags en kunnen overal in een regel voorkomen. Een klein PYM-voorbeeld is als volgt.

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

De output om dit door PYM te laten lopen is als volgt:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referenties ##

* [PYM - Een macro-preprocessor op basis van Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM-tolken](https://github.com/interpreters/pym)

