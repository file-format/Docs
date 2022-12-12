---
date: 2022-01-06
keywords: vtt, .vtt, formát souboru vtt, formát souboru .vtt, přípona .vtt, přípona vtt
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Přečtěte si o souboru .vtt a rozhraních API, která mohou vytvářet a otevírat soubory VTT."
title: Formát souboru VTT - Web Video Text Tracks File
linktitle: VTT
menu:
  docs:
    identifier: "video-vtt"
    parent: "video"
lastmod: 2022-01-06
---

## Co je soubor VTT?

Soubor VTT je textový soubor, který obsahuje informace pro zobrazení časovaných textových stop (jako jsou titulky nebo titulky) pomocí formátu WebVTT (Web Video Text Tracks). Časované textové stopy obsahují informace, jako jsou titulky nebo titulky. Účelem souboru VTT je přidat textové překryvy do a<video> . Formát je poněkud podobný souborům SRT. Textové soubory založené na WebVTT jsou kódovány pomocí UTF-8. Soubor VTT obsahuje informace, jako jsou titulky, popisy, titulky, popisy, kapitoly a metadata. Jako prosté textové soubory lze soubory VTT otevřít pomocí textových editorů, jako je Microsoft Notepad, Apple TextEdit a Notepad++.

## Formát souboru VTT – Další informace

Soubory VTT používají formát souboru WebVTT pro ukládání informací o sekvenčních textových stopách. Každá stopa s časovaným textem se skládá z jednoho řádku nebo více řádků, které se také nazývají „narážka“, jak ukazuje následující příklad.

### Příklad souboru VTT

```
WEBVTT

00:01.000 --> 00:04.500
- Winters come after Autumn.

00:05.000 --> 00:10.000
- Often the weather goes too cold in winter.
- You should cover yourself with warm clothes.
```

### Struktura souborů VTT

Níže jsou uvedeny požadavky na strukturu souboru VTT.

* Volitelná značka pořadí bajtů (BOM).
* Řetězec "WEBVTT".
* Volitelné textové záhlaví napravo od WEBVTT.
* Prázdný řádek, který odpovídá dvěma po sobě jdoucím novým řádkům.
* Žádné nebo více podnětů nebo komentářů.
* Žádný nebo více prázdných řádků.

## Reference

* [VTT – školy W3](https://www.w3.org/TR/webvtt1/)
* [WebVTT – Mozilla](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)

