---
date: 2022-03-20
keywords: mxl, Musepack fájlformátum, .mxl kiterjesztésű
szerző:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Ismerje meg az MXL fájlformátumot és az API-kat, amelyek MXL fájlokat hozhatnak létre és nyithatnak meg."
title: MXL fájlformátum - Tömörített zeneXML fájl
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Mi az MXL fájl?

Az MXL fájl a MusicXML fájlformátum tömörített formája, amely nyílt szabványos formátum a digitális kottacseréhez. Az egyszerű szöveges MusicXML fájlok nagy méretűek, és a nagy fájlméret befolyásolta az ilyen fájlok lapterjesztési formátumként való használatát. Ezt a problémát a [MusicXML](https://www.musicxml.com/) 2.0-val kezeltük az MXL fájlformátum bevezetésével, amely eléggé tömöríti a fájlokat ahhoz, hogy az eredeti MIDI-fájlok méretéhez hasonlóan csökkentse a fájlméretet. Az MXL-fájlokhoz ajánlott médiatípus: application/vnd.recordare.musicxml.

## MXL fájlformátum

Az MXL-fájlok [ZIP](/hu/compression/zip/) tömörített [XML](/hu/web/xml/) fájlokként vannak tárolva .mxl fájlkiterjesztéssel. Az MXL-fájlok tömörítése az [RFC 1951]-ben (https://www.ietf.org/rfc/rfc1951.txt) meghatározott DEFLATE algoritmussal történik.

### MXL fájlstruktúra

Minden MXL-fájl ZIP-alapú XML-formátummal rendelkezik, amelynek tartalmaznia kell egy META-INF/container.xml fájlt, amely leírja a fájl MusicXML-verziójának kiindulópontját. Az MXL fájlformátumhoz nincs definiálva megfelelő .xsd fájl.

Egy egyszerű container.xml fájl tartalma a következő. Ez a példa a MakeMusic webhelyén elérhető Dichterliebe01.mxl fájlból származik.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Ebben a példában a<container> elem a dokumentumelem. Az<rootfiles> elem tartalmazhat egyet vagy többet<rootfile> elemekkel, az elsővel<rootfile> elem, amely leírja a MusicXML gyökerét. A MusicXML fájl, amelyet a<rootfile> lehet<score-partwise> ,<score-timewise> , vagy<opus> dokumentumelemeként.

## Hivatkozások

* [Tömörített MXL-fájlok](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

