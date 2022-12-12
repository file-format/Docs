---
date: 2019-10-11
keywords: f4v, .f4v, format de fișier f4v, format de fișier .f4v, extensie .f4v, extensie f4v, format video f4v, cum se deschide fișierele f4v, ce sunt fișierele f4v
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier F4V și despre API-urile care pot crea și deschide fișiere F4V"
title: Format de fișier F4V
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Ce este un fișier F4V? ##

F4V (Flash MP4 Video File) este un fișier video salvat cu extensia .f4v. Se bazează pe formatul de fișier media de bază ISO (MPEG-4 Partea 12). Este foarte asemănător cu [MP4](/ro/video/mp4/), motiv pentru care este denumit și Flash MP4 în mod informal. [FLV](/ro/video/flv/) a avut limitări la transmiterea în flux a conținutului H.264/ACC, ceea ce a dus la crearea de către Adobe Systems a noului format F4V. Flash Player poate reda fișiere F4V de la lansarea Flash Player 9 Update 3.

## Structura fișierelor F4V ##

Formatul de fișier F4V se bazează pe formatul de fișier media de bază ISO (MPEG-4 Partea 12) și este foarte asemănător cu formatul MP4. Pentru detalii privind structura, vă rugăm să consultați pagina [MP4](/ro/video/mp4/). Diferența majoră dintre F4V și MP4 este formatele de metadate pe care F4V le poate stoca. Mai jos este lista formatelor de metadate acceptate de formatul F4V.

- **Casută de etichete**: patru casete suplimentare de etichete opționale (auth, title, dscp, cprt) în caseta Film (moov).
- **Casa metadate XMP**: această casetă vine imediat după caseta Film (moov). Prin aceasta, fișierul poate comunica metadatele XMP unui film SWF prin ActionScript.
- **casuta ilst**: această casetă apare în interiorul casetei Meta (meta) și poate conține un număr de etichete de metadate. Tipurile de date acceptate sunt prezentate mai jos.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Caseta de metadate a urmăririi textului**: eșantioanele de text (text sau tx3g) din caseta de date media (mdat). Poate conține următoarele casete de metadate.
  - **Style box**: Text style specifications.
  - **Highlight box**: Specifies the range of text to be highlighted.
  - **Highlight Color box**: Specifies the highlight color for the text.
  - **Karaoke box**: Specified the karaoke metadata.
  - **Scroll Delay box**: Specifies the scroll delay.
  - **Drop Shadow Offset box**: Specifies the drop shadow offset coordinates for the text.
  - **Drop Shadow Alpha box**: Specifies the drop shadow alpha value for the text.
  - **Hypertext box**: Specifies the hypertext text with alt text over a text range.
  - **Text Box box**: Defines the coordinates for the text box.
  - **Blinking box**: Specifies blinking for a range of text.
  - **Text Wrap box**: Sets the text wrap flag for the text.
  - **Text Wrap box**: Sets the text wrap flag for the text.

## Referințe ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

