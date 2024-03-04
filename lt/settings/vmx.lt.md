{
  "date": "2023-06-08",
  "keywords": [
"vmx failą",
"kas yra vmx failas",
"vmx failo pavyzdys",
"Kaip atidaryti vmx failą",
"kas yra vmx faile",
"koks yra vmx failo formatas",
"failą",
"vmx failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VMX failo formatas – VMware virtualios mašinos konfigūracijos failas",
  "description": "Sužinokite apie VMX formatą ir API, kurios gali kurti ir atidaryti VMX failus.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-lt",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## Kas yra VMX failas?

VMX failas, taip pat žinomas kaip virtualios mašinos konfigūracijos failas, yra paprasto teksto failas, kurį VMware virtualizacijos programinė įranga naudoja virtualiosios mašinos (VM) nustatymams ir konfigūracijai apibrėžti. VMX failuose yra informacijos, tokios kaip VM aparatinės įrangos konfigūracija, virtualaus disko atvaizdai, tinklo nustatymai ir kiti parametrai.

## VMX failo pavyzdys

Štai pavyzdys, kaip gali atrodyti VMX failas:

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

## Kas yra VMX faile?

VMX faile yra įvairių virtualiosios mašinos (VM) konfigūracijos nustatymų. Štai keletas dažniausiai aptinkamų VMX failo nustatymų:

- `.encoding:` Nurodo faile naudojamą simbolių kodavimą.
- `config.version:` Nurodo VMX failo formato versiją.
- VirtualHW.version: Nurodo virtualiosios aparatinės įrangos versiją, skirtą VM.
- `guestOS:` nurodo VM įdiegtą svečio operacinę sistemą.
- `memSize:` apibrėžia VM skirtos atminties kiekį.
- `displayName:` nustato rodomą VM pavadinimą arba etiketę.
- `powerType:` apibrėžia įvairių operacijų (maitinimo išjungimas, įjungimas, atstatymas, sustabdymas) maitinimo elgesį.
- `floppyX:` Konfigūracijos nustatymai, susiję su diskelių įrenginiais, pvz., buvimo ir failų susiejimas.
- `numvcpus:` Nurodo virtualių procesorių, priskirtų VM, skaičių.
- `scsiX:` SCSI valdiklių ir su jais susijusių virtualių diskų konfigūracijos nustatymai.
- ethernetX: tinklo adapterių konfigūracijos nustatymai, įskaitant virtualaus įrenginio tipą, tinklo pavadinimą ir adreso tipą.
- ideX: IDE valdiklių ir su jais susijusių virtualių diskų konfigūracijos nustatymai.
- usbX: USB įrenginių konfigūracijos nustatymai, pvz., buvimo ir ryšio informacija.
- garsas: virtualaus garso adapterio konfigūracijos nustatymai.
- `tools.syncTime:` Nurodo, ar įjungtas laiko sinchronizavimas su pagrindine sistema.
- `uuid.bios:` Nurodo VM BIOS UUID.
- `uuid.location:` nurodo VM vietos UUID.

## Kaip atidaryti VMX failą?

Nerekomenduojama rankiniu būdu atidaryti VMX failo. Kai paleidžiate virtualią mašiną naudodami VMware Fusion, programinė įranga automatiškai įkelia informaciją iš VMX failo.

Tačiau jei norite rankiniu būdu redaguoti VMX failą, galite tai padaryti naudodami bet kurį teksto rengyklę, pvz., Notepad (Windows) arba TextEdit (Mac).

## Koks yra VMX failo formatas?

VMX failas yra paprasto teksto failas su tam tikru formatu. Formatas atitinka rakto ir reikšmių poros struktūrą, kur kiekviena eilutė nurodo atskirą konfigūracijos parinktį.

Bendras VMX failo formatas yra toks:

```
key1 = value1
key2 = value2
key3 = value3
```

Kiekvieną eilutę sudaro raktas, po kurio yra lygybės ženklas (=) ir atitinkama reikšmė. Raktas žymi tam tikrą konfigūracijos nustatymą, o reikšmė – tam nustatymui priskirtą reikšmę.

Pavyzdžiui, memSize = 8192 VMX faile nurodo, kad virtualios mašinos atminties limitas yra 8192 MB RAM.

Į VMX failo formatą taip pat gali būti komentarų, žymimų svaro ženklu (#) eilutės pradžioje, į kuriuos VMware programinė įranga nepaiso analizuodama failą. Komentarai dažnai naudojami norint pateikti papildomos informacijos arba paaiškinti konkrečius nustatymus.

## Nuorodos
* [VMX failo pavyzdys] (https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





