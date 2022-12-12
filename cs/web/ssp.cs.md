---
date: 2021-07-05
keywords: ssp, .ssp, formát souborů ssp, jak otevřít soubory ssp, Scala Server Page
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Formát souborů Scala Server Pages
linktitle: SSP
description: "Zjistěte, co je formát souboru SSP a rozhraní API, která mohou vytvářet a otevírat soubory SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Co je soubor SSP?

Soubor s příponou .ssp je webová stránka vytvořená pouze kódem Scala pro výrazy namísto prostého HTML. Funguje jako skript na straně serveru pomocí kombinace HTML a Scala. Tyto soubory jsou umístěny na serveru a používají se k vytváření statických webových stránek, které mají být poskytovány uživatelům. Scala sama o sobě je univerzální programovací jazyk, jehož syntaxe je známá uživatelům, kteří pracovali s Velocity, JSP nebo Erb. Soubory SSP lze analyzovat a vyhodnocovat pomocí [Scalate](https://scalate.github.io/scalate/), což je šablonovací stroj založený na Scale pro generování textu a značek.

## Formát souboru SSP – Další informace

Soubory SSP jsou uloženy v prostém textovém souboru a lze je vyhodnotit pomocí Scalate. Šablona Ssp se skládá z prostého textu, což je častěji dokument HTML. Má v sobě vložené značky Ssp, které způsobují, že vykreslovací motory dynamicky vykreslují různé části dokumentu. Značky začínají a končí sekvencí <% ... %> a ${ ... } a vše mimo ně je považováno za doslovný text.

### Příklad SSP

Následující příklad ukazuje kód SSP a jeho výstup, když je vykreslen vykreslovacím modulem.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Výstup je následující.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Reference

– [Reference SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

