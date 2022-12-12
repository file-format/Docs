---
date: 2021-07-05
keywords: ssp, .ssp, format pliku ssp, jak otwierać pliki ssp, Scala Server Page
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP — format pliku stron serwera Scala
linktitle: SSP
description: "Dowiedz się, co to jest format pliku SSP i interfejsy API, które mogą tworzyć i otwierać pliki SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Czym jest plik SSP?

Plik z rozszerzeniem .ssp to strona internetowa stworzona za pomocą kodu Scala dla wyrażeń zamiast zwykłego HTML. Działa jako skrypt po stronie serwera, używając kombinacji HTML i Scali. Pliki te znajdują się na serwerze i służą do tworzenia statycznych stron internetowych, które mają być udostępniane użytkownikom. Sama Scala jest językiem programowania ogólnego przeznaczenia, którego składnia jest znana użytkownikom, którzy pracowali z Velocity, JSP czy Erb. Pliki SSP można analizować i oceniać za pomocą [Scalate](https://scalate.github.io/scalate/), który jest opartym na Scali silnikiem szablonów do generowania tekstu i znaczników.

## Format pliku SSP — więcej informacji

Pliki SSP są zapisywane w zwykłym pliku tekstowym i można je ocenić za pomocą Scalate. Szablon SSP składa się ze zwykłego tekstu, którym częściej jest dokument HTML. Ma osadzone tagi SSP, które powodują, że silniki renderujące dynamicznie renderują różne części dokumentu. Tagi zaczynają się i kończą sekwencją <% ... %> i ${ ... }, a wszystko poza nimi jest traktowane jako tekst dosłowny.

### Przykład SSP

Poniższy przykład przedstawia kod SSP i jego dane wyjściowe podczas renderowania przez aparat renderujący.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Dane wyjściowe są następujące.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Bibliografia

- [Odniesienie do SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

