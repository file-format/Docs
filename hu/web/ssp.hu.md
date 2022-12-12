---
date: 2021-07-05
keywords: ssp, .ssp, ssp fájlformátum, ssp fájlok megnyitása, Scala Server Page
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP – Scala Server Pages fájlformátum
linktitle: SSP
description: "Ismerje meg, mi az az SSP-fájlformátum, valamint az SSP-fájlok létrehozására és megnyitására alkalmas API-k."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Mi az SSP fájl?

Az .ssp kiterjesztésű fájl olyan weboldal, amelyet Scala kóddal hoznak létre a kifejezésekhez, nem csak egyszerű HTML-kódot. Szerveroldali szkriptként működik a HTML és a Scala kombinációjával. Ezek a fájlok a szerveren találhatók, és statikus weboldalak létrehozására szolgálnak, amelyeket a felhasználóknak kiszolgálnak. Maga a Scala egy általános célú programozási nyelv, amelynek szintaxisa ismerős azoknak a felhasználóknak, akik Velocity-vel, JSP-vel vagy Erb-vel dolgoztak. Az SSP-fájlok a [Scalate](https://scalate.github.io/scalate/) segítségével elemezhetők és értékelhetők, amely egy Scala-alapú sablonmotor szövegek és jelölések generálására.

## SSP fájlformátum - További információ

Az SSP-fájlok egyszerű szöveges fájlba kerülnek, és a Scalate segítségével kiértékelhetők. Az Ssp-sablonok egyszerű szövegből állnak, amely gyakrabban HTML-dokumentum. Ssp címkék vannak beágyazva, amelyek hatására a renderelő motorok dinamikusan jelenítik meg a dokumentum különböző részeit. A címkék <% ... %> és ${ ... } sorozattal kezdődnek és végződnek, és bármi, ami ezeken kívül esik, szó szerinti szövegnek minősül.

### SSP példa

A következő példa az SSP-kódot és annak kimenetét mutatja be, amikor azt a renderelő motor rendereli.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
A kimenet a következő.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Hivatkozások

- [SSP-referencia](https://scalate.github.io/scalate/documentation/ssp-reference.html)

