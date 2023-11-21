{
"Datum": "08.06.2023",
  "keywords": [
"vmx-Datei",
"Was ist eine VMX-Datei?",
"VMX-Dateibeispiel",
"Wie öffnet man eine VMX-Datei",
"Was enthält die VMX-Datei",
"Was ist das Format der VMX-Datei?",
"Datei",
"vmx-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "VMX-Dateiformat – VMware Virtual Machine-Konfigurationsdatei",
  "description":"Erfahren Sie mehr über das VMX-Format und APIs, mit denen VMX-Dateien erstellt und geöffnet werden können.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent": "Einstellungen"
}
},
"lastmod": "08.06.2023"
}

## Was ist eine VMX-Datei?

Eine VMX-Datei, auch als Konfigurationsdatei für virtuelle Maschinen bekannt, ist eine Nur-Text-Datei, die von der VMware-Virtualisierungssoftware zum Definieren von Einstellungen und Konfiguration der virtuellen Maschine (VM) verwendet wird. VMX-Dateien enthalten Informationen wie die Hardwarekonfiguration der VM, Zuordnungen virtueller Festplatten, Netzwerkeinstellungen und andere Parameter.

## Beispiel für eine VMX-Datei

Hier ist ein Beispiel dafür, wie eine VMX-Datei aussehen könnte:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Was enthält die VMX-Datei?

Eine VMX-Datei enthält verschiedene Konfigurationseinstellungen für virtuelle Maschinen (VM). Hier sind einige der häufig vorkommenden Einstellungen in VMX-Dateien:

- `.encoding:` Gibt die in der Datei verwendete Zeichenkodierung an.
- `config.version:` Gibt die Version des VMX-Dateiformats an.
- "virtualHW.version:" Gibt die Version der virtuellen Hardware für die VM an.
- "guestOS:" Gibt das in der VM installierte Gastbetriebssystem an.
- `memSize:` Definiert die Menge an Speicher, die der VM zugewiesen wird.
- "displayName:" Legt den Anzeigenamen oder die Bezeichnung für die VM fest.
- "powerType:" Definiert das Energieverhalten für verschiedene Vorgänge (Ausschalten, Einschalten, Zurücksetzen, Suspendieren).
- "floppyX:" Konfigurationseinstellungen im Zusammenhang mit Diskettenlaufwerken, wie z. B. Anwesenheit und Dateizuordnungen.
- `numvcpus:` Gibt die Anzahl der virtuellen CPUs an, die der VM zugewiesen sind.
- "scsiX:" Konfigurationseinstellungen für SCSI-Controller und die zugehörigen virtuellen Festplatten.
- "ethernetX:" Konfigurationseinstellungen für Netzwerkadapter, einschließlich des virtuellen Gerätetyps, des Netzwerknamens und des Adresstyps.
- "ideX:" Konfigurationseinstellungen für IDE-Controller und die zugehörigen virtuellen Festplatten.
- "usbX:" Konfigurationseinstellungen für USB-Geräte, wie z. B. Anwesenheits- und Verbindungsdetails.
- "sound:" Konfigurationseinstellungen für den virtuellen Soundadapter.
- `tools.syncTime:` Gibt an, ob die Zeitsynchronisierung mit dem Hostsystem aktiviert ist.
- `uuid.bios:` Gibt die BIOS-UUID der VM an.
- `uuid.location:` Gibt die Standort-UUID der VM an.

## Wie öffne ich eine VMX-Datei?

Das manuelle Öffnen einer VMX-Datei wird nicht empfohlen. Wenn Sie eine virtuelle Maschine mit VMware Fusion ausführen, lädt die Software die Informationen automatisch aus der VMX-Datei.

Wenn Sie die VMX-Datei jedoch manuell bearbeiten möchten, können Sie dies mit einem beliebigen Texteditor tun, z. B. Notepad (Windows) oder TextEdit (Mac).

## Was ist das Format der VMX-Datei?

Eine VMX-Datei ist eine reine Textdatei mit einem bestimmten Format. Das Format folgt einer Schlüssel-Wert-Paarstruktur, wobei jede Zeile eine separate Konfigurationsoption darstellt.

Das allgemeine Format der VMX-Datei ist wie folgt:

```
key1 = value1
key2 = value2
key3 = value3
```

Jede Zeile besteht aus einem Schlüssel, gefolgt von einem Gleichheitszeichen (=) und einem entsprechenden Wert. Der Schlüssel stellt eine bestimmte Konfigurationseinstellung dar und der Wert stellt den dieser Einstellung zugewiesenen Wert dar.

Beispielsweise gibt "memSize = "8192"" in der VMX-Datei an, dass die Speichergrenze der virtuellen Maschine 8192 MB RAM beträgt.

Das Format der VMX-Datei kann auch Kommentare enthalten, die durch ein Nummernzeichen (#) am Anfang der Zeile gekennzeichnet sind und von der VMware-Software beim Parsen der Datei ignoriert werden. Kommentare werden häufig verwendet, um zusätzliche Informationen oder Erläuterungen zu bestimmten Einstellungen bereitzustellen.

## Verweise
* [Beispiel-VMX-Datei](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




