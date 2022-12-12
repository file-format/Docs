---
date: 2021-07-05
keywords: spc, .spc, format pliku spc, jak otwierać pliki spc, plik certyfikatu wydawcy oprogramowania
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC — plik certyfikatu wydawcy oprogramowania
linktitle: SPC
description: "Dowiedz się, co to jest format pliku SPC i interfejsy API, które mogą tworzyć i otwierać pliki SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Czym jest plik SPC?

Plik z rozszerzeniem .spc to cyfrowy plik certyfikatu bezpieczeństwa utworzony w formacie PKCS # 7. Kilka aplikacji tworzy te pliki certyfikatów w celu bezpiecznej wymiany informacji. Niewiele takich aplikacji obejmuje OpenSSL i aplikację Signcode.exe dołączoną do .NET Framework firmy Microsoft. Podobnie jak inne pliki certyfikatów, takie jak [.cer](/pl/web/cer/), [.p7c](/pl/web/p7c/) i [.ssp](/pl/web/ssp/), pliki SPC zawierają klucz publiczny informacje zaszyfrowane kluczem prywatnym. Ten klucz publiczny może być udostępniany użytkownikom publicznie, podczas gdy klucz prywatny jest poufny.

## Format pliku SPC — więcej informacji

Pliki SPC są zapisywane na dysku jako pliki binarne, które można otworzyć w dowolnym edytorze tekstu, ale nie są one czytelne dla człowieka. Są one oparte na najnowszej wersji PKCS # 7, która jest dostępna [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Bibliografia

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Odniesienie do SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

