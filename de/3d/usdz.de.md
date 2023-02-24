{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz-Datei", "usdz-Dateiformat", "Dateiformat", "3d", "usdz-Datei-Download"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Universelles Szenenbeschreibungs-ZIP-Format",
  "description":"Erfahren Sie mehr über das USDZ-Dateiformat und APIs, die USDZ-Dateien öffnen und erstellen können.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Was ist eine USDZ-Datei?

Eine Datei mit .usdz ist ein unkomprimiertes und unverschlüsseltes ZIP-Archiv für das Dateiformat [USD](/de/3d/usd/) (Universal Scene Description), das darin eingebettete Dateien anderer Formate (z. B. Texturen und Animationen) enthält und Proxys enthält das Archiv und führt sie direkt mit der USD-Laufzeit aus, ohne dass sie entpackt werden müssen. USDZ-Dateien sind Pakete, deren Design auf der neuen Abstraktion eines Pakets auf Ar-Ebene basiert. Usdz wurde bei der IANA registriert und hat den Medientypnamen des Modells und einen Subtypnamen von vnd.usd+zip und seine Details finden Sie auf der [IANA-Registrierungsseite](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ-Dateiformat

USDZ-Dateien basieren auf dem ZIP-Dateiformat, das einzelne Dateien in seinem Container archiviert. Dadurch kann der Empfänger den Inhalt einfach entpacken und die normalen USD-Szenenbeschreibungsdateien verwenden, um damit zu arbeiten und sie zu inspizieren. Fast alle Betriebssysteme bieten integrierte Unterstützung für die ZIP-Dateiformate, und die Wahl dieses Archivierungsformats gegenüber einer beliebigen benutzerdefinierten Methode macht es für USDZ-Dateien einfach, als einfaches Transportprotokoll nützlich zu sein.

### ZIP-Einschränkungen

Das USDZ-Dateiformat verwendet das ZIP-Dateiformat ohne „Komprimierung“ und „Verschlüsselung“. Dies wurde beabsichtigt, um zwei Anforderungen zu erfüllen:

* Für ein Paket, das bereits in den Speicher oder als einzelne Datei auf der Festplatte geladen wurde, sind die APIs in USD für den Zugriff auf die im Image enthaltenen Daten verfügbar
* Es sollte keine Notwendigkeit bestehen, Dateien auf Disc zu extrahieren oder mehr Heap-Speicher zuzuweisen

Mit USDZ werden diese beiden Anforderungen erfüllt, da die meisten Bildformate selbst interne Komprimierungsschemata zulassen, was zu einer kompakten Dateigröße führt.

### Layoutanforderungen

USDZ-Pakete erfordern das Layout der Dateien innerhalb des Pakets, dass die Daten für jede Datei bei einem Vielfachen von 64 Byte vom Anfang des Pakets beginnen sollten. Das Paket sollte jedoch mit einer nativen [USD](/de/3d/usd/)-Datei beginnen, falls das Paket mit einer einfachen Referenz angesprochen wird. In einem solchen Fall wird diese erste USD-Datei als Default Layer bezeichnet. Kunden, die "streamfähige Inhalte" liefern möchten, möchten möglicherweise auch andere Layouteinschränkungen berücksichtigen.

## Herunterladen der USDZ-Datei
Da die usdz-Dateien mit anderen hochwertigen Bildern und usd-Dateien gepackt sind, können sie mehr Festplattenspeicher belegen. Hier finden Sie eine einfache und kleinere USDZ-Beispieldatei zum Download:

- [Muster.usdz](../muster.usdz)

## Verweise

* [USDZ-Dateiformatspezifikationen](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)
