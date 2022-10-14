{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV-Dateiformat",
  "keywords" :[ "mkv", "matroska video", "mkv-format", "wie man mkv-dateien abspielt", "video", "datei", "format" ],
  "description":"Erfahren Sie mehr über das MKV-Dateiformat und APIs, die MKV-Dateien erstellen und öffnen können.",
  "linktitle" :"MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Was ist eine MKV-Datei? ##

MKV (Matroska Video) ist ein Multimedia-Container ähnlich dem Format [MOV](/de/video/mov/) und [AVI](/de/video/avi/), unterstützt jedoch mehr als eine Audio- und Untertitelspur in derselben Datei. Eine MKV-Datei ist das Matroska-Multimedia-Containerformat, das für Videos verwendet wird. MKV basiert auf Extensible Binary Meta Language und unterstützt mehrere Video- und Audiokompressionsformate. Der Hauptunterschied zwischen MKV und anderen Videoformaten besteht darin, dass MKV ein Container und kein Codec ist. MKV-Dateien werden mit der Dateierweiterung .mkv gespeichert. MKV kann Audio, Video und Untertitel in eine einzige Datei integrieren, selbst wenn diese Elemente unterschiedliche Codierungsarten verwenden. Beispielsweise könnten Sie eine MKV-Datei haben, die H.264-Video und MP3 oder AAC für Audio enthält. MKV unterstützt auch Beschreibungen, Bewertungen, Coverbilder und sogar Kapitelpunkte. Es gibt mehrere Schlüsselfunktionen, die MKV zukunftssicher machen. Zu diesen Funktionen gehören:

- Unterstützung für die schnelle Suche.
- Möglichkeit, verschiedene Audio- und Videostreams auszuwählen.
- Unterstützung für Untertitel (hartcodiert und weichcodiert).
- Unterstützung für Metadaten, Kapitel und Menüs.
- Möglichkeit zum Online-Streaming.
- Fähigkeit, fehlerhafte Dateien wiederherzustellen, die die Möglichkeit bieten, beschädigte Dateien abzuspielen.

## Kurze Geschichte ##

Die MKV-Datei entstand 2002 in Russland. Der leitende Entwickler war Lasse Kärkkäinen, der mit dem Gründer von Matroska, Steve Lhomme, und einem Team von Programmierern zusammenarbeitete. MKV wurde als Open-Standards-Projekt entwickelt, was bedeutet, dass es Open Source und kostenlos nutzbar ist. Im Laufe der Zeit wurde das Format verbessert und wurde 2010 zur Grundlage des WebM-Multimediaformats.

## Matroska-Design ##

Matroska fügt der EBML-Spezifikation die folgenden Einschränkungen hinzu.

- Der **docType** des **EBML Header** muss 'matroska' sein.
- Die **EBMLMaxIDLength** des **EBML-Headers** muss 4 sein.
- Die **EBMLMaxSizeLength** des **EBML-Headers** muss zwischen 1 und 8 (einschließlich) liegen.

Alle Elemente der obersten Ebene sind in 4 Oktetts codiert.

- Sprachcodes: Matroska (Version 1 bis 3) verwendete Sprachcodes, die entweder die bibliografische ISO-639-2-Form mit 3 Buchstaben sein können (wie "fre" für Französisch) oder zusätzliche Ländercodes wie "fre-ca " für kanadisches Französisch. Ab Matroska Version 4 KÖNNEN entweder ISO 639-2 oder BCP 47 für Sprachcodes verwendet werden, obwohl BCP 47 empfohlen wird.
- Physische Typen: Diese haben unterschiedliche Bedeutungen für Audio- und Videodateien. Beispielsweise bedeutet ChapterPhysicalEquiv = 60 (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) für Audio und (DVD / VHS / LASERDISC) für Video.
- Blockstruktur - Blockheader: Der Blockheader enthält Informationen zu Titelnummer, Zeitstempel, Art der Schnürung usw.
- Lacing: Dies ist ein Mechanismus zum Speichern von Platz beim Speichern von Daten, der normalerweise für kleine Datenblöcke (Frames) verwendet wird. Es gibt 3 Arten der Schnürung:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock-Struktur: Sie ist von der **Block-Struktur** inspiriert, wobei der Hauptunterschied in der Hinzufügung von **Keyframe**- und **Discardable**-Flags besteht. Ansonsten ist alles gleich.

## Matroska-Struktur ##

Ein Matroska-Dokument muss aus mindestens einem **EBML-Dokument** bestehen, das den **Matroska-Dokumenttyp** verwendet. Jedes **EBML-Dokument** muss mit einem **EBML-Header** beginnen, gefolgt vom **EBML-Wurzelelement**, das als Segment definiert ist. Matroska definiert mehrere Top-Level-Elemente, die innerhalb des **Segments** vorkommen können.

EBML verwendet ein System von Elementen, um ein EBML-Dokument zu erstellen. Das Folgende ist die Liste der Top-Level-Elemente in der Matroska-Datei:

- **EBML-Dokument**: Wrapper für die gesamte Datei.
- **EBML Header**: Enthält die Header-Informationen für die Datei wie DocType.
- **Segment**: Das oberste Element, das alle anderen Elemente der obersten Ebene enthält.
- **SeekHead**: Enthält die Position von Segmenten anderer Top-Level-Elemente.
- **Info**: Enthält allgemeine Informationen über das Segment.
- **Tracks**: Ein Informationselement der obersten Ebene mit vielen beschriebenen Tracks.
- **Kapitel**: Wird verwendet, um grundlegende Menüs und Partitionsdaten zu definieren.
- **Cluster**: Das Top-Level-Element, das die Blockstruktur enthält.
- **Cues**: Ein Top-Level-Element, das alle lokalen Einträge für das Segment enthält, die den Zugriff beschleunigen.
- **Anhänge**: Enthält angehängte Dateien.
- **Tags**: Dieses Element enthält Metadaten, die Tracks, Editionen, Kapitel, Anhänge oder das Segment als Ganzes beschreiben.

Die folgende Tabelle zeigt die Struktur des Matroska-Dokuments, wobei die meisten Elemente in einer Hierarchie angezeigt werden:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML-Header | | | |
| Segment | Suchkopf| Suche | SeekID |
| | | | Suchposition |
| | Infos | SegmentUID | |
| | | SegmentDateiname | |
| | | VorherigeUID | |
| | | ZurückDateiname | |
| | | NächsteUID | |
| | | NächsterDateiname | |
| | | SegmentFamilie | |
| | | KapitelÜbersetzen | |
| | | ZeitstempelSkalierung | |
| | | Dauer | |
| | | DatumUTC | |
| | | Titel | |
| | | MuxingApp | |
| | | SchreibApp | |
| | Spuren | TrackEintrag | Titelnummer |
| | | | TrackUID |
| | | | Spurtyp |
| | | | Name |
| | | | Sprache |
| | | | CodecID |
| | | | CodecPrivat |
| | | | CodecName |
| | | | Videos | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoModus |
| | | | | AlphaMode |
| | | | | Pixelbreite |
| | | | | Pixelhöhe |
| | | | | Anzeigebreite |
| | | | | Anzeigehöhe |
| | | | | AspectRatioType |
| | | | | Farbe |
| | | | Ton | Abtastfrequenz |
| | | | | Kanäle |
| | | | | Bittiefe |
| | Kapitel | AusgabeEintrag | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | KapitelAtom | KapitelUID |
| | | | | KapitelStringUID |
| | | | | KapitelZeitStart |
| | | | | KapitelZeitEnde |
| | | | | KapitelFlagAusgeblendet |
| | | | | KapitelAnzeige | ChapString |
| | | | | | ChapSprache |
| | Cluster | Zeitstempel |
| | | SilentTracks |
| | | Stelle |
| | | VorherigeGröße |
| | | SimpleBlock |
| | | BlockGruppe |
| | | VerschlüsselterBlock |
| | Stichworte | CuePoint | CueTime |
| | | | CueTrackPositionen |
| | Anhänge | AngehängteDatei | Dateibeschreibung |
| | | | Dateiname |
| | | | FileMimeType |
| | | | DateiUID |
| | | | Dateiverweis |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Stichworte | Tag | Ziele | Zieltypwert |
| | | | | Zieltyp |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagKapitelUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagSprache |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinär |
| | | | | SimpleTag |


### Codecs verwenden ###

Wenn Sie keinen neuen Mediaplayer möchten und lieber Ihren vorhandenen Player verwenden möchten, müssen Sie einige Codecs (Abkürzung für Komprimierung/Dekomprimierung) installieren. Auch wenn das Herunterladen von Codecs eine gültige Option ist, sollten Sie auf die Quelle achten, da diese möglicherweise Malware enthalten.

## Verweise ##

- [Matroska von Wikipedia](https://en.wikipedia.org/wiki/Matroska)

