---
date: 2021-07-05
keywords: ssp, .ssp, ssp filformat, hur man öppnar ssp-filer, Scala Server Page
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages Filformat
linktitle: SSP
description: "Lär dig mer om vad som är ett SSP-filformat och API:er som kan skapa och öppna SSP-filer." 
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Vad är en SSP fil?

En fil med tillägget .ssp är en webbsida skapad med Scala-kod för uttryck istället för enbart vanlig HTML. Det fungerar som ett serversideskript med kombinationen av HTML och Scala. Dessa filer finns på servern och används för att skapa statiska webbsidor som ska visas för användare. Scala i sig är ett allmänt programmeringsspråk vars syntax är bekant för användare som har arbetat med Velocity, JSP eller Erb. SSP-filer kan analyseras och utvärderas med [Scalate](https://scalate.github.io/scalate/) som är en Scala-baserad mallmotor för att generera text och uppmärkning.

## SSP-filformat - Mer information

SSP-filer sparas i vanlig textfil och kan utvärderas med Scalate. En Ssp-mall består av vanlig text som oftare är HTML-dokumentet. Den har Ssp-taggar inbäddade i den som gör att renderingsmotorerna renderar olika delar av dokumentet dynamiskt. Taggarna börjar och slutar med sekvensen <% ... %> och ${ ... } och allt utanför dessa betraktas som bokstavlig text.

### SSP Exempel

Följande exempel visar SSP-kod och dess utdata när den renderas av renderingsmotorn.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Utgången är följande.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referenser

- [SSP-referens](https://scalate.github.io/scalate/documentation/ssp-reference.html)

