---
date: 2019-10-11
keywords: pas, .step, format de fișier pas, cum se deschide fișierele pas, extensie .step, extensie pas
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP Format de fișier
linktitle: STEP
description: "Aflați despre formatul de fișier STEP și despre API-urile care pot crea și deschide fișiere STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Ce este un fișier STEP?

Fișierul STEP este un format de schimb de date utilizat pe scară largă pentru proiectarea asistată de computer (CAD). A fost standardizat în 1994 de către comitetul ISO sub denumirea de „ISO 10303-21”. ISO 10303-21 definește mecanismul de codificare pentru reprezentarea datelor în limbajul de modelare a datelor EXPRESS. Un fișier STEP- este cunoscut și sub numele de p21-File și STEP Physical File. Extensiile de fișiere utilizate pentru fișierul STEP sunt .stp și .step.

## Istoria de bază

În 1994, a fost emisă specificația originală Partea 21. Are câteva erori care au fost corectate prin rectificarea tehnică emisă în 1996. A doua ediție a fost publicată în 2002 care includea rectificarea și extensiile pentru mai multe secțiuni de date. A treia ediție a fost publicată în 2016, care a adăugat secțiuni de ancorare și referință care permiteau stocarea entităților și valorilor în fișiere externe. A fost adăugat suportul UTF-8 de șiruri. Au fost adăugate semnături digitale pentru a verifica conținutul fișierului și pentru a valida acreditările. A fost adăugat și suportul pentru comprimarea și stocarea structurii de schimb folosind ZIP.

## STEP Format de fișier

Formatul text simplu pentru un fișier STEP constă dintr-o secvență de înregistrări. Setul de caractere este definit ca puncte de cod ale ISO 10646. „ISO-10303-21;” sunt primele caractere din prima înregistrare. Comentariile sunt înconjurate de caractere „/*” și „*/”. Ultima înregistrare conține „END-ISO-10303-21;” dacă fișierul STEP este conform versiunii 2002. În cazul în care este conform versiunii 2016, pot exista una sau mai multe semnături digitale după „END-ISO-10303-21;” terminator. Întrerupțiile de linie sunt notate cu „\N\”, iar sfârșiturile de pagină sunt notate cu „\F\”.

Fișierul STEP este împărțit în secțiuni, iar numele acestora sunt termeni rezervați. Toate secțiunile se termină cu înregistrarea „ENDSEC” și trebuie să fie în ordinea prezentată mai jos.

- **HEADER**: Aceasta este o secțiune obligatorie și nerepetabilă. Este format din următoarele entități:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCORA**: este o secțiune opțională care nu se repetă care a fost introdusă în versiunea 2016. Definește numele externe pentru instanțe, astfel încât să poată fi referite.
- **REFERINȚĂ**: Este o secțiune opțională care nu se repetă care a fost introdusă și în versiunea 2016. Fiecare intrare din această secțiune asociază un nume de instanță de intrare/valoare cu o instanță/valoare dintr-un fișier extern.
- **DATE**: este o secțiune repetabilă opțională care conține conținutul de bază al instanței model.
- **SEMNATURĂ**: este o secțiune repetabilă opțională care a fost introdusă în versiunea 2016. Acesta deține semnătura digitală pentru a verifica conținutul fișierului sau pentru a valida acreditările.

## Referințe

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

