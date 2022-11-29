---
date: 2019-10-11
keywords: WEBM, Vad är en WEBM-fil, WEBM-filformat
författare:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Lär dig mer om WEBM-filformat och API:er som kan skapa och öppna WEBM-filer." 
title: WEBM - WebM Videofilformat
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Vad är en WEBM fil?

En fil med filtillägget .webm är en videofil baserad på det öppna, royaltyfria filformatet WebM. Den har utformats för att dela video på webben och definierar filbehållarens struktur inklusive video- och ljudformat. WebM är 100 % gratis och implementerar högkvalitativt baserad på öppna teknologier som HTML, HTTP och TCP/IP som är öppna för alla för implementering. WebM har utformats speciellt för att visa video på webben vilket gör den optimerad för streaming med ett lågt beräkningsfotavtryck. Detta gör den lämplig för uppspelning av videor på alla enheter, särskilt lågeffekts netbooks, handdatorer och surfplattor.

## WEBM filformat

WebM-filstrukturen är baserad på en delmängd av Matroska [MKV](/sv/video/mkv/) containerfilformat. Videoströmmarna som är tillgängliga i en WebM-fil komprimeras med VP8- eller VP9-komprimeringstekniker som är mycket effektiva vid komprimering. På liknande sätt komprimeras ljudströmmarna i en WebM-fil med Vorbis- eller Opus-codec som utvecklades av [Xiph Foundation](https://www.xiph.org/). Alla dessa videor och ljudkodekar är royaltyfria och kan användas utan några avgifter.

Följande är de sammanfattade specifikationerna för WebM-filformatet.

|Fält|Beskrivning|
---|---|
|MIME-typ |video/webm|
|Enbart ljud av MIME-typ |audio/webm|
|Uniform Type Identifier| org.webmproject.webm|
|Video Codec Namn| VP8 eller VP9|
|Ljud Codec Namn| Vorbis eller Opus|

### WebM Elements

WebM, som är en delmängd av Matroska-specifikationerna, ger stöd för en del av Matroska-funktionaliteten. Följande är en beskrivning av de stödda elementen.

#### EBML

|Namn |Beskrivning|
---|---|
|EBML|Ställ in EBML-egenskaperna för data som följer. Varje EBML-dokument måste börja med detta.|
|EBMLVersion |Versionen av EBML-parsern som användes för att skapa filen.|
|EBMLReadVersion|Minsta EBML-version som en parser måste stödja för att läsa den här filen.|
|EBMLMaxIDLength |Den maximala längden på ID:n du hittar i den här filen (4 eller mindre i Matroska).|
|EBMLMaxSizeLength|Den maximala längden på storlekarna som du hittar i den här filen (8 eller mindre i Matroska). Detta åsidosätter inte elementstorleken som anges i början av ett element. Element som har en angiven storlek som är större än vad som tillåts av EBMLMaxSizeLength ska anses ogiltiga.|
|DocType|En sträng som beskriver typen av dokument som följer denna EBML-rubrik ("webm" i vårt fall).|
|DocTypeVersion|Versionen av DocType-tolken som användes för att skapa filen.|
|DocTypeReadVersion|Minsta DocType-version som en tolk måste stödja för att kunna läsa den här filen.|

#### Globala element

För tillfället stöds endast "Void"-elementet som används för att ogiltigförklara skadad data, för att undvika oväntade beteenden vid användning av skadad data. Innehållet kasseras. Används även för att reservera utrymme i ett delelement för senare användning.

#### Segmentet
Detta element innehåller alla andra element på toppnivå (nivå 1). Vanligtvis är en Matroska-fil sammansatt av ett segment.

#### Meta Sök information

Följande sökinformation stöds.

|Elementnamn |Beskrivning|
---|---|
|SeekHead |Innehåller positionen för ett annat nivå 1-element.|
|Seek |Innehåller en enda sökpost till ett EBML-element.|
|SeekID |Det binära ID som motsvarar elementnamnet.|
|SeekPosition |Placeringen av elementet i segmentet i oktetter (0 = första nivå 1 element).|

## Referenser

* [WebM](https://www.webmproject.org/)
* [WebM Code Repositories](https://www.webmproject.org/code/#webp-repositories)

