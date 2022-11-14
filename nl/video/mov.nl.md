{
  "date" : "2019-10-11",
  "keywords" :[ "mov-bestand", "mov-bestandsindeling", "wat is een mov-bestand", "bestand", "mov-voorbeeld", "mov-bestandsextensie", "extensie", "formaat", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV-bestand - Apple QuickTime-filmbestandsindeling",
  "description":"Meer informatie over MOV-bestandsindelingen en API's die MOV-bestanden kunnen maken en openen.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Wat is een MOV-bestand?

Een MOV-bestand is een videobestandstype, ontwikkeld door Apple Inc., dat een of meer tracks bevat. Elke track slaat een film, audio, filmclips en ondertitels op. Het is een multimediacontainer die verschillende soorten media-elementen kan opslaan. MOV-videoformaat is compatibel met zowel Windows- als Macintosh-systemen. Het maakt gebruik van MPEG-4 gecodeerd voor compressie en sporen worden onderhouden in objecten die atomen worden genoemd en die in een hiërarchische gegevensstructuur zijn geplaatst.

## Korte geschiedenis van MOV-bestandsindeling

Het MPEG-4-bestandsformaat is in 2001 geëvolueerd van de QuickTime File Format (**QTFF**)-specificatie. De International Organization of Standardization keurde het formaat goed en de MPEG-4 Part 1-systeemspecificaties werden in 1999 gepubliceerd. In 2001 werd een revisiebestand formaat [MP4](/nl/video/mp4/) is gepubliceerd.

De eerste versie van MP4 werd in 2003 herzien als MPEG-4 Part 14 (ISO/IEC 14496-14:2003). In 2004 werd MP4 veralgemeend om een algemene structuur te definiëren voor alle op tijd gebaseerde mediabestanden. Daarom wordt het nu gebruikt als basis voor verschillende andere multimediabestandsindelingen.

## QuickTime-bestandsindeling (QTFF) - Meer informatie

Om met digitale multimedia te kunnen werken, kan QTFF vele soorten gegevens bevatten. Het is een ideeformaat voor de uitwisseling van digitale media, aangezien het formaat de standaarden definieert voor het beschrijven van alle soorten mediastructuren. Het bestandsformaat bestaat uit een flexibele verzameling objectgeoriënteerde objecten. Voor de opslag van films op schijven gebruikt QuickTime twee structuren, namelijk `atoms` en `QT atoms`.

### Atomen

Atom is de basiseenheid van het QuickTime-bestand. Er zijn twee belangrijke velden in elk atoom vóór elk ander veld: de velden Grootte en Type. Het grootteveld toont de grootte van het atoom, terwijl het typeveld het type gegevens aangeeft dat in het atoom is opgeslagen. Van nature zijn atomen hiërarchisch, wat betekent dat één atoom andere atomen kan bevatten die nog andere kunnen bevatten. De lay-out van een voorbeeldatoom wordt weergegeven in de volgende afbeelding.

Elk atoom bestaat uit twee delen, 'header' en 'data'. De koptekst bevat de velden voor grootte en type en het gegevensgedeelte bevat de werkelijke gegevens. Verder wordt elk veld hieronder uitgelegd:

### Atoomgrootte

De kop en inhoud van het atoom worden aangegeven door een 32-bits geheel getal dat bekend staat als de grootte van het atoom. Het veld size bevat de grootte van het atoom in bytes, uitgedrukt in een 32-bits geheel getal zonder teken.

### Atoomtype

Het type atoom wordt ook weergegeven door een 32-bits geheel getal, dat meestal wordt behandeld als een veld van vier tekens met een knemonische waarde, zoals 'moov' (0x6D6F6F76) voor een filmatoom, of 'trak' (0x7472616B) voor een spooratoom. Zodra het atoomtype bekend is, kunnen de gegevens ervan worden geïnterpreteerd.

### QT-atomen en atoomcontainers

QT-atomen bieden een opslagformaat voor algemene doeleinden en hebben een uitgebreide header die bestaat uit de velden Grootte, Type, Atom-ID en Aantal onderliggende atomen. QT-atomen zijn verpakt in een atoomcontainer, een unieke gegevensstructuur met een kop met een slottelling. Er is één wortelatoom in elke atoomcontainer, het QT-atoom. De lay-out van het QT-atoom wordt weergegeven in de onderstaande afbeelding.

QT atom container header heeft de volgende gegevens:

Gereserveerd: Een element van 10 bytes met een waarde van 0.

Lock Count: 16-bits geheel getal met een waarde van 0.

QT-atoomheaders hebben de volgende gegevens:

**Grootte -** QT-atoomkop en inhoud worden aangegeven in bytes door een 32-bits geheel getal. In het geval van een bladatoom bevat dit veld de grootte van een enkel atoom.

**Type -** Het type atoom wordt aangegeven door een 32-bits geheel getal. Als het het wortelatoom is, wordt de waarde ingesteld op 'sean'.

**Atom ID -** Het is een 32-bits geheel getal dat de atoom-ID toont en uniek moet zijn voor alle broers en zussen. Wortelatoom altijd de waarde van atoom-ID als 1.

**Gereserveerd -** Een 16-bits geheel getal dat moet worden ingesteld op 0.

**Child count -** Een 16-bits geheel getal dat het aantal onderliggende atomen van een atoom aangeeft.

**Gereserveerd -** Een 32-bits geheel getal dat moet worden ingesteld op 0.

## Bestandsstructuur van MOV-bestanden

MOV-bestanden bestaan uit opeenvolgende brokken. Elke chunk heeft een header van 8 bytes: een chunkgrootte van 4 bytes (big-endian, eerst high-byte) en een chunktype van 4 bytes - een van de vooraf gedefinieerde handtekeningen: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Het eerste blok is van het type "ftype" en heeft een subtype op offset 8. MOV gedefinieerd door het subtype dat "qt" moet zijn. Om een MOV-bestand samen te stellen, zijn itererende chunks nodig totdat een onbekend type wordt gedetecteerd.

Hier is een `voorbeeldvoorbeeld`: Bij het inspecteren van de binaire gegevens van een voorbeeld MOV-bestand is het duidelijk dat het begint met een handtekening **ftyp** (hex: 66 74 79 70) op offset 4, die het QuickTime-containerbestandstype definieert. Het bestandssubtype is **qt~_~_** (hex: 71 74 20 20) wat verwijst naar het MOV-bestandstype. De eerste blokgrootte is 32 (hex: 00 00 00 20, big-endian, high byte first), grootte bevindt zich op offset 0. Bij offset 32 (hex: 20) bevindt zich de tweede chunk, die een grootte heeft van 8 en typ **mdat** (hex: 6D 64 61 74).

De volgende chunk bevindt zich op offset 32+8#40 (hex: 28) en heeft een grootte van 3.263.028 (hex: 00 31 CA 34) en type **mdat** (hex: 6D 64 61 74) op offset 44 (hex : 2C). De volgende chunk bevindt zich op offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) en heeft een maat 21.189 (hex: 00 00 52 C5) en type **moov** (hex: 6D 6F 6F 76) op offset 1.836.019.574 (hex: 00 31 CA 60). Dit is het laatste stuk, dus de totale bestandsgrootte is 3.263.068+21.189#3.284.257 bytes.

## Hoe MOV-bestand converteren?

Er zijn tal van mediaspelers en software-video-editors beschikbaar om MOV-bestanden naar andere populaire videobestandsindelingen te converteren. Enkele van de mediaspelers die MOV-bestanden naar andere formaten kunnen converteren, zijn:

* VideoLAN VLC-mediaspeler
* Eltima Elmedia-speler

Verschillende mediaspelers en video-editors, waaronder VideoLAN VLC-mediaspeler en Eltima Elmedia Player, kunnen MOV-bestanden converteren naar andere formaten. Deze software kan MOV-bestanden converteren naar de volgende videoformaten.

* MPEG-4-video - [MP4](/nl/video/mp4/)
* WebM-video - [WEBM](/nl/video/webm/)
* Videotransportstream - [TS](/nl/video/ts/)
* Geavanceerde systeemindeling - [ASF](/nl/video/ts/)
* Ogg Vorbis Audio - [OGG](/nl/audio/ogg/)
* MP3-audio - [MP3](/nl/audio/mp3/)
* Gratis Lossless Audio Codec - [FLAC](/nl/audio/flac/)
* WAVE-audio - [WAV](/nl/audio/wav/)

## Open Source API voor MOV-bestanden

* [Reageer Native API om MOV naar MP4 te converteren](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API om MOV-bestanden te repareren](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API om MOV naar GIF te converteren](https://github.com/skygroundmedia/convert-mov-to-gif)

## Referenties

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

