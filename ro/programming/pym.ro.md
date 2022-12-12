---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fișier PYM - Fișier PYM Macro Preprocessor
linktitle: PYM
description: "Aflați despre formatul de fișier PYM și despre API-urile care pot crea și deschide fișiere PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Ce este un fișier PYM?

Un fișier PYM este un fișier macro preprocesor bazat pe limbajul de programare Python. A fost dezvoltat de VRVis Research și stochează comenzi rapide pentru macrocomenzi. Când fișierul PYM este interpretat de etapa de preprocesare a interpretului Python, aceste comenzi rapide sunt extinse ca înlocuitori pentru textul lor complet. În plus, o a treia operație, opțională, care poate fi efectuată de un preprocesor macro este includerea fișierelor. Fișierele PYM pot fi deschise în editori de text precum Notepad, Notepad++, Apple TextEdit și VI pe Linux.

## Format de fișier PYM

Fișierele PYM sunt salvate ca fișiere text simplu pe disc. Un fișier PYM poate include și alte fișiere folosind directiva `#include`.

### Sintaxa PYM

Declarațiile PYM sunt incluse între markerii „"#begin python și "#end python", așa cum se arată mai jos.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Macro Expansion

Extinderea macro PYM este reprezentată de două secvențe, adică <[ și ]>. Acestea sunt etichete html speciale și pot apărea oriunde într-o linie. Un mic exemplu PYM este după cum urmează.

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

Rezultatul rulării prin PYM este după cum urmează:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referințe ##

* [PYM - Un preprocesor macro bazat pe Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Interpreți PYM](https://github.com/interpreters/pym)

