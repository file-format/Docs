---
date: 2021-07-05
keywords: spc, .spc, formát souboru spc, jak otevřít soubory spc, soubor certifikátu vydavatele softwaru
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Soubor certifikátu vydavatele softwaru
linktitle: SPC
description: "Zjistěte, co je formát souboru SPC a rozhraní API, která mohou vytvářet a otevírat soubory SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Co je soubor SPC?

Soubor s příponou .spc je soubor certifikátu digitálního zabezpečení vytvořený ve formátu PKCS # 7. Několik aplikací vytváří tyto soubory certifikátů pro bezpečnou výměnu informací. Jen málo takových aplikací zahrnuje OpenSSL a aplikaci Signcode.exe, která je součástí Microsoft .NET Framework. Stejně jako jiné soubory certifikátů, jako je [.cer](/cs/web/cer/), [.p7c](/cs/web/p7c/) a [.ssp](/cs/web/ssp/), soubory SPC obsahují veřejný klíč informace, které jsou zašifrovány soukromým klíčem. Tento veřejný klíč lze sdílet s uživateli veřejně, zatímco soukromý klíč je důvěrný.

## Formát souboru SPC – Další informace

Soubory SPC se ukládají na disk jako binární soubory, které lze otevřít v libovolném textovém editoru, ale nejsou čitelné pro člověka. Ty jsou založeny na nejnovější verzi PKCS # 7, která je k dispozici [RFC 2315] (https://datatracker.ietf.org/doc/html/rfc2315).

## Reference

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Reference SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

