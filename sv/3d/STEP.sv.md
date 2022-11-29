---
date: 2019-10-11
keywords: step, .step, step filformat, hur man öppnar step-filer, .step extension, step extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEG Filformat
linktitle: STEP
description: "Lär dig om STEP-filformat och API:er som kan skapa och öppna STEP-filer."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Vad är STEP fil?

STEP-fil är ett allmänt använt format för datautbyte för datorstödd design (CAD). Den standardiserades 1994 av ISO-kommittén under namnet "ISO 10303-21". ISO 10303-21 definierar kodningsmekanismen för att representera data i EXPRESS datamodelleringsspråk. En STEP-fil är också känd som p21-fil och STEP Physical File. Filtilläggen som används för STEP-fil är .stp och .step.

## Grundläggande historia

1994 utfärdades den ursprungliga Part 21-specifikationen. Den har några buggar som korrigerades av den tekniska rättelse som utfärdades 1996. Den andra upplagan publicerades 2002 som inkluderade rättelse och tillägg för flera datasektioner. Den tredje upplagan publicerades 2016 som lade till ankar- och referenssektioner som gjorde att enheter och värden kunde lagras i externa filer. UTF-8-stöd lades till av strängar. Digitala signaturer lades till för att verifiera innehållet i filen och för att validera referenser. Stödet för att komprimera och lagra utbytesstrukturen med ZIP lades också till.

## STEG Filformat

Oformaterad text för en STEP-fil består av en sekvens av poster. Teckenuppsättningen definieras som kodpunkter enligt ISO 10646. "ISO-10303-21;" är de första tecknen i den första posten. Kommentarer omges av "/*" och "*/" tecken. Den sista posten innehåller "END-ISO-10303-21;" om STEP-filen överensstämmer med 2002 års version. Om den överensstämmer med 2016 års version kan det finnas en eller flera digitala signaturer efter "END-ISO-10303-21;" terminator. Radbrytningar betecknas med "\N\" och sidbrytningar betecknas med "\F\".

STEP-filen är uppdelad i sektioner och deras namn är reserverade termer. Alla avsnitt slutar med "ENDSEC"-posten och måste vara i den ordning som visas nedan.

- **HEADER**: Detta är ett obligatoriskt avsnitt som inte kan upprepas. Den består av följande enheter:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Det är en valfri icke-repeterande sektion som introducerades i 2016 års version. Den definierar de externa namnen för instanser så att de kan refereras till.
- **REFERENS**: Det är ett valfritt avsnitt som inte upprepas som också introducerades i 2016 års version. Varje post i det här avsnittet associerar ett namn på en post/värdeinstans till en instans/värde i en extern fil.
- **DATA**: Det är ett valfritt repeterbart avsnitt som innehåller kärninnehållet i modellinstansen.
- **SIGNATUR**: Det är en valfri repeterbar sektion som introducerades i 2016 års version. Den innehåller den digitala signaturen för att verifiera filens innehåll eller för att validera referenser.

## Referenser

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

