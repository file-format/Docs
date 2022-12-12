---
date: 2019-12-13
keywords: flac, format de fișier flac, extensie .flac, fișier flac, flac vs mp3
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Aflați despre formatul de fișier FLAC și despre API-urile care pot crea și deschide fișiere FLAC."
title: Format de fișier FLAC
linktitle: FLAC
menu:
  docs:
    parent: "audio"
lastmod: 2021-28-05
---

## Ce este un fișier FLAC?

FLAC (Free Lossless Audio Codec) este un format de codare audio cu compresie fără pierderi dezvoltat de Fundația Xiph.Org. FLAC este un format deschis fără drepturi de autor care este salvat cu extensia .flac. Audio digital comprimat folosind algoritmul FLAC este de obicei redus la 50 până la 70 la sută în dimensiune. Fișierele FLAC pot fi decomprimate într-o copie identică a fișierelor audio originale.

## Format fișier FLAC

Aceasta este o prezentare generală a fluxului de biți FLAC.

- **marker fLaC**: acest marcator este adăugat la începutul fluxului. Este urmată de unul sau mai multe blocuri de metadate.
- **Blocuri de metadate**: FLAC acceptă 128 de tipuri de blocuri de metadate; în prezent sunt definite următoarele.
  - **STREAMINFO**: Contains the information about the whole stream.
  - **APPLICATION**: This is used by third-party applications for identification.
  - **PADDING**: It is used to reserve space for metadata if the metadata will be edited after encoding. When the metadata is edited, the padding is replaced by the actual metadata.
  - **SEEKTABLE**: An optional table to store seek points.
  - **VORBIS_COMMENT**: Used to store human-readable key/value pairs.
  - **CUESHEET**: Used to store cue sheet information.
  - **PICTURE**: Used to store pictures.
- **FRAME**: Datele audio sunt compuse din unul sau mai multe cadre audio.
  - **FRAME_HEADER**: Contains the basic information about the stream.
  - **SUBFRAME**: To decrease the complexity, individual subframes are coded separately within a frame (one frame per channel).
  - **FRAME_FOOTER**: Contains the CRC of the complete frame.

## Scurt istoric al formatului de fișier FLAC

Josh Coalson a început dezvoltarea FLAC în 2000. Prima versiune a FLAC a fost lansată pe 20 iulie 2001. FLAC a fost încorporat sub steag Xiph.Org la 20 ianuarie 2003. Dezvoltarea FLAC a fost mutată în depozitul git Xiph.Org cu lansarea versiunii 1.3.0 pe 26 martie 2013.

## Componența proiectului FLAC

Proiectul FLAC constă în următoarele:

- Formate de flux.
- Format container simplu pentru flux (FLAC).
- libFLAC: O bibliotecă de codificatoare de referință, decodore și interfață de metadate.
- libFLAC++: un wrapper orientat pe obiecte pentru libFLAC.
- flac: un program de linie de comandă pentru a codifica și decoda fluxurile FLAC.
- metaflac: un editor de metadate de linie de comandă pentru FLAC.
- Pluginuri de intrare pentru playere muzicale precum Winamp, XMMX etc.
- Format container Ogg (Ogg FLAC).

## Design FLAC

În funcție de densitatea și amplitudinea muzicii, dimensiunea fișierului comprimat poate fi cu 80% mai mică decât fișierul original.

### Codificator sursă ###

- Acceptă doar eșantioane întregi și nu în virgulă mobilă. Poate gestiona rezoluția de biți PCM de la 4 la 32 de biți per probă și rata de eșantionare de la 1 Hz la 65.535 Hz. Codificarea FLAC este limitată la 24 de biți per probă.
- Canalele pot fi grupate pentru a profita de corelațiile intercanale pentru a crește compresia.
- Sumele de control CRC sunt folosite pentru a identifica cadrele corupte.
- Pentru conversia probelor audio, FLAC folosește predicția liniară.

### Metadate ###

- FLAC acceptă ReplayGain (folosit pentru a percepe și a normaliza zgomotul în audio).
- FLAC folosește același sistem folosit în comentariile Vorbis pentru etichetare.
- libFLAC este folosit de majoritatea aplicațiilor FLAC pentru codificare/decodare.
- libFLAC API este organizat în fluxuri, fluxuri căutate și fișiere pentru a crește abstracția din fluxul de biți FLAC de bază.

### Compresie ###

libFLAC folosește niveluri de compresie de la 0 la 8, unde 0 este cel mai rapid și 8 este cel mai lent nivel de compresie. Fișierele comprimate sunt întotdeauna fără pierderi, deși compromisul este între viteză și dimensiune.

## FLAC vs MP3
MP3 este un format de compresie cu pierderi, ceea ce înseamnă că poate tăia o parte din sunet pentru a-i reduce dimensiunea după aplicarea compresiei. În timp ce, FLAC este un format de fișier fără pierderi, ceea ce înseamnă că puteți auzi sunetul în forma sa cea mai pură. Anterior, formatele de fișiere fără pierderi erau CDA sau WAV, care nu erau foarte eficiente în spațiu ca FLAC. Următorul tabel va arăta comparația dintre aceste două formate pentru câțiva termeni importanți:

|Termen|FLAC|MP3|
---|---|---|
|**Calitatea datelor**|Fără pierderi de date audio| Unele date se pot pierde la comprimarea datelor audio|
|**Dimensiune**|Dimensiunea fișierului mai mare în comparație cu formatele cu pierderi. Deci nevoie de o capacitate de stocare mai mare| Dimensiune mai mică a fișierului, potrivită pentru redare pe dispozitive audio compacte cu spațiu de stocare redus |
|**Cerințe hardware**| Aveți nevoie de echipament audio de înaltă calitate și capacitate mare de stocare | Biblioteci audio uriașe pot fi salvate într-un spațiu de stocare mai mic. Potrivit pentru dispozitive portabile, cum ar fi playere audio sau telefoane mobile|
|**Distribuire pe internet**|Nu poate fi distribuit cu ușurință pe internet din cauza dimensiunii masive a fișierului |Dimensiunea compactă a fișierului facilitează distribuirea pe internet|
|**Compatibilitate**|Cel mai popular codec de ascultare muzicală și audio, aproape compatibil cu orice dispozitiv de pe planetă.Compatibil cu calculatoare, telefoane, receptoare AV, playere blu-ray, dispozitive de streaming precum Roku sau Fire TV de nouă generație |

## Referințe ##

- [FLAC - Wikipedia](https://en.wikipedia.org/wiki/FLAC)

