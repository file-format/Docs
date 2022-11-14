---
date: 2021-07-05
keywords: spc, .spc, spc-bestandsindeling, hoe spc-bestanden te openen, Software Publisher-certificaatbestand
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Certificaatbestand voor software-uitgevers
linktitle: SPC
description: "Meer informatie over wat een SPC-bestandsindeling is en API's die SPC-bestanden kunnen maken en openen."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Wat is een SPC-bestand?

Een bestand met de extensie .spc is een bestand met digitale beveiligingscertificaten dat is gemaakt in de PKCS # 7-indeling. Verschillende toepassingen maken deze certificaatbestanden aan voor een veilige uitwisseling van informatie. Weinig van dergelijke toepassingen bevatten OpenSSL en de toepassing Signcode.exe die bij Microsoft's .NET Framework wordt geleverd. Net als andere certificaatbestanden zoals [.cer](/nl/web/cer/), [.p7c](/nl/web/p7c/) en [.ssp](/nl/web/ssp/), bevatten de SPC-bestanden de openbare sleutel informatie die is versleuteld met een privésleutel. Deze openbare sleutel kan openbaar met gebruikers worden gedeeld, terwijl de privésleutel vertrouwelijk blijft.

## SPC-bestandsindeling - Meer informatie

De SPC-bestanden worden op schijf opgeslagen als binaire bestanden die in elke teksteditor kunnen worden geopend, maar die niet door mensen leesbaar zijn. Deze zijn gebaseerd op de nieuwste versie van PKCS # 7 die beschikbaar is [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referenties

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [SSP-referentie](https://scalate.github.io/scalate/documentation/ssp-reference.html)

