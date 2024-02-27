{
  "date": "2019-10-11",
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "title": "MKV filformat",
  "keywords": [
"mkv",
"matroska video",
"mkv format",
"hvordan man spiller mkv-filer",
"video",
"fil",
"format"
],
  "description": "Lær om MKV-filformat og API'er, der kan oprette og åbne MKV-filer.",
  "linktitle": "MKV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mk-dav"
}
},
  "lastmod": "2020-17-11"
}


## Hvad er en MKV-fil? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle track in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV is future-proof. These features include:

- Support til hurtig søgning.
- Mulighed for at vælge forskellige lyd- og videostreams.
- Understøttelse af undertekster (hard-coded og soft-coded).
- Understøttelse af metadata, kapitler og menuer.
- Mulighed for at streame online.
- Evne til at gendanne fejlagtige filer, der giver mulighed for at afspille beskadigede filer.

## Kort historie ##

MKV-fil opstod i 2002 i Rusland. Den ledende udvikler var Lasse Kärkkäinen, som arbejdede sammen med grundlæggeren af Matroska, Steve Lhomme, og et team af programmører. MKV er udviklet som et åbent standardprojekt, hvilket betyder, at det er open source og gratis at bruge. Som tiden gik, blev formatet forbedret og blev grundlaget for WebM multimedieformat i 2010.

## Matroska Design ##

Matroska tilføjer følgende begrænsninger til EBML-specifikationen.

- **EBML-headeren**s **docType** skal være 'matroska'.
- **EBML-headeren**s **EBMLMaxIDLength** skal være 4.
- **EBML Headeren**s **EBMLMaxSizeLength** skal være mellem 1 og 8 (inklusive).

Alle elementer på øverste niveau er kodet i 4 oktetter.

- Sprogkoder: Matroska (version 1 til 3) brugte sprogkoder, der enten kan være den bibliografiske ISO-639-2-form på 3 bogstaver (som fre for fransk), eller yderligere landekode kan bruges som fre-ca  for canadisk fransk. Fra Matroska version 4 KAN enten ISO 639-2 eller BCP 47 bruges til sprogkoder, selvom BCP 47 anbefales.
- Fysiske typer: Disse har forskellig betydning for både lyd- og videofiler. For eksempel betyder ChapterPhysicalEquiv = 60 (CD / 12 / 10 / 7 / TAPE / MINIDISC / DAT) for lyd og (DVD / VHS / LASERDISC) for video.
- Blokstruktur - Blokhoved: Blokhovedet indeholder information om spornummer, tidsstempler, snøretype osv.
- Snøring: Det er en mekanisme til at spare plads ved lagring af data, der typisk bruges til små datablokke (rammer). Der er 3 typer snøring:
  - "Xiph: Ramme med et størrelsesmultipel på 255 kodet med et 0 i slutningen af størrelsen. For eksempel er koden for 765 255;255;255;0."
  - "EBML: Rammestørrelsen er kodet som en forskel mellem den tidligere størrelse og denne størrelse. Den første størrelse i blonden er usigneret, men andre bruger et områdeskift for at få et tegn på hver værdi."
  - "fast størrelse: Størrelsen forbliver den samme."
- SimpleBlock Structure: Den er inspireret af **Blokstrukturen**, hvor den største forskel er tilføjelsen af **Keyframe** og **Discardable** flag. Bortset fra det er alt det samme.

## Matroska-struktur ##

Et Matroska-dokument skal bestå af mindst ét **EBML-dokument** ved brug af **Matroska-dokumenttypen**. Hvert **EBML-dokument** skal starte med en **EBML-header** efterfulgt af **EBML-rodelementet**, der er defineret som et segment. Matroska definerer flere Top-Level Elementer, der kan forekomme inden for **Segment**.

EBML bruger et system af elementer til at komponere et EBML-dokument. Følgende er listen over elementer på øverste niveau i Matroska-filen:

- **EBML-dokument**: Indpakning for hele filen.
- **EBML Header**: Den indeholder headeroplysninger for filen som DocType.
- **Segment**: Det øverste element, der indeholder alle andre elementer på øverste niveau.
- **SeekHead**: Det indeholder positionen for segmenter af andre elementer på øverste niveau.
- **Info**: Den indeholder generel information om segmentet.
- **Spor**: Et informationselement på øverste niveau med mange spor beskrevet.
- **Chapters**: It is used to define basic menus and partition data.
- **Klynge**: Top-Level Element, der indeholder blokstrukturen.
- **Cues**: Et element på øverste niveau, der indeholder alle indgange lokalt til segmentet, som fremskynder adgangssøgning.
- **Vedhæftede filer**: Dette indeholder vedhæftede filer.
- **Tags**: Dette element indeholder metadata, der beskriver spor, udgaver, kapitler, vedhæftede filer eller segmentet som helhed.

Følgende tabel viser strukturen af Matroska-dokumentet med de fleste af elementerne vist i et hierarki:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML Header | | | |
| Segment | SeekHead| Søg | Søg ID |
| | | | SeekPosition |
| | Info | SegmentUID | |
| | | SegmentFilnavn | |
| | | PrevUID | |
| | | Forrige Filnavn | |
| | | NextUID | |
| | | NæsteFilnavn | |
| | | SegmentFamilie | |
| | | Kapitel Oversæt | |
| | | TidsstempelSkala | |
| | | Varighed | |
| | | DatoUTC | |
| | | Titel | |
| | | MuxingApp | |
| | | Skriveapp | |
| | Spor | TrackEntry | Spornummer |
| | | | TrackUID |
| | | | TrackType |
| | | | Navn |
| | | | Sprog |
| | | | CodecID |
| | | | CodecPrivat |
| | | | Codecnavn |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHøjde |
| | | | | DisplayBredde |
| | | | | Displayhøjde |
| | | | | AspectRatioType |
| | | | | Farve |
| | | | Lyd | Sampling Frequency |
| | | | | Kanaler |
| | | | | BitDepth |
| | Kapitler | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | ChapterAtom | KapitelUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | KapitelFlagSkjult |
| | | | | Kapitelvisning | ChapString |
| | | | | | ChapLanguage |
| | Klynge | Tidsstempel |
| | | SilentTracks |
| | | Stilling |
| | | PrevSize |
| | | SimpleBlock |
| | | Blokgruppe |
| | | Krypteret blok |
| | Stikord | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Vedhæftede filer | Vedhæftet fil | Filbeskrivelse |
| | | | Filnavn |
| | | | FileMimeType |
| | | | FileUID |
| | | | Filhenvisning |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Tags | Tag | Mål | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | Tagnavn |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### Brug af codecs ###

Hvis du ikke vil have en ny medieafspiller og foretrækker at bruge din eksisterende afspiller, skal du installere nogle codecs (forkortelse for komprimering/dekompression). Selvom det er en gyldig mulighed at downloade codecs, bør du være forsigtig med kilden, og disse kan indeholde malware.

## Referencer ##

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)

