---
date: 2021-07-05
keywords: spc, .spc, formato de archivo spc, cómo abrir archivos spc, Archivo de certificado de editor de software
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Archivo de certificado de editor de software
linktitle: SPC
description: "Obtenga información sobre qué es un formato de archivo SPC y las API que pueden crear y abrir archivos SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## ¿Qué es un archivo SPC?

Un archivo con extensión .spc es un archivo de certificado de seguridad digital creado en formato PKCS #7. Varias aplicaciones crean estos archivos de certificados para el intercambio seguro de información. Pocas aplicaciones de este tipo incluyen OpenSSL y la aplicación Signcode.exe incluida con .NET Framework de Microsoft. Al igual que otros archivos de certificado como [.cer](/es/web/cer/), [.p7c](/es/web/p7c/) y [.ssp](/es/web/ssp/), los archivos SPC contienen la clave pública información cifrada con una clave privada. Esta clave pública se puede compartir con los usuarios públicamente, mientras que la clave privada se mantiene confidencial.

## Formato de archivo SPC: más información

Los archivos SPC se guardan en el disco como archivos binarios que se pueden abrir en cualquier editor de texto, pero no son legibles por humanos. Estos se basan en la última versión de PKCS # 7 que está disponible [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Referencias

* [PKCS 7](https://en.wikipedia.org/wiki/PKCS_7)
* [Referencia SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)
