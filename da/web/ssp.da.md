---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages File Format
linktitle: SSP
description: Ltjene om, hvad der er et SSP-filformat og API'er, der kan oprette og åbne SSP-fils.
menu:
  docs:
    identifier: "web-ss-dap"
    parent: "web"
lastmod: 2021-09-30
---

## Hvad er en SSP fil?

En fil med filtypenavnet .ssp er en webside oprettet med Scala-kode til udtryk i stedet for kun almindelig HTML. Det fungerer som et serversidescript ved hjælp af kombinationen af HTML og Scala. Disse filer ligger på serveren og bruges til at oprette statiske websider, der skal vises til brugerne. Scala i sig selv er et alment programmeringssprog, hvis syntaks er velkendt for brugere, der har arbejdet med Velocity, JSP eller Erb. SSP-filer kan analyseres og evalueres ved hjælp af [Scalate](https://scalate.github.io/scalate/), som er en Scala-baseret skabelonmotor til generering af tekst og opmærkning.

## SSP-filformat - flere oplysninger

SSP-filer gemmes i almindelig tekstfil og kan evalueres ved hjælp af Scalate. En Ssp-skabelon består af almindelig tekst, som oftere er HTML-dokumentet. Det har Ssp-tags indlejret i det, der får gengivelsesmotorerne til at gengive forskellige dele af dokumentet dynamisk. Mærkerne starter og slutter med sekvensen <% ... %> og ${ ... }, og alt uden for disse betragtes som bogstavelig tekst.

### SSP eksempel

Følgende eksempel viser SSP-kode og dens output, når den gengives af renderingsmotoren.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Udgangen er som følger.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referencer

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

