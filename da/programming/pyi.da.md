---
date: 2022-05-09
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI-filformat - Python Interface Definition
linktitle: PYI
description: Ltjene om PYI filformat og API'er, der kan oprette og åbne PYI fils.
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Hvad er en PYI fil?

En PYI-fil er en Python Interface Definition-fil, der indeholder kodestub-reference til implementering af grænsefladen. Hvert Python-modul er repræsenteret som en .pyi-stub, som er en normal Python-fil, men med tomme metoder. Syntaksen for PYI-filer er den samme som for et almindeligt Python-modul. Implementeringen af de tomme metoder er overladt til slutbrugeren for at opnå det specifikke mål, som modulet er skrevet til. Det er der, hvor PYI-filer er anderledes end [PY](/programming/py/)-filer, som indeholder fuldstændig implementering af programmet. PYI-filer kan åbnes med teksteditorer som Notepad, Notepad++, Microsoft Visual Studio Code og JetBrains PyCharm.

## PYI filformat

PYI-filer gemmes som almindelige tekstfiler, der kan åbnes med enhver teksteditor. Python er et fortolkersprog, der udfører typekontrol, når koden udføres. I sådanne tilfælde er PYI-filer fordelagtige på den måde, at udviklere manuelt kan definere og kontrollere et moduls typer, mens de skriver applikationen.

## Referencer ##

 * [Grænseflader - Java](https://en.wikipedia.org/wiki/Interface_(Java))
 * [PYM-tolke](https://github.com/interpreters/pym)

