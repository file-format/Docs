---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formát souboru PYD – dynamický modul Python
linktitle: PYD
description: "Přečtěte si o formátu souboru PYD a rozhraních API, která mohou vytvářet a otevírat soubory PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Co je soubor PYD?

Soubor PYD je dynamicky propojovaná knihovna napsaná v Pythonu, kterou lze za běhu spouštět jiným kódem Pythonu. Obsahuje jeden nebo více modulů Pythonu, které usnadňují opětovné použití kódu a poskytují architekturu modulů pro psaní aplikací. Soubory PYD lze vytvářet a ukládat s příponou .pyd, např. helloworld.pyd. Vývojáři aplikací mohou použít příkaz import k zahrnutí modulů PYD do svých aplikací. Soubory PYD lze otevřít pomocí Python Software Foundation Python, který je k dispozici pro OS Windows, Mac a Linux.

## Formát souboru PYD – Další informace

Soubory PYD jsou napsány v programovacím jazyce Python a jsou generovány kompilací kódu Python.

## Rozdíl mezi formáty souborů PY a PYD

Soubor [PY](/cs/programming/py/) obsahuje zdrojový kód, který je spuštěn tak, jak je, a nelze jej zahrnout jako opakovaně použitelný kód v jiných aplikacích Pythonu. Soubor PYD je však dynamicky propojená knihovna pro použití v operačním systému Windows.

## Jak vytvořit soubor PYD?

Soubor PYD lze vytvořit vytvořením modulu s názvem např. exmaple.pyd. Tento modul bude obsahovat všechny funkce ve formě jedné nebo více funkcí, např. PyMod_example(). Když program obsahuje tuto knihovnu a volá ji, lze to provést importem modulu a spustí se funkce PyMod_example().

## Reference ##

* [Vytváření rozšíření Python v C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (programovací jazyk) – Wikipedie](https://en.wikipedia.org/wiki/Python_(programming_language))

