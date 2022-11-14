---
date: 2019-10-11
keywords: f4v, .f4v, f4v bestandsformaat, .f4v bestandsformaat, .f4v extensie, f4v extensie, f4v videoformaat, hoe f4v-bestanden te openen, wat zijn f4v-bestanden
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Meer informatie over de F4V-bestandsindeling en API's die F4V-bestanden kunnen maken en openen"
title: F4V-bestandsindeling
linktitle: F4V
menu:
  docs:
    parent: "video"
lastmod: 2020-10-12
---

## Wat is een F4V-bestand? ##

F4V (Flash MP4-videobestand) is een videobestand dat is opgeslagen met de extensie .f4v. Het is gebaseerd op het ISO-basismediabestandsformaat (MPEG-4 Part 12). Het lijkt erg op [MP4](/nl/video/mp4/) en daarom wordt het informeel ook wel Flash MP4 genoemd. [FLV](/nl/video/flv/) had beperkingen bij het streamen van H.264/ACC-inhoud, wat ertoe leidde dat Adobe Systems het nieuwe F4V-formaat creëerde. Flash Player kan F4V-bestanden afspelen sinds de release van Flash Player 9 Update 3.

## Structuur van F4V-bestanden ##

Het F4V-bestandsformaat is gebaseerd op het ISO-basismediabestandsformaat (MPEG-4 Part 12) en lijkt erg op het MP4-formaat. Zie de [MP4](/nl/video/mp4/) pagina voor details over de structuur. Het grote verschil tussen F4V en MP4 zijn de metadataformaten die F4V kan opslaan. Hieronder vindt u de lijst met metadataformaten die worden ondersteund door het F4V-formaat.

- **Tagbox**: extra vier optionele tagboxen (auth, title, dscp, cprt) in de Movie (moov) box.
- **XMP Metadata-box**: deze box komt direct na de Movie (moov) box. Hiermee kan het bestand via ActionScript XMP-metadata doorgeven aan een SWF-film.
- **ilst box**: deze box komt voor in de Meta (meta) box en kan een aantal metadata tags bevatten. De ondersteunde gegevenstypen worden hieronder gegeven.
  - **0**: Custom Data.
  - **1**: Text Data.
  - **12, 14**: Binary Data
  - **21**: Generic Data.
- **Text Track Metadata-box**: de tekstvoorbeelden (tekst of tx3g) in de Media Databox (mdat). Het kan de volgende metadatavakken bevatten.
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

## Referenties ##

- [Flash-video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

