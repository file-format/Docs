---
date: 2022-05-09
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM-filformat - PYM Macro Preprocessor-fil
linktitle: PYM
description: "Lär dig om PYM-filformat och API:er som kan skapa och öppna PYM-filer." 
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Vad är PYM fil?

En PYM-fil är en makroförbearbetningsfil baserad på programmeringsspråket Python. Den har utvecklats av VRVis Research och genvägar för butiksmakro. När PYM-filen tolkas av Python-tolkens förbearbetningssteg, utökas dessa genvägar som ersättningar för hela texten. Dessutom är en tredje, valfri operation som kan utföras av en makroförbehandlare filinkludering. PYM-filer kan öppnas i textredigerare som Notepad, Notepad++, Apple TextEdit och VI på Linux.

## PYM filformat

PYM-filer sparas som vanliga textfiler på skiva. En PYM-fil kan också inkludera andra filer genom att använda "#include"-direktivet.

### PYM-syntax

PYM-satser är inkluderade mellan ""#begin python och "#end python"-markörer som visas nedan.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM Makro Expansion

PYM makroexpansionen representeras av två sekvenser, dvs <[ och ]>. Dessa är speciella html-taggar och kan visas var som helst på en rad. Ett litet PYM-exempel är som följer.

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

Resultatet av att köra detta genom PYM är som följer:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Referenser ##

* [PYM - En makroförprocessor baserad på Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM Tolkar](https://github.com/interpreters/pym)

