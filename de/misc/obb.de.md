{
  "date" : "2022-02-16",
  "keywords" :[ "obb-Datei", "obb-Dateiformat", "was ist eine obb-Datei", "Datei", "obb-Beispiel", "obb-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB-Dateiformat - Undurchsichtige binäre Blob-Datei für Android",
  "description":"Erfahren Sie mehr über das OBB-Dateiformat und APIs, die OBB-Dateien erstellen und öffnen können.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Was ist eine OBB-Datei?

Eine OBB-Datei ist eine Erweiterungsdatei, die zusätzliche Daten enthält, die zusätzlich zur Android [APK](/de/compression/apk/)-Datei vorhanden sind. Der Google Play Store erlaubt keine Android-APK-Datei mit einer Größe von mehr als 100 MB. Einige Anwendungen erfordern jedoch möglicherweise zusätzlich zu den APK-Dateien das Hosten von hochauflösenden Grafiken, Mediendateien oder anderen großen Assets. Hier kommen die OBB-Dateitypen ins Spiel. Google Play erlaubt es, diese Erweiterungsdateien als Ergänzung zur APK-Datei anzuhängen.

## OBB-Dateiformat

OBB-Dateien werden zusammen mit den APK-Dateien als Binärdateien gespeichert. Wenn die OBB-Dateien von einem APK begleitet werden, hostet Google Play die Erweiterungsdateien auf seinem Server, und dem Entwickler werden keine zusätzlichen Kosten in Rechnung gestellt. Diese zusätzlichen Dateien werden im freigegebenen Speicher des Geräts auf einer SD-Karte oder einer per USB montierbaren Partition gespeichert, wenn die App zur Installation heruntergeladen wird.

Die OBB-Dateien werden beim Herunterladen heruntergeladen und installiert. Aber in einigen Fällen werden diese zur Installation heruntergeladen, wenn die Anwendung zum ersten Mal ausgeführt wird.

### OBB Maximale Dateigröße

Im Google Play Store können Sie OBB-Erweiterungsdateien mit einer Größe von bis zu 2 GB hochladen. Es wird empfohlen, große Dateien als komprimierte [ZIP](/de/compression/zip/)-Dateien hochzuladen, um ein effizientes Hochladen über das Internet zu ermöglichen.

Diese Erweiterungsdateien können entweder als primäre **Haupterweiterungsdatei** für zusätzliche Ressourcen gehostet werden, die von der App benötigt werden, oder als optionale Patch-Erweiterungsdatei, die für kleine Aktualisierungen der Haupterweiterungsdatei vorgesehen ist.

## Verweise

* [Android-Entwickler – Erweiterungsdateien](https://developer.android.com/google/play/expansion-files)

