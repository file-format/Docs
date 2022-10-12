{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf-Datei", "Dateiformat", "Was ist eine .ovf-Datei", "Datei", "Dateierweiterung"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie, was ein .ovf-Dateiformat und APIs sind, die OVF-Dateien erstellen und öffnen können.",
  "title" :"OVF-Dateiformat - Virtualisierungsdatei öffnen",
  "linktitle" :"OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Was ist eine OVF-Datei?

Eine OVF-Datei ist eine Textdatei, die Informationen über das Packen und Verteilen einer Software enthält, die auf einer virtuellen Maschine ausgeführt wird. Es ist gemäß den [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) formatiert, die alle Anforderungen (wie Sicherheit, Portabilität, Effizienz und Erweiterbarkeit) für die Ausführung von Anwendungen auf virtuellen Maschinen beschreiben. Die Internationale Organisation für Normung (ISO) hat OVF als ISO 17203-Standard übernommen.

## Kurze Geschichte des OVF-Dateiformats

Das OVF-Dateiformat wurde von der DMTF (Distributed Management Task Force) eingeführt, die offene Verwaltbarkeitsstandards schafft. Es ist unabhängig von einer bestimmten Hypervisor- oder Befehlssatzarchitektur. Das OVF-Paket enthält ein oder mehrere virtuelle Systeme, die jeweils auf einer virtuellen Maschine bereitgestellt werden können.

## OVF-Dateiformat - Weitere Informationen

Ein OVF-Paket besteht aus mehreren Dateien, die in einem einzigen Verzeichnis abgelegt werden. Unter diesen enthält es genau eine OVF-Deskriptordatei (mit der Erweiterung .ovf), die im Dateiformat [XML](/de/web/xml/) gespeichert ist. Es beschreibt die gepackten Informationen der virtuellen Maschine und die Metadateninformationen zum OVF-Paket, z. B.:

* Name
* Hardware-Anforderungen
* Verweise auf die anderen Dateien im OVF-Paket und
* menschenlesbare Beschreibungen

Andere Dateien, die in einem OVF-Paket zu finden sind, umfassen ein oder mehrere Disk-Images und optional Zertifikatsdateien und andere Hilfsdateien.

## Verweise

* [Offenes Virtualisierungsformat - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF-Dateiformatspezifikationen](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

