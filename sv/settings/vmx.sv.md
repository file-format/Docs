{
"date": "2023-06-08",
  "keywords": [
"vmx-fil",
"vad är en vmx-fil",
"vmx fil exempel",
"hur man öppnar vmx-filen",
"vad innehåller vmx-filen",
"vilket är formatet på vmx-filen",
"fil",
"vmx filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "VMX-filformat - VMware Virtual Machine Configuration File",
  "description":"Läs mer om VMX-format och API:er som kan skapa och öppna VMX-filer.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Vad är en VMX fil?

En VMX-fil, även känd som konfigurationsfil för virtuell maskin, är en vanlig textfil som används av VMwares virtualiseringsprogram för att definiera inställningar och konfiguration av virtuell maskin (VM). VMX-filer innehåller information som VM:s hårdvarukonfiguration, virtuella diskmappningar, nätverksinställningar och andra parametrar.

## Exempel på VMX-fil

Här är ett exempel på hur VMX-filen kan se ut:

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

## Vad innehåller VMX-filen?

En VMX-fil innehåller olika konfigurationsinställningar för virtuell maskin (VM). Här är några av de vanligaste inställningarna i VMX-filen:

- `.encoding:` Anger teckenkodningen som används i filen.
- `config.version:` Indikerar versionen av VMX-filformatet.
- `virtualHW.version:` Anger versionen av den virtuella hårdvaran för den virtuella datorn.
- `guestOS:` Anger gästoperativsystemet som är installerat i den virtuella datorn.
- `memSize:` Definierar mängden minne som allokeras till den virtuella datorn.
- `displayName:` Ställer in visningsnamnet eller etiketten för den virtuella datorn.
- `powerType:` Definierar strömbeteendet för olika operationer (ström av, ström på, återställ, avbryt).
- `floppyX:` Konfigurationsinställningar relaterade till diskettenheter, såsom närvaro och filmappningar.
- `numvcpus:` Anger antalet virtuella processorer som tilldelats den virtuella datorn.
- `scsiX:` Konfigurationsinställningar för SCSI-kontroller och deras tillhörande virtuella diskar.
- `ethernetX:` Konfigurationsinställningar för nätverkskort, inklusive typen av virtuell enhet, nätverksnamn och adresstyp.
- `ideX:` Konfigurationsinställningar för IDE-kontroller och deras tillhörande virtuella diskar.
- `usbX:` Konfigurationsinställningar för USB-enheter, såsom närvaro och anslutningsdetaljer.
- `ljud:` Konfigurationsinställningar för den virtuella ljudadaptern.
- `tools.syncTime:` Indikerar om tidssynkronisering med värdsystemet är aktiverat.
- `uuid.bios:` Specificerar BIOS UUID för den virtuella datorn.
- `uuid.location:` Anger platsen UUID för den virtuella datorn.

## Hur öppnar man filen VMX?

Att öppna en VMX-fil manuellt rekommenderas inte. När du kör en virtuell maskin med VMware Fusion, laddar programvaran automatiskt informationen från VMX-filen.

Men om du vill redigera VMX-filer manuellt kan du göra det med valfri textredigerare, t.ex. Notepad (Windows) eller TextEdit (Mac).

## Vilket är formatet på filen VMX?

En VMX-fil är en vanlig textfil med ett specifikt format. Formatet följer en nyckel-värde-parstruktur där varje rad representerar ett separat konfigurationsalternativ.

Det allmänna formatet för VMX-filen är som följer:

```
key1 = value1
key2 = value2
key3 = value3
```

Varje rad består av nyckel följt av likhetstecken (=) och motsvarande värde. Nyckeln representerar en specifik konfigurationsinställning och värdet representerar värdet som tilldelats den inställningen.

Till exempel, `memSize = "8192"` i VMX-filen anger att den virtuella maskinens minnesgräns är 8192 MB RAM.

Formatet för VMX-filen kan också innehålla kommentarer, betecknade med ett pundtecken (#) i början av raden, som ignoreras av VMware-programvaran när filen analyseras. Kommentarer används ofta för att ge ytterligare information eller förklaringar till specifika inställningar.

## Referenser
* [Exempel på VMX-fil](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




