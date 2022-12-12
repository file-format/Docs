---
date: 2021-07-05
keywords: ssp, .ssp, format de fișier ssp, cum să deschideți fișierele ssp, pagina serverului Scala
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages File Format
linktitle: SSP
description: "Aflați despre ce este un format de fișier SSP și despre API-urile care pot crea și deschide fișiere SSP."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## Ce este un fișier SSP?

Un fișier cu extensia .ssp este o pagină web creată cu cod Scala pentru expresii în loc de HTML simplu. Acționează ca un script pe partea de server folosind combinația de HTML și Scala. Aceste fișiere se află pe server și sunt folosite pentru a crea pagini web statice care să fie oferite utilizatorilor. Scala în sine este un limbaj de programare de uz general a cărui sintaxă este familiară utilizatorilor care au lucrat cu Velocity, JSP sau Erb. Fișierele SSP pot fi analizate și evaluate folosind [Scalate](https://scalate.github.io/scalate/), care este un motor de șablon bazat pe Scala pentru generarea de text și marcare.

## Format de fișier SSP - Mai multe informații

Fișierele SSP sunt salvate într-un fișier text simplu și pot fi evaluate folosind Scalate. Un șablon Ssp constă din text simplu, care este mai adesea documentul HTML. Are etichete Ssp încorporate care determină motoarele de randare să redeze dinamic diferite porțiuni ale documentului. Etichetele încep și se termină cu secvența <% ... %> și ${ ... } și orice în afara acestora este considerat text literal.

### Exemplu SSP

Următorul exemplu arată codul SSP și ieșirea acestuia atunci când este redat de motorul de randare.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Ieșirea este după cum urmează.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Referințe

- [Referință SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

