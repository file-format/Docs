{
  "date": "2023-06-08",
  "keywords": [
"vmx fil",
"hvad er en vmx-fil",
"vmx fil eksempel",
"hvordan man åbner vmx fil",
"hvad indeholder vmx-filen",
"hvad er formatet på vmx-filen",
"fil",
"vmx filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VMX-filformat - VMware Virtual Machine Configuration File",
  "description": "Lær om VMX-format og API'er, der kan oprette og åbne VMX-filer.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-da",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## Hvad er en VMX fil?

En VMX-fil, også kendt som virtuel maskine-konfigurationsfil, er en almindelig tekstfil, der bruges af VMware virtualiseringssoftware til at definere indstillinger og konfiguration af virtuel maskine (VM). VMX-filer indeholder information såsom VM's hardwarekonfiguration, virtuelle disk-mappings, netværksindstillinger og andre parametre.

## Eksempel på VMX-fil

Her er et eksempel på, hvordan VMX-filen kan se ud:

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

## Hvad indeholder VMX-filen?

En VMX-fil indeholder forskellige konfigurationsindstillinger for virtuel maskine (VM). Her er nogle af de almindeligt forekommende indstillinger i VMX-filen:

- `.encoding:` Angiver den tegnkodning, der bruges i filen.
- `config.version:` Angiver versionen af VMX-filformatet.
- `virtualHW.version:` Specificerer versionen af den virtuelle hardware til VM'en.
- `guestOS:` Specificerer gæsteoperativsystemet installeret i VM'en.
- `memSize:` Definerer mængden af hukommelse, der er allokeret til VM'en.
- `displayName:` Indstiller displaynavnet eller etiketten for VM'en.
- `powerType:` Definerer strømadfærden for forskellige operationer (sluk, tænd, nulstil, suspender).
- `floppyX:` Konfigurationsindstillinger relateret til diskettedrev, såsom tilstedeværelse og filtilknytning.
- `numvcpus:` Specificerer antallet af virtuelle CPU'er, der er tildelt VM'en.
- `scsiX:` Konfigurationsindstillinger for SCSI-controllere og deres tilknyttede virtuelle diske.
- `ethernetX:` Konfigurationsindstillinger for netværksadaptere, inklusive den virtuelle enhedstype, netværksnavn og adressetype.
- `ideX:` Konfigurationsindstillinger for IDE-controllere og deres tilknyttede virtuelle diske.
- `usbX:` Konfigurationsindstillinger for USB-enheder, såsom tilstedeværelse og forbindelsesdetaljer.
- `lyd:` Konfigurationsindstillinger for den virtuelle lydadapter.
- `tools.syncTime:` Angiver om tidssynkronisering med værtssystemet er aktiveret.
- `uuid.bios:` Specificerer VM'ens BIOS UUID.
- `uuid.location:` Specificerer placeringens UUID for VM'en.

## Hvordan åbner jeg filen VMX?

Det anbefales ikke at åbne en VMX-fil manuelt. Når du kører en virtuel maskine ved hjælp af VMware Fusion, indlæser softwaren automatisk oplysningerne fra VMX-filen.

Men hvis du ønsker at redigere VMX-fil manuelt, kan du gøre det ved at bruge en hvilken som helst teksteditor, f.eks. Notepad (Windows) eller TextEdit (Mac).

## Hvad er formatet på filen VMX?

En VMX-fil er en almindelig tekstfil med et specifikt format. Formatet følger en nøgleværdi-parstruktur, hvor hver linje repræsenterer en separat konfigurationsmulighed.

Det generelle format for VMX-filen er som følger:

```
key1 = value1
key2 = value2
key3 = value3
```

Hver linje består af nøgle efterfulgt af lighedstegn (=) og tilsvarende værdi. Nøglen repræsenterer en specifik konfigurationsindstilling, og værdien repræsenterer den værdi, der er tildelt denne indstilling.

For eksempel angiver `memSize = 8192` i VMX-filen, at den virtuelle maskine-hukommelsesgrænse er 8192 MB RAM.

Formatet på VMX-filen kan også indeholde kommentarer, angivet med et pund-tegn (#) i begyndelsen af linjen, som ignoreres af VMware-software, når filen analyseres. Kommentarer bruges ofte til at give yderligere oplysninger eller forklaringer til specifikke indstillinger.

## Referencer
* [Eksempel på VMX-fil](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





