{
  "date": "2023-06-08",
  "keywords": [
"vmx failu",
"kas ir vmx fails",
"vmx faila piemērs",
"kā atvērt vmx failu",
"ko satur vmx fails",
"kāds ir vmx faila formāts",
"failu",
"vmx faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VMX faila formāts — VMware virtuālās mašīnas konfigurācijas fails",
  "description": "Uzziniet par VMX formātu un API, kas var izveidot un atvērt VMX failus.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-lv",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## Kas ir VMX fails?

VMX fails, kas pazīstams arī kā virtuālās mašīnas konfigurācijas fails, ir vienkārša teksta fails, ko izmanto VMware virtualizācijas programmatūra, lai definētu virtuālās mašīnas (VM) iestatījumus un konfigurāciju. VMX faili satur tādu informāciju kā VM aparatūras konfigurācija, virtuālā diska kartējumi, tīkla iestatījumi un citi parametri.

## VMX faila piemērs

Šeit ir piemērs tam, kā varētu izskatīties VMX fails:

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

## Ko satur VMX fails?

VMX fails satur dažādus virtuālās mašīnas (VM) konfigurācijas iestatījumus. Šeit ir daži no visbiežāk sastopamajiem iestatījumiem VMX failā:

- `.encoding:` norāda failā izmantoto rakstzīmju kodējumu.
- `config.version:` norāda VMX faila formāta versiju.
- VirtualHW.version: norāda virtuālās mašīnas virtuālās aparatūras versiju.
- `guestOS:` norāda virtuālajā mašīnā instalēto viesa operētājsistēmu.
- `memSize:` definē VM piešķirtās atmiņas apjomu.
- `displayName:` iestata VM parādāmo nosaukumu vai iezīmi.
- `powerType:` definē barošanas uzvedību dažādām darbībām (barošanas izslēgšana, ieslēgšana, atiestatīšana, apturēšana).
- `floppyX:` Ar diskešu diskdziņiem saistīti konfigurācijas iestatījumi, piemēram, klātbūtnes un failu kartējumi.
- `numvcpus:` norāda virtuālajam datoram piešķirto virtuālo centrālo procesoru skaitu.
- `scsiX:` SCSI kontrolleru un ar tiem saistīto virtuālo disku konfigurācijas iestatījumi.
- `ethernetX:` Tīkla adapteru konfigurācijas iestatījumi, tostarp virtuālās ierīces veids, tīkla nosaukums un adreses veids.
- IdeX: IDE kontrolleru un ar tiem saistīto virtuālo disku konfigurācijas iestatījumi.
- `usbX:` USB ierīču konfigurācijas iestatījumi, piemēram, klātbūtne un savienojuma informācija.
- `skaņa:` virtuālā skaņas adaptera konfigurācijas iestatījumi.
- `tools.syncTime:` norāda, vai ir iespējota laika sinhronizācija ar resursdatora sistēmu.
- `uuid.bios:` norāda virtuālās mašīnas BIOS UUID.
- `uuid.location:` norāda virtuālās mašīnas atrašanās vietas UUID.

## Kā atvērt VMX failu?

Nav ieteicams manuāli atvērt VMX failu. Palaižot virtuālo mašīnu, izmantojot VMware Fusion, programmatūra automātiski ielādē informāciju no VMX faila.

Tomēr, ja vēlaties manuāli rediģēt VMX failu, varat to izdarīt, izmantojot jebkuru teksta redaktoru, piemēram, Notepad (Windows) vai TextEdit (Mac).

## Kāds ir VMX faila formāts?

VMX fails ir vienkārša teksta fails ar noteiktu formātu. Formāts atbilst atslēgu un vērtību pāra struktūrai, kur katra rinda apzīmē atsevišķu konfigurācijas opciju.

Vispārējais VMX faila formāts ir šāds:

```
key1 = value1
key2 = value2
key3 = value3
```

Katra rinda sastāv no atslēgas, kam seko vienādības zīme (=) un atbilstošā vērtība. Taustiņš apzīmē konkrētu konfigurācijas iestatījumu, un vērtība apzīmē šim iestatījumam piešķirto vērtību.

Piemēram, memSize = 8192” VMX failā norāda, ka virtuālās mašīnas atmiņas ierobežojums ir 8192 MB RAM.

VMX faila formātā var būt arī komentāri, kas apzīmēti ar mārciņas zīmi (#) rindas sākumā, kurus VMware programmatūra ignorē, parsējot failu. Komentāri bieži tiek izmantoti, lai sniegtu papildu informāciju vai paskaidrojumus par konkrētiem iestatījumiem.

## Atsauces
* [VMX faila paraugs](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





