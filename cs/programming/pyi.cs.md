---
date: 2022-05-09
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formát souboru PYI - definice rozhraní Python
linktitle: PYI
description: "Přečtěte si o formátu souboru PYI a rozhraních API, která mohou vytvářet a otevírat soubory PYI."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Co je soubor PYI?

Soubor PYI je soubor definice rozhraní Python, který obsahuje odkaz na útržek kódu pro implementaci rozhraní. Každý modul Pythonu je reprezentován jako .pyi stub, což je normální soubor Pythonu, ale s prázdnými metodami. Syntaxe souborů PYI je stejná jako u běžného modulu Pythonu. Implementace prázdných metod je ponechána na koncovém uživateli, aby dosáhl konkrétního cíle, pro který je modul napsán. To je místo, kde se soubory PYI liší od souborů [PY](/cs/programming/py/), které obsahují kompletní implementaci programu. Soubory PYI lze otevřít pomocí textových editorů, jako je Notepad, Notepad++, Microsoft Visual Studio Code a JetBrains PyCharm.

## Formát souboru PYI

Soubory PYI se ukládají jako prosté textové soubory, které lze otevřít v libovolném textovém editoru. Python je tlumočnický jazyk, který při spuštění kódu provádí kontrolu typu. V takovém případě jsou soubory PYI výhodné v tom smyslu, že vývojáři mohou ručně definovat a kontrolovat typy modulu při psaní aplikace.

## Reference ##

* [Rozhraní – Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [tlumočníci PYM](https://github.com/interpreters/pym)

