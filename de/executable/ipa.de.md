{
  "date" : "2021-08-30",
  "keywords" :[ "ipa-datei", "ipa-dateiformat", "was ist eine ipa-datei", "datei", "ipa-beispiel", "ipa-dateierweiterung", "erweiterung", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das IPA-Dateiformat und APIs, die IPA-Dateien erstellen und öffnen können.",
  "title" :"IPA - iOS-Anwendungspaketdatei",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Was ist eine IPA-Datei?
Eine Datei mit der Erweiterung .ipa gehört zu iOS und ist als Anwendungspaketdatei bekannt. Dies ist eine Archivdatei (komprimiert mit [ZIP](/de/compression/zip/)-Komprimierung), die eine iOS-Anwendung speichert, aber diese Anwendung kann nur auf iOS- oder ARM-basierten MacOS-Geräten wie einem iPad, iPhone oder IPod Touch. Hauptsächlich können iTunes, Apple Configurator 2 oder Software von Drittanbietern verwendet werden, um IPA-Dateien zu installieren.

## IPA-Dateiformat
Die IOS-Entwickler, die die Apps mit dem Apple Xcode entwickeln, sind mit IPA-Dateien gut vertraut, da sie ihre entwickelten Apps als IPA-Dateien verpacken müssen, um die Bereitstellung im App Store zu testen. Die IPA-Dateien werden zwar bekanntermaßen als iOS-Apps installiert, Sie können sie aber auch entpacken, um die enthaltenen App-Daten anzuzeigen. Da eine IPA-Datei nur eine Binärdatei für die ARM-Architektur von Mobiltelefonen und keine Binärdatei für die x86-Architektur enthält, können viele .ipa-Dateien nicht auf dem iPhone-Simulator installiert werden.
### Aufbau einer .ipa-Datei
Das folgende Beispiel zeigt den Aufbau eines IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Das Obige ist eine integrierte Struktur, die iTunes und App Store erkennen können. Nach dieser Struktur:
- Das Payload-Verzeichnis enthält alle App-Daten.
- Die iTunes Artwork-Datei ist ein 512 × 512 Pixel großes PNG-Bild, das das Symbol der App enthält, das in iTunes und der App Store-App auf dem iPad angezeigt wird.
- Die iTunesMetadata.plist enthält verschiedene Informationen, die vom Namen und der ID des Entwicklers, den Copyright-Informationen, der Bundle-ID, dem Namen der App, dem Genre, dem Veröffentlichungsdatum, dem Kaufdatum usw. reichen.
- Der Ordner META-INF enthält nur Metadaten darüber, mit welchem Programm das IPA erstellt wurde.


## Verweise

* [.ipa - von Wikipedia](https://en.wikipedia.org/wiki/.ipa)


