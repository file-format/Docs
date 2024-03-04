---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP – „Scala Server“ puslapių failo formaat
linktitle: SSP
description: Luždirbti apie tai, kas yra SSP failo formatas ir API, kurios gali sukurti ir atidaryti SSP failąs.
menu:
  docs:
    identifier: "web-ss-ltp"
    parent: "web"
lastmod: 2021-09-30
---

## Kas yra SSP failas?

Failas su plėtiniu .ssp yra tinklalapis, sukurtas naudojant Scala kodą išraiškoms, o ne tik paprastą HTML. Jis veikia kaip serverio scenarijus, naudojant HTML ir Scala derinį. Šie failai yra serveryje ir naudojami kuriant statinius tinklalapius, kurie bus teikiami vartotojams. Pati Scala yra bendrosios paskirties programavimo kalba, kurios sintaksę žino vartotojai, dirbę su Velocity, JSP ar Erb. SSP failus galima analizuoti ir įvertinti naudojant [Scalate](https://scalate.github.io/scalate/), kuris yra Scala pagrindu sukurtas šablonų variklis, skirtas tekstui ir žymėjimui generuoti.

## SSP failo formatas – daugiau informacijos

SSP failai išsaugomi paprasto teksto faile ir gali būti įvertinti naudojant Scalate. Ssp šabloną sudaro paprastas tekstas, kuris dažniau yra HTML dokumentas. Jame yra įterptos Ssp žymos, dėl kurių atvaizdavimo varikliai dinamiškai atvaizduoja skirtingas dokumento dalis. Žymos prasideda ir baigiasi seka <% ... %> ir ${ ... }, o viskas, kas nėra jų, laikoma pažodiniu tekstu.

### SSP pavyzdys

Šiame pavyzdyje parodytas SSP kodas ir jo išvestis, kai jį pateikia atvaizdavimo variklis.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Išvestis yra tokia.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Nuorodos

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

