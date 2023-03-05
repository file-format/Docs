---
date: 2021-07-05
keywords: spc, .spc, format de fichier spc, comment ouvrir les fichiers spc, fichier de certificat de l'éditeur de logiciels
auteur:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Fichier de certificat d'éditeur de logiciel
linktitle: SPC
description: "Découvrez ce qu'est un format de fichier SPC et les API qui peuvent créer et ouvrir des fichiers SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Qu'est-ce qu'un fichier SPC ?

Un fichier avec l'extension .spc est un fichier de certificat de sécurité numérique créé au format PKCS # 7. Plusieurs applications créent ces fichiers de certificat pour un échange sécurisé d'informations. Peu de ces applications incluent OpenSSL et l'application Signcode.exe incluse avec le .NET Framework de Microsoft. Comme d'autres fichiers de certificat tels que [.cer](/fr/web/cer/), [.p7c](/fr/web/p7c/) et [.ssp](/fr/web/ssp/), les fichiers SPC contiennent la clé publique informations chiffrées avec une clé privée. Cette clé publique peut être partagée publiquement avec les utilisateurs tandis que la clé privée reste confidentielle.

## Format de fichier SPC - Plus d'informations

Les fichiers SPC sont enregistrés sur le disque sous forme de fichiers binaires qui peuvent être ouverts dans n'importe quel éditeur de texte mais ne sont pas lisibles par l'homme. Ceux-ci sont basés sur la dernière version de PKCS # 7 qui est disponible [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Références

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Référence SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)
