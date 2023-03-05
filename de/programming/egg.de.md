{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG-Dateiformat - Python-Distributionsdatei",
  "description":"Erfahren Sie mehr über das EGG-Dateiformat und APIs, die EGG-Dateien erstellen und öffnen können.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Was ist eine EGG-Datei?

Eine EGG-Datei, auch bekannt als Python-Eier, ist ein älteres Distributionsformat von Python-Distributionen. Es ist ein [ZIP](/de/compression/zip/) komprimiertes Archiv mit der Erweiterung .egg und enthält die Quelldateien der Python-Anwendung zusammen mit Metainformationen über die Distribution. EGG-Dateien sind eine Alternative zu einer Windows Executable [EXE](/de/executable/exe/)-Datei, sind aber plattformübergreifend. Dieses ältere Format für Python-Distributionen wurde Anfang 2010 durch das neuere Dateiformat Wheel (WHL) ersetzt.

## EGG-Dateiformat

EGG-Dateien werden als komprimierte ZIP-Archive gespeichert. Wenn Sie also die Erweiterung .egg durch .zip ersetzen, können Sie sie mit standardmäßigen Dekomprimierungsdienstprogrammen wie Corel WinZIP, Microsoft Explorer oder RARLAB WinRAR öffnen.

EGG-Dateien können mit dem von Python verfügbaren Paket **distutils** erstellt werden. Ein weiteres Tool, das EGG-Dateien erstellen und öffnen kann, ist **SetupTools**. EGG-Dateien können mit **easy_install** als Paket installiert werden.

`HINWEIS - Das EGG-Dateiformat wurde zugunsten des neuen Rad-WHL-Dateiformats veraltet.`

## Bezug ##

* [Python-Eier](https://python101.pythonlibrary.org/chapter38_eggs.html)

