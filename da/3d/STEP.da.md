---
date: 2019-10-11
keywords: step, .step, step file format, how to open step files, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP-filformularat
linktitle: STEP
description: Ltjene om STEP filformat og API'er, der kan oprette og åbne STEP fils.
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Hvad er STEP fil?

STEP-fil er et udbredt dataudvekslingsformat til computerstøttet design (CAD). Det blev standardiseret i 1994 af ISO-udvalget under navnet ISO 10303-21. ISO 10303-21 definerer kodningsmekanismen til at repræsentere data i EXPRESS datamodelleringssprog. En STEP-fil er også kendt som p21-fil og STEP fysisk fil. Filtypenavnene til STEP-fil er .stp og .step.

## Grundlæggende historie

In 1994, the original Part 21 specification was issued. It has some bugs which were corrected by the technical corrigendum issued in 1996. Den anden udgave blev udgivet i 2002, der omfattede berigtigelsen og udvidelser til flere datasektioner. Den tredje udgave blev udgivet i 2016, der tilføjede anker- og referencesektioner, der gjorde det muligt at lagre enheder og værdier i eksterne filer. UTF-8-understøttelse blev tilføjet af strenge. Digitale signaturer blev tilføjet for at verificere indholdet af filen og for at validere legitimationsoplysninger. Understøttelsen til komprimering og lagring af udvekslingsstrukturen ved hjælp af ZIP blev også tilføjet.

## TRIN Filformat

The plain text format for a STEP-file consists of a sequence of records. The character set is defined as code points of ISO 10646. ISO-10303-21; er de første tegn i den første post. Kommentarer er omgivet af /* og */ tegn. Den sidste post indeholder END-ISO-10303-21; hvis STEP-filen er i overensstemmelse med 2002-versionen. Hvis det er i overensstemmelse med 2016-versionen, kan der være en eller flere digitale signaturer efter END-ISO-10303-21; terminator. Linjeskift er angivet med \N\ og sideskift er angivet med \F\.

STEP-filen er opdelt i sektioner, og deres navne er reserverede termer. Alle sektioner slutter med ENDSEC-posten og skal være i den rækkefølge, der er vist nedenfor.

- **HEADER**: Dette er et obligatorisk og ikke-gentageligt afsnit. Den består af følgende enheder:
  - file_description (mandatory)
  - "filnavn (obligatorisk)"
  - "filskema (obligatorisk)"
  - "schema_population (valgfrit)"
  - "file_population (valgfrit)"
  - "section_language (valgfrit)"
  - "section_context (valgfrit)"
- **ANKER**: Det er en valgfri ikke-gentagelig sektion, der blev introduceret i 2016-versionen. Den definerer de eksterne navne for forekomster, så der kan refereres til dem.
- **REFERENCE**: Det er et valgfrit, ikke-gentaget afsnit, der også blev introduceret i 2016-versionen. Hver post i denne sektion knytter et indgangs-/værdiforekomstnavn til en forekomst/værdi i en ekstern fil.
- **DATA**: Det er en valgfri gentagelig sektion, der indeholder kerneindholdet i modelforekomsten.
- **SIGNATURE**: It is an optional repeatable section that was introduced in the 2016 version. It holds the digital signature to verify the file's content or to validate credentials.

## Referencer

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

