{
"datum": "2023-06-08",
  "keywords": [
"soubor vmx",
"co je soubor vmx",
"příklad souboru vmx",
"jak otevřít soubor vmx",
"co obsahuje soubor vmx",
"jaký je formát souboru vmx",
"soubor",
"přípona souboru vmx",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru VMX - konfigurační soubor virtuálního stroje VMware",
  "description":"Další informace o formátu VMX a rozhraních API, která mohou vytvářet a otevírat soubory VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Co je soubor VMX?

Soubor VMX, také známý jako konfigurační soubor virtuálního stroje, je prostý textový soubor používaný virtualizačním softwarem VMware k definování nastavení a konfigurace virtuálního stroje (VM). Soubory VMX obsahují informace, jako je hardwarová konfigurace VM, mapování virtuálních disků, nastavení sítě a další parametry.

## Příklad souboru VMX

Zde je příklad toho, jak může soubor VMX vypadat:

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

## Co obsahuje soubor VMX?

Soubor VMX obsahuje různá nastavení konfigurace pro virtuální počítač (VM). Zde jsou některá z běžně se vyskytujících nastavení v souboru VMX:

- `.encoding:` Určuje kódování znaků použité v souboru.
- `config.version:` Označuje verzi formátu souboru VMX.
- `virtualHW.version:` Určuje verzi virtuálního hardwaru pro virtuální počítač.
- `guestOS:` Určuje hostovaný operační systém nainstalovaný ve virtuálním počítači.
- `memSize:` Definuje množství paměti přidělené virtuálnímu počítači.
- `displayName:` Nastaví zobrazovaný název nebo popisek pro virtuální počítač.
- `powerType:` Definuje chování napájení pro různé operace (vypnutí, zapnutí, reset, pozastavení).
- `floppyX:` Nastavení konfigurace týkající se disketových jednotek, jako je přítomnost a mapování souborů.
- `numvcpus:` Udává počet virtuálních CPU přiřazených k virtuálnímu počítači.
- `scsiX:` Nastavení konfigurace pro SCSI řadiče a jejich přidružené virtuální disky.
- `ethernetX:` Nastavení konfigurace pro síťové adaptéry, včetně typu virtuálního zařízení, názvu sítě a typu adresy.
- `ideX:` Nastavení konfigurace pro řadiče IDE a jejich přidružené virtuální disky.
- `usbX:` Nastavení konfigurace pro zařízení USB, jako jsou podrobnosti o přítomnosti a připojení.
- `sound:` Nastavení konfigurace virtuálního zvukového adaptéru.
- `tools.syncTime:` Označuje, zda je povolena synchronizace času s hostitelským systémem.
- `uuid.bios:` Určuje BIOS UUID virtuálního počítače.
- `uuid.location:` Udává UUID umístění virtuálního počítače.

## Jak otevřít soubor VMX?

Ruční otevírání souboru VMX se nedoporučuje. Když spustíte virtuální počítač pomocí VMware Fusion, software automaticky načte informace ze souboru VMX.

Pokud však chcete ručně upravit soubor VMX, můžete tak učinit pomocí libovolného textového editoru, např. Notepad (Windows) nebo TextEdit (Mac).

## Jaký je formát souboru VMX?

Soubor VMX je prostý textový soubor se specifickým formátem. Formát se řídí strukturou páru klíč–hodnota, kde každý řádek představuje samostatnou možnost konfigurace.

Obecný formát souboru VMX je následující:

```
key1 = value1
key2 = value2
key3 = value3
```

Každý řádek se skládá z klíče, za kterým následuje rovnítko (=) a odpovídající hodnota. Klíč představuje konkrétní konfigurační nastavení a hodnota představuje hodnotu přiřazenou tomuto nastavení.

Například `memSize = "8192"` v souboru VMX určuje, že limit paměti virtuálního počítače je 8192 MB RAM.

Formát souboru VMX může také obsahovat komentáře označené znakem libry (#) na začátku řádku, které software VMware při analýze souboru ignoruje. Komentáře se často používají k poskytnutí dalších informací nebo vysvětlení konkrétních nastavení.

## Reference
* [Ukázkový soubor VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




