---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM failo formatas – PYM makro pirminio procesorius File
linktitle: PYM
description: Luždirbti apie PYM failo formatą ir API, kurios gali sukurti ir atidaryti PYM failąs.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Kas yra PYM failas?

PYM failas yra makrokomandos pirminio procesoriaus failas, pagrįstas Python programavimo kalba. Jį sukūrė VRVis Research ir parduotuvės makrokomandos nuorodos. Kai PYM failą interpretuoja Python interpretatoriaus išankstinio apdorojimo stadija, šie spartieji klavišai išplečiami kaip viso jų teksto pakaitalai. Be to, trečioji, pasirenkama operacija, kurią gali atlikti makrokomandos pirminis procesorius, yra failų įtraukimas. PYM failus galima atidaryti teksto rengyklėse, tokiose kaip Notepad, Notepad++, Apple TextEdit ir VI sistemoje Linux.

## PYM failo formatas

PYM failai diske išsaugomi kaip paprasto teksto failai. PYM failas taip pat gali apimti kitus failus, naudojant direktyvą #include.

### PYM sintaksė

PYM teiginiai yra tarp #begin python ir #end python žymeklių, kaip parodyta toliau.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM makrokomandos išplėtimas

PYM makrokomandos išplėtimas vaizduojamas dviem sekomis, ty <[ ir ]>. Tai yra specialios html žymos ir gali būti rodomos bet kurioje eilutės vietoje. Mažas PYM pavyzdys yra toks.

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

Paleidimo per PYM išvestis yra tokia:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Nuorodos Nr.

 * [PYM – makrokomandos pirminis procesorius, pagrįstas Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
 * [PYM vertėjai](https://github.com/interpreters/pym)

