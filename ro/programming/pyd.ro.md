---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format de fișier PYD - Modulul dinamic Python
linktitle: PYD
description: "Aflați despre formatul de fișier PYD și despre API-urile care pot crea și deschide fișiere PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Ce este un fișier PYD?

Un fișier PYD este o bibliotecă de linkuri dinamice scrisă în Python care poate fi rulată de alt cod Python în timpul rulării. Conține unul sau mai multe module Python care facilitează reutilizarea codului și oferă arhitectură de module pentru scrierea aplicațiilor. Fișierele PYD pot fi create și salvate cu extensia .pyd, de exemplu helloworld.pyd. Dezvoltatorii de aplicații pot folosi instrucțiunea de import pentru a include modulele PYD în aplicațiile lor. Fișierele PYD pot fi deschise cu Python Software Foundation Python, care este disponibil pentru sistemul de operare Windows, Mac și Linux.

## Format de fișier PYD - Mai multe informații

Fișierele PYD sunt scrise în limbajul de programare Python și sunt generate prin compilarea codului Python.

## Diferența dintre formatele de fișiere PY și PYD

Un fișier [PY](/ro/programming/py/) conține cod sursă care este executat așa cum este și nu poate fi inclus ca cod reutilizabil în alte aplicații Python. Cu toate acestea, un fișier PYD este o bibliotecă cu legături dinamice care poate fi utilizată pe sistemul de operare Windows.

## Cum se creează un fișier PYD?

Un fișier PYD poate fi creat prin crearea unui modul cu un nume de exemplu exmaple.pyd. Acest modul va conține toată funcționalitatea sub forma uneia sau mai multor funcții, de exemplu PyMod_example(). Când programul include această bibliotecă și o apelează, se poate face importând modulul și se va rula funcția PyMod_example().

## Referințe ##

* [Crearea extensiilor Python în C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (limbaj de programare) - Wikipedia](https://en.wikipedia.org/wiki/Python_(limbaj_de_programare))

