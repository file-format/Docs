---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM faila formāts — PYM makro priekšprocesors File
linktitle: PYM
description: Lnopelniet par PYM faila formātu un API, kas var izveidot un atvērt PYM failus.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Kas ir PYM fails?

PYM fails ir makro priekšprocesora fails, kura pamatā ir Python programmēšanas valoda. To izstrādāja VRVis Research un veikala makro saīsnes. Kad PYM failu interpretē Python tulka priekšapstrādes stadija, šie īsinājumtaustiņi tiek izvērsti kā pilnā teksta aizstājēji. Turklāt trešā izvēles darbība, ko var veikt makro priekšapstrādātājs, ir failu iekļaušana. PYM failus var atvērt teksta redaktoros, piemēram, Notepad, Notepad++, Apple TextEdit un VI operētājsistēmā Linux.

## PYM faila formāts

PYM faili diskā tiek saglabāti kā vienkārša teksta faili. PYM fails var ietvert arī citus failus, izmantojot direktīvu #include.

### PYM sintakse

PYM priekšraksti ir iekļauti starp marķieriem #begin python un #end python, kā parādīts tālāk.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM makro paplašināšana

PYM makro paplašinājumu attēlo divas secības, ti, <[ un ]>. Tie ir īpaši html tagi, un tie var parādīties jebkurā rindā. Neliels PYM piemērs ir šāds.

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

Šīs darbības rezultāts, izmantojot PYM, ir šāds:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Atsauces Nr.

 * [PYM — makro priekšprocesors, kura pamatā ir Python] (http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM tulki](https://github.com/interpreters/pym)

