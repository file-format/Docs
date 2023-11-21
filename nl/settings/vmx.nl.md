{
"datum": "2023-06-08",
  "keywords": [
"vmx-bestand",
"wat is een vmx-bestand",
"vmx-bestandsvoorbeeld",
"hoe een vmx-bestand te openen",
"wat bevat het vmx-bestand",
"wat is het formaat van het vmx-bestand",
"bestand",
"vmx bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"VMX-bestandsindeling - Configuratiebestand voor virtuele VMware-machines",
  "description":"Leer meer over het VMX-formaat en API's die VMX-bestanden kunnen maken en openen.",
"linktitel": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent":"instellingen"
}
},
"laatste mod": "2023-06-08"
}

## Wat is een VMX-bestand?

Een VMX-bestand, ook wel bekend als configuratiebestand voor virtuele machines, is een tekstbestand dat door VMware-virtualisatiesoftware wordt gebruikt om de instellingen en configuratie van de virtuele machine (VM) te definiëren. VMX-bestanden bevatten informatie zoals de hardwareconfiguratie van de VM, virtuele schijftoewijzingen, netwerkinstellingen en andere parameters.

## VMX-bestandsvoorbeeld

Hier is een voorbeeld van hoe het VMX-bestand eruit zou kunnen zien:

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

## Wat bevat het VMX-bestand?

Een VMX-bestand bevat verschillende configuratie-instellingen voor een virtuele machine (VM). Hier zijn enkele van de vaak voorkomende instellingen in het VMX-bestand:

- `.encoding:` Specificeert de tekencodering die in het bestand wordt gebruikt.
- `config.version:` Geeft de versie van het VMX-bestandsformaat aan.
- `virtualHW.version:` Specificeert de versie van de virtuele hardware voor de VM.
- `guestOS:` Specificeert het gastbesturingssysteem dat in de VM is geïnstalleerd.
- `memSize:` Definieert de hoeveelheid geheugen die aan de VM is toegewezen.
- `displayName:` Stelt de weergavenaam of het label in voor de VM.
- `powerType:` Definieert het energiegedrag voor verschillende bewerkingen (uitschakelen, inschakelen, resetten, onderbreken).
- `floppyX:` Configuratie-instellingen gerelateerd aan diskettestations, zoals aanwezigheid en bestandstoewijzingen.
- `numvcpus:` Specificeert het aantal virtuele CPU's dat aan de VM is toegewezen.
- `scsiX:` Configuratie-instellingen voor SCSI-controllers en de bijbehorende virtuele schijven.
- `ethernetX:` Configuratie-instellingen voor netwerkadapters, inclusief het virtuele apparaattype, netwerknaam en adrestype.
- `ideX:` Configuratie-instellingen voor IDE-controllers en de bijbehorende virtuele schijven.
- `usbX:` Configuratie-instellingen voor USB-apparaten, zoals aanwezigheids- en verbindingsdetails.
- `sound:` Configuratie-instellingen voor de virtuele geluidsadapter.
- `tools.syncTime:` Geeft aan of tijdsynchronisatie met het hostsysteem is ingeschakeld.
- `uuid.bios:` Specificeert de BIOS UUID van de VM.
- `uuid.location:` Specificeert de locatie-UUID van de VM.

## Hoe open je een VMX-bestand?

Het handmatig openen van een VMX-bestand wordt niet aanbevolen. Wanneer u een virtuele machine gebruikt met VMware Fusion, laadt de software automatisch de informatie uit het VMX-bestand.

Als u het VMX-bestand echter handmatig wilt bewerken, kunt u dit doen met een willekeurige teksteditor, bijvoorbeeld Kladblok (Windows) of Teksteditor (Mac).

## Wat is het formaat van een VMX-bestand?

Een VMX-bestand is een tekstbestand met een specifiek formaat. De indeling volgt een sleutel-waardepaarstructuur waarbij elke regel een afzonderlijke configuratieoptie vertegenwoordigt.

Het algemene formaat van het VMX-bestand is als volgt:

```
key1 = value1
key2 = value2
key3 = value3
```

Elke regel bestaat uit een sleutel gevolgd door een gelijkteken (=) en de bijbehorende waarde. De sleutel vertegenwoordigt een specifieke configuratie-instelling en de waarde vertegenwoordigt de waarde die aan die instelling is toegewezen.

`memSize = "8192"` in het VMX-bestand geeft bijvoorbeeld aan dat de geheugenlimiet van de virtuele machine 8192 MB RAM is.

Het formaat van het VMX-bestand kan ook opmerkingen bevatten, aangegeven met een hekje (#) aan het begin van de regel, die door VMware-software worden genegeerd bij het parseren van het bestand. Opmerkingen worden vaak gebruikt om aanvullende informatie of uitleg te geven over specifieke instellingen.

## Referenties
* [Voorbeeld VMX-bestand] (https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




