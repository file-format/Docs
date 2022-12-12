---
date: 2019-10-11
keywords: flv, .flv, format de fișier flv, format de fișier .flv, extensie .flv, extensie flv, format video flv
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier FLV și despre API-urile care pot crea și deschide fișiere FLV."
title: Format de fișier FLV
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## Ce este un fișier FLV? ##

FLV (Flash Video) este un format de fișier container cu extensia .flv. FLV este folosit pentru a livra conținut audio/video pe internet folosind Adobe Flash Player sau Adobe Air. Datele din fișierele FLV sunt codificate în același mod ca și fișierele SWF. Suportul direct a fost adăugat la Flash Player 7 în 2003. Sistemele Adobe au creat F4V în 2007 din cauza restricțiilor FLV.

### Codificare ###

Fișierele FLV conțin fluxuri de biți video ale Sorenson Spark, care sunt o variantă proprietară a standardului video H.263. Este formatul de compresie necesar pentru Flash Player 6 și 7. Versiunea 8 a Flash Player suportă fluxurile de biți video On2 TrueMotion VP6. Este formatul de compresie recomandat pentru Flash Player 8 și versiuni ulterioare. FLV acceptă audio în MP3, codecul Nellymoser Asao și codecul Speex cu sursă deschisă. De asemenea, acceptă audio necomprimat sau audio în format ADPCM. AAC (HE-AAC/AAC SBR, AAC Main Profile și AAC-LC) sunt acceptate de versiunile recente de Flash Player 9.

## Structura ##

Fișierele FLV constau din antet și pachete. Un fișier FLV începe cu antetul. Antetul are următoarele câmpuri.

- **Semnătura**: valoarea sa este FLV
- **Versiune**: valoarea sa implicită este 1. Doar 0x01 este valid.
- **Flags**: 0x04 este folosit pentru audio și 0x01 este folosit pentru video, așa că 0x05 este folosit atât pentru audio, cât și pentru video.
- **Dimensiune antet**: valoarea implicită este 9. Este folosită pentru a omite un antet extins mai nou.

După antet vin Pachetele. Fișierul FLV este împărțit în mai multe pachete numite etichete FLV care au antete de 15 octeți. Pachetele conțin metadatele pentru audio, video, scripturi, informații de criptare și încărcătură utilă. Pachetele FLV au următoarele câmpuri.

- **Rezervat**: este rezervat pentru FMS și ar trebui să fie 0.
- **Filtru**: indică dacă pachetele sunt filtrate sau nu.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Tipul pachet**: Acesta definește tipul de conținut din pachet.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Dimensiunea datelor**: Aceasta denotă lungimea mesajului.
- **Timestamp Lower**: Aceasta stochează marcajul de timp în milisecunde la care se aplică datele etichetei. Este setat la NULL pentru primul pachet.
- **Timestamp Upper**: Extensie pentru a crea o valoare uint32_be.
- **ID flux**: Acesta este setat la NULL pentru primul flux.
- **Payload Data**: Acestea sunt datele bazate pe tipul de pachet.

## Referințe ##

- [Flash Video - Wikipedia](https://en.wikipedia.org/wiki/Flash_Video)

