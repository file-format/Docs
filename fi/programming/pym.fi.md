---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM-tiedostomuoto - PYM Macro Preprocessor File
linktitle: PYM
description: Ltienaa PYM-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata PYM-tiedostons.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Mikä on PYM-tiedosto?

PYM-tiedosto on Python-ohjelmointikieleen perustuva makroesikäsittelytiedosto. Sen on kehittänyt VRVis Research and store makropikakuvakkeet. Kun Python-tulkin esikäsittelyvaihe tulkitsee PYM-tiedoston, nämä pikakuvakkeet laajennetaan korvaamaan koko tekstinsä. Lisäksi kolmas, valinnainen toiminto, jonka makroesikäsittelijä voi suorittaa, on tiedostojen sisällyttäminen. PYM-tiedostoja voidaan avata tekstieditoreilla, kuten Notepad, Notepad++, Apple TextEdit ja VI Linuxissa.

## PYM tiedostomuoto

PYM-tiedostot tallennetaan pelkkänä tekstitiedostona levylle. PYM-tiedosto voi sisältää myös muita tiedostoja #include-ohjeen avulla.

### PYM-syntaksi

PYM-lauseet sisältyvät #begin python- ja #end python -merkkien väliin alla olevan kuvan mukaisesti.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM-makrolaajennus

PYM-makrolaajennus esitetään kahdella sekvenssillä eli <[ ja ]>. Nämä ovat erityisiä html-tageja, ja ne voivat esiintyä missä tahansa rivissä. Pieni PYM-esimerkki on seuraava.

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

Tämän PYM:n kautta suoritettava tulos on seuraava:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Viitteet ##

 * [PYM – Pythoniin perustuva makroesikäsittely](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM Interpreters](https://github.com/interpreters/pym)

