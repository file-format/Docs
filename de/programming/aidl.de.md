{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL-Datei - Sprachdatei für die Definition der Android-Oberfläche",
  "description":"Erfahren Sie anhand von Beispielen und APIs, mit denen AIDL-Dateien erstellt und geöffnet werden können, was das AIDL-Dateiformat ist.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Was ist eine AIDL-Datei?

Eine AIDL-Datei (Android Interface Definition Language) ermöglicht es Android-Entwicklern, die Kommunikation zwischen verschiedenen Apps herzustellen. Basierend auf der Programmierschnittstelle einigen sich sowohl der Client als auch der Dienst darauf, mittels Interprozesskommunikation (IPC) zu kommunizieren. Die AIDL-Datei enthält [Java](/de/programming/java/)-Quellcode zum Definieren dieser Schnittstellen und Verträge für die Kommunikation zwischen Apps.

Sie können AIDL-Dateien mit Google Android Studio oder einem beliebigen Texteditor wie Microsoft Notepad und Notepad++ öffnen.

## AIDL-Dateiformat – Weitere Informationen

AIDL sind Textdateien, die die Schnittstellen für die Kommunikation zwischen Apps enthalten. Android OS erlaubt einem Prozess nicht, auf den Speicher eines anderen Prozesses zuzugreifen. Dies führt dazu, dass die Prozesse ihre Objekte zum Verständnis des zugrunde liegenden Betriebssystems in Grundelemente aufteilen und den Prozess der Kommunikationsstrukturen für den Entwickler einrichten.

### Welche Datentypen werden von AIDL unterstützt?

AIDL unterstützt standardmäßig die folgenden Datentypen.

* Alle primitiven Typen in der Programmiersprache Java (wie z. B. int, long, char, boolean usw.)
* Zeichenfolge
* Zeichenfolge
* Liste
* Karte

## Beispiel einer AIDL-Datei

Es folgt eine Beispiel-AIDL-Datei.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Verweise

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

