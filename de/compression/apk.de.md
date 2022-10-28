{
  "date" : "2019-10-11",
  "keywords" :[ "apk-Datei", "apk-Dateiformat", "was ist eine apk-Datei", "Datei", "apk-Beispiel", "apk-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Was ist eine APK-Datei?",
  "description":"Erfahren Sie, was eine APK-Datei und APIs sind, die APK-Dateien erstellen und öffnen können.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Was ist eine APK-Datei?

Eine Datei mit der Erweiterung .apk ist eine Google-Android-App-Datei, die zum Installieren von Apps (Anwendungen) auf Android-Geräten verwendet wird. Es wird als ausführbare Datei mit der offiziellen IDE Google Android Studio erstellt und in den Google Play Store hochgeladen, um von Endbenutzern heruntergeladen und installiert zu werden. APK-Dateien können generiert und für die manuelle Installation bereitgestellt werden, bevor sie im Google Play Store veröffentlicht werden. Dies hilft beim Testen der Funktionalität und des Verhaltens der generierten APK-Paketdatei. Daher muss man sicher sein, dass die APK-Datei aus einer vertrauenswürdigen Quelle stammt und keine Malware enthält.

## APK-Dateiformat

APK-Dateien sind komprimiert im Dateiformat [ZIP](/de/compression/zip/) gepackt, das mit jeder Software zum Öffnen von ZIP-Dateien geöffnet werden kann. Die .apk-Erweiterung einer solchen Datei kann in .zip umbenannt und die Datei in einer beliebigen ZIP-Anwendung geöffnet oder deren Inhalt extrahiert werden.

## Inhalt des APK-Pakets

Eine einzelne APK-Datei enthält alle notwendigen Dateien, die für ihre Installation und Ausführung erforderlich sind. Eine APK-Datei enthält, wenn sie mit einer ZIP-Anwendung extrahiert wird, die folgenden Dateien und Ordner.

* `META-INF/`: Verzeichnis, das die Manifestdatei, die Signatur und eine Liste der Ressourcen im Archiv enthält
* „lib/“: Verzeichnis mit kompiliertem Code für bestimmte Plattformen wie armeabi-v7a, x86, arm64-v8a usw.
* `res/`: Verzeichnis, das nicht kompilierte Ressourcen wie Bilder enthält
* `assets/`: Verzeichnis mit Anwendungs-Assets, die von AssetManager abgerufen werden können.
* „androidManifest.xml“: Enthält den Namen, die Versionsinformationen und den Inhalt der APK-Datei
* `classes.dex`: Dies sind kompilierte Java-Klassen, die auf der virtuellen Maschine von Dalvik und von der Android-Laufzeit ausgeführt werden können
* `resources.arsc`: Kompilierte Ressourcendatei wie Strings

## Wie installiere ich die APK-Datei auf einem Android-Gerät?

Um eine APK-Datei auf Ihren Android-Geräten zu installieren, können die folgenden Schritte verwendet werden.

1. Laden Sie die APK mit einem Webbrowser herunter
2. Tippen Sie darauf – Sie sollten dann den Download in der oberen Leiste Ihres Geräts sehen können
3. Öffnen Sie nach dem Herunterladen Downloads, tippen Sie auf die APK-Datei und tippen Sie auf Ja, wenn Sie dazu aufgefordert werden.

Befolgen Sie diese Schritte, um die Installation der App auf Ihrem Gerät zu starten.

## Verweise

* [APK-Dateiformat](https://en.wikipedia.org/wiki/Android_application_package)

