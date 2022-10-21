
{
  "date" : "2022-02-06",
"Schlüsselwörter": [ ".apks-Datei", "Erweiterung", "Format", "APK-Set-Archiv", "wie man eine .apks-Datei öffnet", "apks-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS-Datei - APK-Set-Archiv",
  "description":"Erfahren Sie, was eine APKS-Datei ist?",
  "linktitle" :"APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Was ist eine APKS-Datei?

Eine Datei mit der Erweiterung .apks ist eine Archivdatei, die eine Sammlung von **APK**-Dateien von Android-Paketen darstellt. Jede einzelne APK-Datei in der APKS-Datei wird unter Berücksichtigung verschiedener Aspekte der Geräte generiert. Dazu gehören Architektur, Sprache, Bildschirmdichte und andere Gerätefunktionen. APKS-Dateien werden von **bundletool** generiert. Es wird verwendet, um Android App Bundle zu erstellen und App Bundle in verschiedene APKs für die Bereitstellung auf Geräten zu konvertieren.

## APKS-Dateiformat - Weitere Informationen

APKS-Dateien werden als komprimierte Dateien im Dateiformat [ZIP](/de/compression/zip/) gespeichert.

## Wie erstelle ich eine APKS-Datei?

Wenn das Android App Bundle (AAB) fertig ist, kann sein Verhalten im Google Play Store für die Bereitstellung auf einem Gerät getestet werden. APKS-Dateien können zu diesem Zweck aus AAB-Dateien generiert und mit dem Android [Bundletool] von Google (https://developer.android.com/studio/command-line/bundletool) auf Testgeräten installiert werden. Es bietet Befehlszeilentools zum Erstellen der APKS-Archivdatei aus APKs mit dem folgenden Befehl.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Um die APKs auf einem Gerät bereitzustellen, kann die APKS-Datei wie folgt mit den Gerätesignaturinformationen signiert werden.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Verweise

* [bundletool - Kommandozeile](https://developer.android.com/studio/command-line/bundletool)

