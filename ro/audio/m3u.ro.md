---
date: 2019-12-13
keywords: m3u, format de fișier m3u, extensie .m3u, listă de redare multimedia m3u, format de listă de redare m3u
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier M3U și despre API-urile care pot crea și deschide fișiere M3U."
title: Format de fișier M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Ce este un fișier M3U? ##

M3U (MP3 URL) este un fișier de listă de redare audio stocat cu extensia .m3u. M3U nu este un fișier audio real, ci doar indică fișiere audio și uneori video. M3U a fost dezvoltat pentru a fi utilizat cu software-ul Winplay3 de Fraunhofer. De asemenea, este acceptat de diverse playere media și software.

## Format de fișier M3U

Nu există o specificație oficială pentru formatul de fișier M3U, este un standard de facto. M3U este un fișier text simplu care utilizează extensia .m3u dacă textul este codificat în codificarea implicită non-Unicode a sistemului local sau cu extensia .m3u8 dacă textul este codificat UTF-8. Fiecare intrare din fișierul M3U poate fi una dintre următoarele:

- Calea absolută către fișier
- Calea fișierului în raport cu fișierul M3U.
- URL

### M3U extins ###

În M3U extins, sunt introduse directive suplimentare care încep cu „#” și se termină cu două puncte (:) dacă au parametri. Mai jos este o listă de directive pentru M3U extins.

- **#EXTM3U** - Este antetul fișierului care indică M3U extins și trebuie să fie prima linie a fișierului.
- **#EXTENC:** - Codificarea textului. Trebuie să fie a doua linie a fișierului.
- **#EXTINF:** - Folosit pentru informații despre piesă și alte proprietăți suplimentare.
- **#PLAYLIST:** - Titlul listei de redare
- **#EXTGRP:** - Începeți gruparea numelor
- **#EXTALB:** - Informații despre album
- **#EXTART:** - Artist album
- **#EXTGENRE** - Genul albumului
- **#EXTM3A** - Lista de redare cu un singur fișier pentru melodiile sau capitolele albumului.
- **#EXTBYT:** - Dimensiunea fișierului în octeți.
- **#EXTBIN:** - Urmează date binare.
- **#EXTIMG:** - Logo, Copertă sau alte imagini.

### HLS M3U ###

HLS (HTTP Live Streaming) a fost creat de Apple pentru a transmite audio și radio pe dispozitivele iOS. Se bazează pe M3U extins codificat UTF-8. A fost standardizat ca RFC 8216 în 2017 de IETF. Etichetele pentru lista de redare HLS încep cu „#EXT-X-”. Mai jos este o listă de etichete pentru HLS

- **EXT-X-VERSION** - Indică versiunea de compatibilitate a fișierului pe baza media și a serverului acestuia.
- **#EXT-X-START:** - Indică punctul de pornire preferat pentru lista de redare.
- **#EXT-X-PLAYLIST-TYPE:** - Oferă tipul de playlist (EVENT sau VOD).
- **#EXT-X-TARGETDURATION:** - Specifică durata maximă a Segmentului.
- **#EXT-X-MEDIA-SEQUENCE:** - Indică numărul de secvență media.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Indică faptul că toate mostrele media sunt independente și pot fi decodificate fără alte segmente.
- **#EXT-X-MEDIA:** - Este folosit pentru a lega liste de redare media care conțin redări alternative ale aceluiași conținut.
- **#EXT-X-STREAM-INF:** - Specifică un flux de variante care face parte din redări.
- **#EXT-X-BYTERANGE:** - Indică faptul că Segmentul Media este un sub-gamă al resursei identificate prin URI-ul său.
- **#EXT-X-DISCONTINUITY** - Indică discontinuitate între segmentele media precedente și următoare.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Permite sincronizarea între diferite redări ale aceluiași Flux Variant sau diferite Fluxuri Variante.
- **#EXT-X-KEY:** - Specifică modul de decriptare a segmentelor media.
- **#EXT-X-MAP:** - Specifică modul de obținere a secțiunii de inițializare media. Este necesar să analizați segmentele media aplicabile.
- **#EXT-X-PROGRAM-DATE-TIME:** - Asociază primul eșantion al Segmentului Media cu o dată și/sau oră absolută.
- **#EXT-X-DATERANGE:** - Asociază un interval de date.
- **#EXT-XI-FRAMES-ONLY** - Indică faptul că fiecare segment media din lista de redare descrie un singur cadru I.
- **EXT-XI-FRAME-STREAM-INF** - Indică faptul că fișierul playlist conține cadre I ale prezentării multimedia.
- **#EXT-X-SESSION-DATA:** - Permite date arbitrare ale sesiunii
incluse într-o listă de redare principală.
- **#EXT-X-SESSION-KEY:** - Permite chei de criptare. Clientul poate preîncărca aceste taste fără a citi mai întâi lista de redare.
- **#EXT-X-ENDLIST** - Indică faptul că nu vor fi adăugate alte segmente media la fișier.

Următoarea este lista de tipuri de media pe Internet utilizate de M3U:

- **application/vnd.apple.mpegurl**: este singurul tip media înregistrat (înregistrat în 2009) pentru M3U care este folosit pentru a se referi la listele de redare din aplicațiile HLS.
- Următoarele tipuri de media Internet sunt utilizate de aplicațiile non-HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Exemplu M3U ##

Acesta este un exemplu de fișier M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Referințe ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Streaming live HTTP](https://tools.ietf.org/html/rfc8216)

