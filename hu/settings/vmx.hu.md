{
"dátum": "2023-06-08",
  "keywords": [
"vmx fájl",
"mi az a vmx fájl",
"vmx fájl példa",
"hogyan kell megnyitni a vmx fájlt",
"mit tartalmaz a vmx fájl",
"mi a vmx fájl formátuma",
"fájl",
"vmx fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "VMX fájlformátum - VMware virtuális gép konfigurációs fájl",
  "description":"További információ a VMX formátumról és az API-król, amelyek VMX-fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Mi az a VMX fájl?

A VMX fájl, más néven virtuális gép konfigurációs fájl, egy egyszerű szöveges fájl, amelyet a VMware virtualizációs szoftver használ a virtuális gép (VM) beállításainak és konfigurációjának meghatározására. A VMX-fájlok olyan információkat tartalmaznak, mint a virtuális gép hardverkonfigurációja, virtuális lemezleképezések, hálózati beállítások és egyéb paraméterek.

## VMX fájl példa

Íme egy példa arra, hogyan nézhet ki a VMX fájl:

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

## Mit tartalmaz a VMX fájl?

A VMX-fájl különféle konfigurációs beállításokat tartalmaz a virtuális géphez (VM). Íme néhány a VMX fájlban gyakran előforduló beállítások közül:

- `.encoding:` Megadja a fájlban használt karakterkódolást.
- `config.version:` A VMX fájlformátum verzióját jelzi.
- `virtualHW.version:` Megadja a virtuális gép virtuális hardverének verzióját.
- `guestOS:` Megadja a virtuális gépre telepített vendég operációs rendszert.
- `memSize:` Meghatározza a virtuális gép számára lefoglalt memória mennyiségét.
- `displayName:` Beállítja a virtuális gép megjelenítési nevét vagy címkéjét.
- `powerType:` Meghatározza a tápellátás viselkedését a különböző műveletekhez (kikapcsolás, bekapcsolás, visszaállítás, felfüggesztés).
- `floppyX:` Hajlékonylemez-meghajtókkal kapcsolatos konfigurációs beállítások, például jelenlét és fájlleképezés.
- `numvcpus:` Megadja a virtuális géphez rendelt virtuális CPU-k számát.
- `scsiX:` Az SCSI-vezérlők és a hozzájuk tartozó virtuális lemezek konfigurációs beállításai.
- `ethernetX:` A hálózati adapterek konfigurációs beállításai, beleértve a virtuális eszköz típusát, a hálózat nevét és a cím típusát.
- `ideX:` Az IDE-vezérlők és a hozzájuk tartozó virtuális lemezek konfigurációs beállításai.
- `usbX:` Az USB-eszközök konfigurációs beállításai, például a jelenlét és a csatlakozás részletei.
- `hang:` A virtuális hangadapter konfigurációs beállításai.
- `tools.syncTime:` Azt jelzi, hogy az időszinkronizálás a gazdarendszerrel engedélyezve van-e.
- "uuid.bios:" Megadja a virtuális gép BIOS UUID-jét.
- `uuid.location:` Megadja a virtuális gép hely UUID-jét.

## Hogyan lehet megnyitni a VMX fájlt?

A VMX-fájlok kézi megnyitása nem ajánlott. Ha virtuális gépet futtat a VMware Fusion használatával, a szoftver automatikusan betölti az információkat a VMX-fájlból.

Ha azonban manuálisan szeretné szerkeszteni a VMX-fájlt, akkor ezt bármilyen szövegszerkesztővel megteheti, például a Jegyzettömb (Windows) vagy a TextEdit (Mac) segítségével.

## Mi a VMX fájl formátuma?

A VMX fájl egy egyszerű szöveges fájl, meghatározott formátummal. A formátum egy kulcs-érték pár struktúrát követ, ahol minden sor külön konfigurációs lehetőséget jelent.

A VMX fájl általános formátuma a következő:

```
key1 = value1
key2 = value2
key3 = value3
```

Minden sor egy kulcsból, majd egyenlőségjelből (=) és a megfelelő értékből áll. A kulcs egy adott konfigurációs beállítást jelöl, az érték pedig az ehhez a beállításhoz rendelt értéket.

Például a VMX-fájlban a `memSize = "8192"` azt határozza meg, hogy a virtuális gép memóriakorlátja 8192 MB RAM.

A VMX fájl formátuma tartalmazhat megjegyzéseket is, amelyeket egy font jel (#) jelöl a sor elején, amelyeket a VMware figyelmen kívül hagy a fájl elemzésekor. A megjegyzéseket gyakran arra használják, hogy további információkat vagy magyarázatokat adjanak bizonyos beállításokhoz.

## Hivatkozások
* [Minta VMX-fájl](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




