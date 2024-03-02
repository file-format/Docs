---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PFormáid Chomhaid YM - Réamhphróiseálaí Macra PYM File
linktitle: PYM
description: Ltuilleamh faoi fhormáid comhaid PYM agus APIs ar féidir leo comhad PYM a chruthú agus a oscailts.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Cad is comhad PYM ann?

Is comhad réamhphróiseálaí macra é comhad PYM bunaithe ar theanga ríomhchlárúcháin Python. Forbraíodh é ag VRVis Research agus aicearraí macra a stóráil. Nuair a dhéantar an comhad PYM a léirmhíniú ag céim réamhphróiseála an ateangaire Python, leathnaítear na haicearraí seo mar athsholáthar ar a dtéacs iomlán. Ina theannta sin, is éard atá sa tríú oibríocht roghnach is féidir le réamhphróiseálaí macra a dhéanamh ná cuimsiú comhaid. Is féidir comhaid PYM a oscailt in eagarthóirí téacs mar Notepad, Notepad ++, Apple TextEdit, agus VI ar Linux.

## Formáid Chomhaid PYM

Déantar comhaid PYM a shábháil mar chomhaid gnáth-théacs ar diosca. Is féidir comhaid eile a áireamh i gcomhad PYM freisin ag baint úsáide as an treoir `#include`.

### Comhréir PYM

Áirítear ráitis PYM idir na marcóirí #begin python agus #end python mar a thaispeántar thíos.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Leathnú Macra PYM

Léirítear leathnú macra PYM ag dhá sheicheamh .i. <[ agus ]>. Is clibeanna html speisialta iad seo agus is féidir iad a thaispeáint áit ar bith i líne. Seo a leanas sampla beag PYM.

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

Seo a leanas an t-aschur chun é seo a rith trí PYM:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Tagairtí ##

 * [PYM - Réamhphróiseálaí Macra Bunaithe ar Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [Ateangairí PYM]( https://github.com/interpreters/pym)

