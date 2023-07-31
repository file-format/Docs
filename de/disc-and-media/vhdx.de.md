{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das VHDX-Dateiformat und APIs, die VHDX-Dateien erstellen und öffnen können.",
  "title" :"VHDX-Dateiformat - Was ist eine VHDX-Datei?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Was ist eine VHDX-Datei?

Eine VHDX-Datei ist eine Disk-Image-Datei im Dateiformat Virtual Hard Disk v2. Es enthält ein vollständiges Betriebssystem, das geladen und wie jede normale Maschine zum Testen von Software oder zum Ausführen von Software verwendet werden kann, die ein bestimmtes Betriebssystem erfordert. Eine VHDX wird, obwohl es sich um ein vollständiges Disk-Image handelt, in einer einzigen Datei gespeichert. Software für virtuelle Maschinen wie Parallels Desktop, Windows Virtual Machine und Virtual Box kann das Disk-Image laden und öffnen.

VHDX-Dateien können mit Hyper-V Manager in [VHD](/de/disc-and-media/vhd/) oder mit VirtualBox in [VDI](/de/disc-and-media/vdi/) konvertiert werden.

## VHDX-Dateiformat – Weitere Informationen

Die Details zum VHDX-Dateiformat sind vollständig dokumentiert und online verfügbar als [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) in der Microsoft-Dokumentation. Es ist eine Erweiterung des VHD-Formats und enthält erweiterte Funktionen. Das VHDX-Dateiformat bietet zusätzliche Funktionen, die auf den Ebenen der virtuellen Festplatte und der virtuellen Festplattendatei verfügbar sind. Es ist optimierter und liefert bessere Ergebnisse für die Konfiguration und die Fähigkeiten der Speicherhardware. VHDX-Dateien können geöffnet werden

### Unterstützung für virtuelle Festplatten in VHDX

Es unterstützt drei Arten von virtuellen Festplatten.

1. **Feste virtuelle Festplatte** – Virtuelle Festplatte mit fest zugewiesener Datengröße. Die Größe der virtuellen Festplatte ändert sich nicht, wenn Daten hinzugefügt oder entfernt werden.

1. **Dynamische virtuelle Festplatte** – Virtuelle Festplatte mit dynamischer Diskgröße. Seine Größe ist zu jedem Zeitpunkt so groß wie die tatsächlich darauf geschriebenen Daten und Metadaten. Die Dateigröße nimmt dynamisch zu, wenn Daten hinzugefügt oder daraus entfernt werden.

1. **Virtuelle Festplatte differenzieren** – Repräsentiert den aktuellen Wert der virtuellen Festplatte als Satz geänderter Blöcke im Vergleich zu einer übergeordneten virtuellen Festplattendatei.

## Verweise

* [VHDX-Dateiformatspezifikationen](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - von Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

