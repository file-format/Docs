{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV-filformat",
  "keywords" :[ "mkv", "matroska video", "mkv-format", "hur man spelar upp mkv-filer", "video", "fil", "format" ],
  "description":"Läs mer om MKV-filformat och API:er som kan skapa och öppna MKV-filer.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Vad är en MKV-fil? ##

MKV (Matroska Video) är en multimediabehållare som liknar formaten [MOV](/sv/video/mov/) och [AVI](/sv/video/avi/) men den stöder mer än ett ljud- och undertextspår i samma fil. En MKV-fil är Matroskas multimediacontainerformat som används för video. MKV är baserat på Extensible Binary Meta Language och det stöder flera video- och ljudkomprimeringsformat. Den stora skillnaden mellan MKV och andra videoformat är att MKV är en behållare och inte en codec. MKV-filer sparas med filtillägget .mkv. MKV kan inkludera ljud, video och undertexter i en enda fil även om dessa element använder olika typer av kodning. Du kan till exempel ha en MKV-fil som innehåller H.264-video och MP3 eller AAC för ljud. MKV stöder också beskrivningar, betyg, omslagsbilder och till och med kapitelpunkter. Det finns flera nyckelfunktioner som MKV är framtidssäker. Dessa funktioner inkluderar:

- Stöd för snabbsökning.
- Möjlighet att välja olika ljud- och videoströmmar.
- Stöd för undertexter (hårdkodad och mjukkodad).
- Stöd för metadata, kapitel och menyer.
- Möjlighet att streama online.
- Möjlighet att återställa felaktiga filer som ger möjlighet att spela upp skadade filer.

## Kortfattad bakgrund ##

MKV-filen har sitt ursprung 2002 i Ryssland. Huvudutvecklaren var Lasse Kärkkäinen som arbetade med grundaren av Matroska, Steve Lhomme, och ett team av programmerare. MKV utvecklades som ett projekt med öppen standard, vilket innebär att det är öppen källkod och gratis att använda. Allt eftersom tiden gick förbättrades formatet och blev grunden för WebM multimediaformat 2010.

## Matroska Design ##

Matroska lägger till följande begränsningar till EBML-specifikationen.

- **EBML Header**s **docType** måste vara "matroska".
- **EBML Header**s **EBMLMaxIDLength** måste vara 4.
- **EBML Header**s **EBMLMaxSizeLength** måste vara mellan 1 och 8 (inklusive).

Alla element på toppnivå är kodade i 4 oktetter.

- Språkkoder: Matroska (version 1 till 3) använde språkkoder som kan vara antingen den bibliografiska ISO-639-2-formen med tre bokstäver (som "fre" för franska), eller ytterligare landskod kan användas som "fre-ca" " för kanadensisk franska. Från och med Matroska version 4 KAN antingen ISO 639-2 eller BCP 47 användas för språkkoder, även om BCP 47 rekommenderas.
- Fysiska typer: Dessa har olika betydelse för både ljud- och videofiler. Till exempel betyder ChapterPhysicalEquiv = 60 (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) för ljud och (DVD / VHS / LASERDISC) för video.
- Blockstruktur - Blockhuvud: Blockhuvud innehåller information om spårnummer, tidsstämplar, typ av snörning, etc.
- Snörning: Det är en mekanism för att spara utrymme vid lagring av data som vanligtvis används för små datablock (ramar). Det finns 3 typer av snörning:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Structure: Den är inspirerad av **Blockstrukturen** med den största skillnaden är tillägget av **Keyframe** och **Discardable**-flaggor. Förutom det är allt sig likt.

## Matroska-struktur ##

Ett Matroska-dokument måste bestå av minst ett **EBML-dokument** med **Matroska Document Type**. Varje **EBML-dokument** måste börja med en **EBML-rubrik** följt av **EBML-rotelementet** som definieras som ett segment. Matroska definierar flera toppnivåelement som kan förekomma inom **segmentet**.

EBML använder ett system av element för att skapa ett EBML-dokument. Följande är listan över element på toppnivå i Matroska-filen:

- **EBML-dokument**: Omslag för hela filen.
- **EBML Header**: Den innehåller rubrikinformationen för filen som DocType.
- **Segment**: Det översta elementet som innehåller alla andra toppnivåelement.
- **SeekHead**: Den innehåller positionen för segment av andra toppnivåelement.
- **Info**: Den innehåller allmän information om segmentet.
- **Spår**: Ett informationselement på toppnivå med många beskrivna spår.
- **Kapitel**: Det används för att definiera grundläggande menyer och partitionsdata.
- **Kluster**: Toppnivåelementet som innehåller blockstrukturen.
- **Cues**: Ett element på toppnivå som innehåller alla poster som är lokala för segmentet som snabbar upp söker åtkomst.
- **Bilagor**: Detta innehåller bifogade filer.
- **Taggar**: Detta element innehåller metadata som beskriver spår, upplagor, kapitel, bilagor eller segmentet som helhet.

Följande tabell visar strukturen för Matroska-dokumentet med de flesta av elementen som visas i en hierarki:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML Header | | | |
| Segment | SeekHead| Sök | SökID |
| | | | SeekPosition |
| | Info | SegmentUID | |
| | | SegmentFilnamn | |
| | | PrevUID | |
| | | FöregåendeFilnamn | |
| | | NextUID | |
| | | NästaFilnamn | |
| | | SegmentFamilj | |
| | | KapitelÖversätt | |
| | | Tidsstämpelskala | |
| | | Varaktighet | |
| | | DatumUTC | |
| | | Titel | |
| | | MuxingApp | |
| | | WritingApp | |
| | Spår | TrackEntry | Spårnummer |
| | | | TrackUID |
| | | | TrackType |
| | | | Namn |
| | | | Språk |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | FlagInterlaced |
| | | | | Fältorder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Färg |
| | | | Ljud | Samplingsfrekvens |
| | | | | Kanaler |
| | | | | BitDepth |
| | Kapitel | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapterFlagDold |
| | | | | Chapter Display | ChapString |
| | | | | | ChapLanguage |
| | Kluster | Tidsstämpel |
| | | SilentTracks |
| | | Position |
| | | Föregående Storlek |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Ledtrådar | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Bilagor | Bifogad fil | Filbeskrivning |
| | | | Filnamn |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Taggar | Tagga | Mål | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### Använda codecs ###

Om du inte vill ha en ny mediaspelare och föredrar att använda din befintliga spelare, måste du installera några codecs (shorthand för komprimering/dekompression). Även om nedladdning av codecs är ett giltigt alternativ bör du vara försiktig med källan och dessa kan innehålla skadlig programvara.

## Referenser ##

- [Matroska av Wikipedia](https://en.wikipedia.org/wiki/Matroska)

