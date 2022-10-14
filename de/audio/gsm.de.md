{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "file", "extension", "format", "Audio", "Global System for Mobile Audio", "gsm extension", "gsm files"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das GSM-Dateiformat und APIs, die GSM-Dateien erstellen und öffnen können.",
  "title" :"GSM - Globales System für mobiles Audiodateiformat",
  "linktitle" :"GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## Was ist eine GSM-Datei? ##

GSM ist eine Dateierweiterung, die mit Global System for Mobile Audio Format Files verknüpft ist. Dateien mit GSM-Erweiterungen können auf Linux-, Windows- und Mac OS-Plattformen geöffnet werden. Das GSM-Dateiformat gehört zur Kategorie der Audiodateien.

Eine GSM-Datei wird mit einem verlustbehafteten CBR-Soundkompressionscodec (Constant Bitrate) kodiert. Die Abtastrate in einer GSM-Audiodatei beträgt 8000 Abtastungen/Sekunde, während die Datenrate etwa 13 kbps beträgt. Die Bitrate innerhalb der GSM-Dateien gewährleistet die Qualität während der Sprachaufzeichnung. Darüber hinaus ist das GSM-Dateiformat auch als weltweites Standardformat für die Verwendung in Mobiltelefonen bekannt, und WAV-Dateien können auch einfach unter Verwendung eines GSM-Dateiformats codiert werden. Alle Probleme mit einer GSM-Datei können vom Benutzer leicht selbst gelöst werden, ohne einen Experten aufzusuchen. Benutzer können auch GSM-Dateien in die Formate [MP3](/de/audio/mp3/) und [MP4](/de/audio/mp4/) konvertieren.

## Kurze Geschichte ##

GSM ist ein Audiodateiformat, das für die Internettelefonie in Europa entwickelt wurde. Es wurde vom European Telecommunications Standard Institute (ETSI) entwickelt, um als digitales 2G-Mobiltelefon in Mobiltelefonen und Tablets verwendet zu werden. Heute wird es verwendet, um Aufzeichnungen von Telefongesprächen und Sprachnachrichten zu speichern.

## Spezifikationen des GSM-Dateiformats ##

GSM arbeitet in einem strukturierten Netzwerk, das aus folgenden Abschnitten besteht:

- **Modulation** : Es ist ein Prozess der Umwandlung von Eingabedaten in ein Format, das leicht übertragen werden kann. Die übertragenen Daten werden auf der Empfangsseite demoduliert
- **Übertragungsrate** : GSM ist ein digitales System mit einer Bitrate von über 270 kbps
- **Uplink-Frequenzbereich** : 933-960 MHz
- **Downlink-Frequenzbereich**: 890 – 915 MHz
- **Channel Spacing** : Dies bedeutet den Abstand zwischen benachbarten Barrieren, der etwa 200 kHz betragen sollte
- **Duplex Distance** : Dies ist der Abstand zwischen Uplink- und Downlink-Frequenzen, der 80 MHz betragen sollte
- **Sprachcodierung**: GSM verwendet Linear Predictive Coding (LPC). LPC komprimiert die Bitrate. Wenn das Audiosignal einen Filter passiert und den Vokaltrakt nachahmt. GSM codiert Sprache mit 13 kbps

| Audiokomprimierungsformat | Algorithmus | Abtastrate | Bitratentransformation | Latenz | CBR | VBR | Stereoanlage | Mehrkanal |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8kHz | 5,6 kbit/s | 25ms | Ja | Nein | Nein | Nein |
| GSM-FR | RPE-LTP | 8kHz | 13kbit/s | 20–30 ms | Ja | Nein | Nein | Nein |
| GSM-EFR | ACELP | 8kHz | 12,2 kbit/s | 20–30 ms | Ja | Nein | Nein | Nein |


## Verweise ##

* [GSM – Von Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

