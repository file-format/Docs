---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Format pliku PYM — plik preprocesora makr PYM
linktitle: PYM
description: "Dowiedz się więcej o formacie plików PYM i interfejsach API, które mogą tworzyć i otwierać pliki PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Czym jest plik PYM?

Plik PYM to plik preprocesora makr oparty na języku programowania Python. Został opracowany przez VRVis Research i przechowuje skróty do makr. Kiedy plik PYM jest interpretowany przez etap wstępnego przetwarzania interpretera Pythona, skróty te są rozwijane jako zamienniki ich pełnego tekstu. Ponadto trzecią, opcjonalną operacją, którą może wykonać preprocesor makr, jest włączanie plików. Pliki PYM można otwierać w edytorach tekstu, takich jak Notatnik, Notepad ++, Apple TextEdit i VI w systemie Linux.

## Format pliku PYM

Pliki PYM są zapisywane jako zwykłe pliki tekstowe na dysku. Plik PYM może również zawierać inne pliki przy użyciu dyrektywy `#include`.

### Składnia PYM

Instrukcje PYM są zawarte między znacznikami „”#begin python i „#end python”, jak pokazano poniżej.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### Rozszerzenie makro PYM

Ekspansja makro PYM jest reprezentowana przez dwie sekwencje, tj. <[ i ]>. Są to specjalne znaczniki HTML, które mogą pojawić się w dowolnym miejscu wiersza. Mały przykład PYM jest następujący.

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

Wynik uruchomienia tego przez PYM jest następujący:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## Bibliografia ##

* [PYM — preprocesor makr oparty na języku Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [Tłumacze PYM](https://github.com/interpreters/pym)

