{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "Was ist eine JAR-Datei", "Wie man eine JAR-Datei öffnet", "Erweiterung", "Datei", "JAR-Datei", "JAR-Dateiformat", ".jar-Erweiterung "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java-Archivdateiformat",
  "description":"Erfahren Sie mehr über das JAR-Dateiformat und APIs, die JAR-Dateien erstellen und öffnen können.",
  "linktitle" :"KRUG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine JAR-Datei?

Eine Datei mit der Erweiterung .jar ist eine Java-Archivdatei, die viele verschiedene anwendungsbezogene Dateien in einer einzigen Datei enthält. Dieses Dateiformat wurde erstellt, um die Geschwindigkeit beim Laden eines heruntergeladenen Java-Applets im Browser über eine HTTP-Transaktion zu verringern, indem vermieden wird, dass mehrere HTTP-Verbindungen erstellt werden. Eine einzelne JAR-Datei kann Java-Klassendateien ([.class](/de/programming/class/)), [images](/de/image/) und [sounds](/de/audio/) enthalten. Einzelne Elemente in einer JAR-Datei können vom Anwendungsentwickler digital signiert werden, um ihre Herkunft zu authentifizieren. JAR-Dateien werden regelmäßig verwendet, um funktionale APIs zu erstellen, die spezifische Funktionen in Bezug auf diese API enthalten.

## JAR-Dateiformat

JAR-Dateien basieren auf dem beliebten [ZIP-Dateiformat](/de/compression/zip/), das seine einzelnen Inhaltsdateien in einer einzigen Datei archiviert. Das JAR-Dateiformat unterstützt Komprimierungen, was zu einer geringeren Dateigröße zum Herunterladen führt und somit die Downloadzeit weiter verbessert. Der Artikel [JAR-Dateispezifikationen](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) von Oracle enthält vollständige Einzelheiten zu den internen Spezifikationen von JAR-Dateien.

### Die Manifestdatei

Wenn eine JAR-Datei erstellt wird, wird darin automatisch eine Manifestdatei erstellt, die die Metadateninformationen zum Inhalt der JAR-Datei enthält. Diese Datei zeigt den Inhalt, der in der JAR-Datei verpackt ist. Eine typische Manifest-Datei sieht wie folgt aus und zeigt die Ordner und Klassen, die in der JAR-Datei enthalten sind.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifestspezifikationen

Manifestspezifikationen werden von Oracle wie folgt definiert.

`manifest-file`: main-section newline \*individual-section

`Hauptabschnitt`: Versionsinfo Zeilenumbruch \*Hauptattribut

`version-info`: Manifest-Version : Versionsnummer

`Versionsnummer` : Ziffer+{.Ziffer+}*

`Hauptattribut`: (irgendein legitimes Hauptattribut) Zeilenumbruch

`individual-section`: Name : value newline \*perentry-attribute

`perentry-attribute`: (jedes legitime perentry-Attribut) Zeilenumbruch

`newline` : CR LF | LF | CR (nicht gefolgt von LF)

`digit`: {0-9}

### Ausführbares JAR

JAR-Dateien können auch aus einer Anwendung bestehen, die von Java Virtual Machine (JVM) ausgeführt werden kann, ähnlich wie jede andere Anwendung auf dem Microsoft Windows-Betriebssystem. In diesem Fall muss die JVM den Einstiegspunkt der Anwendung kennen, der eine beliebige Klasse mit einer öffentlichen statischen void-Hauptmethode ist. Die Manifestdatei identifiziert eine solche Klasse mit dem Header „Main-Class“ im folgenden Format:

```
Main-Class: com.example.MyClassName
```



## Verweise

* [JAR-Dateiübersicht](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR-Dateiformat](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,in%20one%20file%20for% 20distribution.&text=Sie%20sind%20auf%20der,jar%20Datei-%20Erweiterung aufgebaut%20.)

