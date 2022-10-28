{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "was ist eine arsc-Datei", "wie man eine arsc-Datei öffnet", "Erweiterung", "Datei", "arsc-Datei", "arsc-Dateiformat", "arsc-Dateierweiterung" ,"arsc-Dateibeispiel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC – Android-Paket-Ressourcentabellendatei",
  "description":"Erfahren Sie mehr über das ARSC-Dateiformat und APIs, die ARSC-Dateien erstellen und öffnen können.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Was ist eine ARSC-Datei?

Eine ARSC-Datei ist eine Android-Ressourcentabellendatei, die die Ressourcenliste der Anwendung in einem Tabellenformat enthält. Diese enthält Informationen wie Ressourcennamen, Eigenschaften und IDs. ARSC-Dateien sind Teil von APK-Paketen, die zum Installieren dieser Android-Apps verwendet werden. Alle Ressourcen wie Bilder, Layouts, Stile und Zeichenfolgen in einer Android-Anwendung werden beim Generieren der APK-Datei in Binärdateien konvertiert. Gleichzeitig wird auch die ARSC-Datei generiert, die eine Liste aller kompilierten Ressourcen des Programms und ihrer IDs enthält.

## ARSC-Dateiformat

Die .arsc-Erweiterungsdateien sind Binärdateien, die generiert werden, nachdem der Compiler wie ANT (Eclipse) oder Gradle (AS) den Android-Anwendungscode kompiliert hat, um die Datei [APK](/de/compression/apk/) zu erstellen. Sie können die APK-Datei mit einem beliebigen Archivierungsprogramm wie WinZip extrahieren, um ihren Inhalt anzuzeigen, bei dem es sich um die kompilierten Java-Klassendateien handelt, dh "classes.dex". Zusätzlich zu diesen enthält es auch diese ARSC-Datei, die Metainformationen enthält über:

* Die XML-Knoten
* Die Attribute
* Die Ressourcen-IDs

Ressourcen in einer APK-Datei werden durch die Ressourcen-IDs referenziert, während die Attribute zur Laufzeit in einen Wert aufgelöst werden. Das Android-Tool aapt sammelt alle in Dateien definierten Ressourcen zur Build-Zeit und weist ihnen Ressourcen-IDs zu. Nachdem den kompilierten Ressourcen Kennungen zugewiesen wurden, wird aus dem Quellcode sowie der Datei resources.arsc eine R.java-Datei generiert.

## Verweise

* [Struktur der binären Ressourcentabelle] (https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

