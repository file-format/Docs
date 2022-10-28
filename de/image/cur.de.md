{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "extension", "file", "format", "image", "Device-Independent Bitmap", "Cursor File Format", "Cursor", "Windows", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Cursor-Dateiformat",
  "description":"Erfahren Sie mehr über das CUR-Dateiformat und APIs, die CUR-Dateien erstellen und öffnen können.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine CUR-Datei? ##

Eine CUR-Datei ist ein statisches Microsoft Windows-Cursor-Dateiformat. Grundsätzlich handelt es sich um stationäre Bilder, die mit Ausnahme der Erweiterung in jeder Hinsicht mit ICO-Dateien (Symboldateien) identisch sind. Sowohl CUR als auch [ICO](/de/image/ico/) basieren auf der Device-Independent-Bitmap-Spezifikation [DIB](/de/image/dib/) (Device-Independent Bitmap). Standard- und benutzerdefinierte Cursor wie der Windows-Mauszeiger für das Windows-Betriebssystem werden in CUR-Dateien gespeichert. Es kann ein Pfeil für den normalen Gebrauch, eine sich drehende Sanduhr zur Darstellung von Wartezeiten oder ein I-Balken für die Textbearbeitung sein. CUR-Dateien werden mit dem Installationspaket der benutzerdefinierten Desktopdesigns geliefert, um sicherzustellen, dass der Windows-Cursor mit dem benutzerdefinierten Desktopdesign übereinstimmt.

## Technische Spezifikation ##

CUR-Dateien sind binäre Systemdateien, die auf Geräten zu finden sind, die auf dem Microsoft Windows-Betriebssystem laufen. CUR-Zeigerbilder gibt es in verschiedenen Standardgrößen wie 16×16, 32×32 usw. CUR-Dateien sind den ICO-Dateien sehr ähnlich; beide bestehen aus kleinen stationären Bildern. Nur die Erweiterung von CUR- und ICO-Dateien ist unterschiedlich. Darüber hinaus unterscheidet sich die Erläuterung eines Hotspots im Header der CUR-Datei von der ICO-Datei. Der Hotspot interpretiert den Pixelversatz von der oberen linken Ecke zu der Stelle, an der Sie mit der Maus zeigen. Windows-Systeme verwenden immer noch die CUR-Dateien, aber die animierten Cursor haben jetzt normalerweise die Dateierweiterung ANI anstelle von CUR.

## Kurze Geschichte ##

Die CUR-Datei wird aus der ICO-Datei erstellt. Das erste CUR-Dateiformat wurde 1981 in Microsofts Betriebssystem Windows 1.0 integriert, um die kommerzielle Nutzung zu erleichtern. Bald wurden mehr interaktive Cursor eingeführt, die es Benutzern ermöglichten, ihre Cursoreinstellungen aus den verfügbaren vorinstallierten Optionen zu ändern. Es ist jedoch einfach, eine CUR-Datei selbst zu bearbeiten, selbst wenn Sie über unzureichende technische Kenntnisse verfügen.


## CUR-Beispiel ##

Die CUR-Dateien finden Sie unter *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="CUR-Dateiformat" >}}

