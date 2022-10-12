{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "Datei", "Erweiterung", "Format", "MPEG-4", "Digital Rights Management", "DRM", "Apple", "Video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Erfahren Sie mehr über das M4V-Dateiformat und APIs, die M4V-Dateien erstellen und öffnen können.",
  "linktitle" :"M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Was ist eine M4V-Datei?

Das von Apple entwickelte **M4V**-Dateiformat ist ein Video-Container, der optional mit Digital Rights Management (DRM)-Kopierschutz geschützt ist, um die Privatsphäre oder das Kopieren zu schützen. Videos und Audiospuren werden von Containerdateien umschlossen, um Wiedergabestreams zu indizieren und zu organisieren. Darüber hinaus bieten Container auch die Funktion von Kapiteln, ähnlich denen auf DVDs. Apple verwendet M4V, um Videos in seinem iTunes Store zu codieren. Es schützt die unbefugte Vervielfältigung durch Apples FairPlay-Kopierschutz, indem M4V-Dateien nur auf autorisierten Computern abgespielt werden können, die über die Konten verfügen, die zum Kauf des Videos verwendet wurden. Wenn jedoch der DRM-Schutz von M4V-Dateien entfernt wird, können diese Dateien in anderen Videoplayern abgespielt werden, indem die Erweiterung von .m4v in .mp4 geändert wird, weshalb M4V-Dateien mit MPEG-4 verknüpft sind. M4V verwendet H.264 für Video und **[AAC](/de/audio/aac/)** und Dolby Digital für Audiokodierung und -dekodierung.

## M4V-Dateistruktur ##

M4V-Dateien haben kontinuierliche Chunks mit 8 Byte Header, 4 Byte Chunk-Größe und 4 Byte Chunk-Typ in jedem Chunk. Der erste Block ist „ftype“ und hat einen Untertyp bei Offset 8. M4V definiert durch den Untertyp, der „M4V_“ sein muss. Weitere Chunk-Typen sind vordefinierte Signaturen: „ftyp“, „mdat“, „moov“, „pnot“, „udta“, „uuid“, „moof“, „free“, „skip“, „jP2“, „wide“ , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " BILD". Iterierende Chunks, bis ein unbekannter Typ erkannt wird, erstellen wir eine M4V-Datei.

Hier ist eine Untersuchung eines Beispiels: Die Binärdaten einer Beispiel-m4v-Datei werden durch Hex Viewer untersucht und es kann beobachtet werden, dass sie mit einer Signatur **ftyp** (Hex: 66 74 79 70) bei Offset 4 beginnt, was QuickTime definiert Containerdateityp. Der Dateiuntertyp ist **M4V_** (Hex: 4D 34 56 20), was auf den Dateityp M4V (MPEG-4) verweist. Die erste Blockgröße ist 32 (hex: 00 00 00 20, Big-Endian, High Byte first), die Größe befindet sich bei Offset 0. Bei Offset 32 (hex: 20) befindet sich der zweite Chunk, der eine Größe von 30.322 (hex : 00 00 76 72, Big-Endian, niedrigeres Byte zuerst) und geben Sie **moov** (hex: 6D 6F 6F 76) ein. Der nächste Chunk befindet sich bei Offset 32+30.322#30.354 (hex: 00 00 76 92) und hat die Größe 8 (hex: 00 00 00 08) und den Typ **free** (hex: 66 72 65 65).
### In M4V verwendete Codecs ###

#### Videocodec H.264 ####

H.264 ist ein Videokomprimierungsstandard, der digitales Video in ein Format konvertiert, das bei der erforderlichen Übertragung oder Speicherung weniger Platz benötigt. M4V verwendet H.264 für die Videokomprimierung. Seine Anwendung reicht von DVD, TV, Videokonferenzen und Video-Streaming über das Internet. H.264 besteht aus zwei Hauptteilen: Encoder – der das Video komprimiert, Decoder – der das komprimierte Video wieder dekomprimiert. In der folgenden Abbildung sind Codierungs- und Decodierungsprozesse hervorgehoben, und andere Prozesse werden vom H.264-Standard abgedeckt.

##### Videocodierungs- und -decodierungsprozess in H.264 #####

Für den komprimierten H.264-Bitstrom führt der Videocodierer den Vorhersage-, Transformations- und Codierungsprozess durch. Gleichzeitig führt der Decodierer den umgekehrten Vorgang des Decodierens, der inversen Transformation und der Rekonstruktion durch, um die Videodatei zurückzuerzeugen. H.264 ist halb so groß wie MPEG.

#### Audio-Codec ####

Advanced Audio Coding (AAC) ist ein Audio-Codec für die verlustbehaftete digitale Audiokomprimierung und wird in einem M4V-Container verwendet. AAC ist der Nachfolger des [MP3](/de/audio/mp3/)-Formats und erreicht bei gleicher Bitrate eine bessere Qualität als MP3. Das AAC-Format wirft während des Komprimierungsprozesses einige Informationen weg, die weniger wichtig sind. AAC ist ein blockbasierter Codec mit variabler Bitrate (VBR), bei dem jeder Block in 1024 Zeitdomänen-Samples dekodiert wird.

### Verweise ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

