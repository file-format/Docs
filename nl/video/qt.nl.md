{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT-bestandsindeling - Quick Movie-bestand",
  "keywords" :[ "QT", "QuickTime-video", "qt-formaat", "hoe qt-bestanden af te spelen", "Quick Movie File", "QTFF", "video", "Apple"],
  "description":"Meer informatie over QT-bestandsindeling en API's die QT-bestanden kunnen maken en openen.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Wat is een QT-bestand?

Een bestand met de extensie .qt is een multimediacontainerbestand dat door het QuickTime-framework wordt gebruikt om de inhoud van multimediabestanden op te slaan. Het QuickTime-bestandsformaat (QTFF) is ontwikkeld door Apple Inc. en is een multimedia-containerbestand dat audio, video of tekst bevat om later af te spelen. Het is het formaat bij uitstek voor de uitwisseling van digitale media tussen apparaten, applicaties en besturingssystemen. QT-bestanden worden ook opgeslagen in de [MOV](/nl/video/mov/)-indeling die ook is ontwikkeld door Apple Inc. Sommige van de toepassingen die QT-bestanden kunnen openen, zijn Apple QuickTime-speler, VLC-mediaspeler en Media Player Classic met K- Lite Codec-pakket.

## QT-bestandsindeling

De QTFF is objectgeoriënteerd en biedt een flexibele verzameling objecten voor gemakkelijke ontleding en uitbreiding. Elke track in een QT-bestand bevat een digitaal gecodeerde mediastream of een gegevensverwijzing naar de mediastream in een ander bestand. De hiërarchische gegevensstructuur die bestaat uit objecten die atomen worden genoemd, fungeert als sporencontainers. Bestandsformaatspecificaties voor [QT-bestandsformaat](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) zijn officieel beschikbaar door Apple Inc ter referentie van de ontwikkelaar.

### Mediabeschrijving

De mediabeschrijving van een QuickTime-bestand wordt apart van de mediagegevens opgeslagen. Informatie zoals het aantal tracks, het videocompressieformaat en timinginformatie wordt opgeslagen in de mediabeschrijving (ook bekend als filmbron, filmatoom of gewoon de film). In deze mediastructuur wordt naar de mediagegevens verwezen door een index. De mediagegevens zijn de daadwerkelijke voorbeeldgegevens, zoals videoframes en audiomonsters, die in de film worden gebruikt.

### Atomen

Atom is de basiseenheid van het QuickTime-bestand. Er zijn twee belangrijke velden in elk atoom vóór elk ander veld: de velden Grootte en Type. Het grootteveld toont de grootte van het atoom, terwijl het typeveld het type gegevens aangeeft dat in het atoom is opgeslagen. Van nature zijn atomen hiërarchisch, wat betekent dat één atoom andere atomen kan bevatten die nog andere kunnen bevatten. De lay-out van een voorbeeldatoom wordt weergegeven in de volgende afbeelding.

Elk atoom heeft twee delen, koptekst en gegevens. De koptekst bevat de velden voor grootte en type en het gegevensgedeelte bevat de werkelijke gegevens. Verder wordt elk veld hieronder uitgelegd:

#### Atoomgrootte

De kop en inhoud van het atoom worden aangegeven door een 32-bits geheel getal dat bekend staat als de grootte van het atoom. Het veld size bevat de grootte van het atoom in bytes, uitgedrukt in een 32-bits geheel getal zonder teken.

#### Atoomtype

Het type atoom wordt ook weergegeven door een 32-bits geheel getal, dat meestal wordt behandeld als een veld van vier tekens met een knemonische waarde, zoals 'moov' (0x6D6F6F76) voor een filmatoom, of 'trak' (0x7472616B) voor een spooratoom. Zodra het atoomtype bekend is, kunnen de gegevens ervan worden geïnterpreteerd.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Bestandsstructuur ##

QT/MOV-bestanden bestaan uit opeenvolgende brokken. Elke chunk heeft een header van 8 bytes: een chunkgrootte van 4 bytes (big-endian, eerst high-byte) en een chunktype van 4 bytes - een van de vooraf gedefinieerde handtekeningen: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Het eerste blok is van het type "ftype" en heeft een subtype op offset 8. MOV gedefinieerd door het subtype dat "qt" moet zijn. Om een MOV-bestand samen te stellen, zijn itererende chunks nodig totdat een onbekend type wordt gedetecteerd.

Hier is een voorbeeldvoorbeeld: Bij het inspecteren van de binaire gegevens van een voorbeeld MOV-bestand is het duidelijk dat het begint met een handtekening **ftyp** (hex: 66 74 79 70) op offset 4, die het QuickTime-containerbestandstype definieert. Het bestandssubtype is **qt~_~_** (hex: 71 74 20 20) wat verwijst naar het MOV-bestandstype. De eerste blokgrootte is 32 (hex: 00 00 00 20, big-endian, high byte first), grootte bevindt zich op offset 0. Bij offset 32 (hex: 20) bevindt zich de tweede chunk, die een grootte heeft van 8 en typ **mdat** (hex: 6D 64 61 74).

De volgende chunk bevindt zich op offset 32+8#40 (hex: 28) en heeft een grootte van 3.263.028 (hex: 00 31 CA 34) en type **mdat** (hex: 6D 64 61 74) op offset 44 (hex : 2C). De volgende chunk bevindt zich op offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) en heeft een maat 21.189 (hex: 00 00 52 C5) en type **moov** (hex: 6D 6F 6F 76) op offset 1.836.019.574 (hex: 00 31 CA 60). Dit is het laatste stuk, dus de totale bestandsgrootte is 3.263.068+21.189#3.284.257 bytes.

## Referenties ##

* [QT-bestandsindeling - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [QuickTime-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

