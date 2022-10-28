{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "file", "extension", "format", "audio", "smaf", "mmf extension", "mmf files", "mobile music file", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das MMF-Dateiformat und APIs, die MMF-Dateien erstellen und öffnen können.",
  "title" :"MMF - Mobiles Musikdateiformat",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Was ist eine MMF-Datei? ##

MMF ist eine Dateierweiterung, die einer SMAF-Datei zugeordnet ist. Das MMF steht für Mobile Music File, während das SMAF für Synthetic-Music Mobile Application Format steht. Die MMF-Dateien innerhalb eines Smartphones enthalten Systemklingeltöne, Sound und können auch Grafiken und Textanzeigen enthalten. Das MMF enthält ferner drei Arten von Instrumentenparametern, einschließlich FM, PCM und Stream PCM. Diese Dateiformate sind mit der Windows-Systemplattform kompatibel. Die MMF-Dateien werden als Datendateien kategorisiert. Normalerweise unterstützt Microsoft Mail MMF-Dateien. Die Datei mit dem MMF-Suffix kann auf jedes mobile Gerät oder jede Systemplattform kopiert werden.
Darüber hinaus sind diese Dateien im Vergleich zu Dateien im Standard-MIDI-Format viel kleiner. [WAV](/de/audio/wav/)- und [MID](/de/audio/mid/)-Dateien können in das MMF-Format konvertiert werden, das dann als Audioinhalt geteilt und verteilt werden kann. Diese Dateien können per E-Mail direkt an Telefone und PCs gesendet werden.


## Kurze Geschichte ##

Yamaha hat SMAF-Tools als Sounddateien entwickelt, damit Smartphones eine größere Anzahl einzigartiger Klingeltöne speichern können. Yamaha führte SMAF mit der Produktion seiner MA-1-, MA-2-, MA-3-, MA-5- und MA-7-LSI-Soundchips ein. Alle diese Formate wurden Anfang 2000 bei Mobiltelefonen auf dem ostasiatischen Markt ziemlich vertraut.

Auf internationaler Ebene wurde das MMF-Format von Samsung autorisiert. Mit Hilfe des MMF-Formats war Samsung in der Lage, eine große Auswahl an polyphonen Klingeltönen zu entwerfen, die in Samsung-Smartphones verwendet werden können.

Yamaha wollte das Format noch bekannter machen und veröffentlichte daher neben den offiziellen Yamaha SMAF-Dateien weitere Tools, die mit diesem Format kompatibel sind. Damit können Benutzer jetzt ganz einfach MMF-Dateien auf ihren Computern abspielen.


## Spezifikationen des MMF-Dateiformats ##

MMF-Dateien sind in Datenabschnitte kategorisiert. Eine vorangestellte Struktur um ein 8-Byte herum wird verwendet, um jedes Segment zu beschreiben.
Das 4-Byte-Etikett enthält CNTI, OPDA, MSTR, MTR und ATR. Datengröße plus 8 Byte ist die Chunk-Größe; Die gesamte Dateigröße wird durch Summieren aller Chunk-Größen berechnet. Wenn eine Datei nicht beschädigt wurde, sollte die summierte Dateigröße gleich einer primären Header-Größe sein.

### Header ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Hier ist ein Beispiel für eine MMF-Datei:

![](../mmf.png)

## Verweise ##

* [MMF – Von Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

