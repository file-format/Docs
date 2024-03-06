---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP faila veidlapaat
linktitle: STEP
description: Lnopelniet par STEP faila formātu un API, kas var izveidot un atvērt STEP failus.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Kas ir STEP fails?

STEP fails ir plaši izmantots datu apmaiņas formāts datorizētai projektēšanai (CAD). ISO komiteja to standartizēja 1994. gadā ar nosaukumu ISO 10303-21. ISO 10303-21 nosaka kodēšanas mehānismu datu attēlošanai EXPRESS datu modelēšanas valodā. STEP fails ir pazīstams arī kā p21-File un STEP fiziskais fails. STEP failam izmantotie faila paplašinājumi ir .stp un .step.

## Pamatvēsture

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. Otrais izdevums tika publicēts 2002. gadā, kurā bija iekļauts labojums un paplašinājumi vairākām datu sadaļām. Trešais izdevums tika publicēts 2016. gadā, kurā tika pievienotas enkura un atsauces sadaļas, kas ļāva entītijas un vērtības saglabāt ārējos failos. Tika pievienots virkņu UTF-8 atbalsts. Lai pārbaudītu faila saturu un apstiprinātu akreditācijas datus, tika pievienoti digitālie paraksti. Tika pievienots arī atbalsts apmaiņas struktūras saspiešanai un glabāšanai, izmantojot ZIP.

## STEP faila formāts

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; ir pirmās rakstzīmes pirmajā ierakstā. Komentārus ieskauj rakstzīmes /* un */. Pēdējais ieraksts satur END-ISO-10303-21; ja STEP fails atbilst 2002. gada versijai. Ja tas atbilst 2016. gada versijai, aiz END-ISO-10303-21; var būt viens vai vairāki ciparparaksti. terminators. Rindas pārtraukumi ir apzīmēti ar \N\ un lappušu pārtraukumi ir apzīmēti ar \F\.

STEP fails ir sadalīts sadaļās, un to nosaukumi ir rezervēti vārdi. Visas sadaļas beidzas ar ierakstu ENDSEC, un tām ir jābūt tālāk norādītajā secībā.

- **HEADDER**: šī ir obligāta un neatkārtojama sadaļa. Tas sastāv no šādām vienībām:
  - file_description (mandatory)
  - "faila_nosaukums (obligāts)"
  - "file_schema (obligāti)"
  - "shēmas_populācija (neobligāti)"
  - "file_population (neobligāti)"
  - "sadaļas_valoda (neobligāti)"
  - "section_context (neobligāti)"
- **ANCHOR**: tā ir izvēles sadaļa, kas neatkārtojas un tika ieviesta 2016. gada versijā. Tas definē gadījumu ārējos nosaukumus, lai uz tiem varētu atsaukties.
- **ATSAUCES**: tā ir izvēles sadaļa, kas neatkārtojas un tika ieviesta arī 2016. gada versijā. Katrs šīs sadaļas ieraksts saista ieraksta/vērtības instances nosaukumu ar instanci/vērtību ārējā failā.
- **DATI**: tā ir neobligāta atkārtojama sadaļa, kas satur modeļa instances galveno saturu.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## Atsauces

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

