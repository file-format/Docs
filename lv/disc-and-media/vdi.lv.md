{
  "date": "2021-08-11",
  "keywords": [
"vdi fails",
"vdi faila formātā",
"kas ir vdi fails",
"failu",
"vdi piemērs",
"vdi faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par VDI failu formātu un API, kas var izveidot un atvērt VDI failus.",
  "title": "VDI — VirtualBox virtuālā diska attēla fails",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vd-lvi"
}
},
  "lastmod": "2021-08-11"
}

## Kas ir VDI fails?
Fails ar paplašinājumu .vdi ir virtuālā diska attēls; raksturīgs Oracle atvērtā pirmkoda darbvirsmas virtualizācijas programmai VirtualBox. VDI faili tiek izmantoti, lai palaistu VirtualBox virtuālo mašīnu. Virtuālās mašīnas ļauj lietotājiem palaist papildu operētājsistēmas vai programmas vienā datorā. Tādējādi VDI failu priekšrocība ir tāda, ka lietotāji var saglabāt šos diska attēlu failus savā cietajā diskā un var tos palaist, izmantojot emulatorus, kad vien nepieciešams.

## VDI faila formāts
Virtuālais diska attēls (VDI) ir primārais diska faila formāts aktīvi izstrādātam, atvērtā koda Oracle VM, kas pazīstams kā VirtualBox, kas ir uzņēmuma klases virtualizācijas produkts. VDI faila formāts ir paredzēts, lai izveidotu pārnēsājama diska attēlu, ko var viegli palaist, izmantojot citas virtualizācijas programmas. Tā atbalsta gan dinamiski piešķirtu, gan fiksēta izmēra krātuvi. Tas ļauj izvērst attēla failu pēc tā izveides, pat ja tajā jau ir dati.

### Disku virtualizācija
Sistēma emulē cietos diskus VDI diska attēla formātā. VirtualBox virtuālā mašīna var izmantot iepriekšējos diskus, kas izveidoti programmā Microsoft Virtual PC vai VMware, kā arī savu vietējo formātu. VirtualBox var arī izveidot savienojumu ar iSCSI mērķiem un neapstrādātu sadalīšanu resursdatorā, izmantojot vai nu kā virtuālos cietos diskus. VirtualBox emulē IDE (kontrolleri PIIX4 un ICH6), SATA (kontrolleris ICH8M), SAS kontrollerus, kuriem var pievienot cietos diskus, un SCSI.

Atbalsts ir pieejams atvērtajam virtualizācijas formātam (OVF) kopš VirtualBox versijas 2.2.0. Gan ar resursdatoru savienotas fiziskās ierīces, gan ISO attēlus var uzstādīt kā CD vai DVD diskus.
Pēc noklusējuma VirtualBox atbalsta grafiku, izmantojot ar VESA saderīgu pielāgotu virtuālo grafikas karti.

### Virtualizācijas atbalsts Ethernet
VirtualBox virtualizē šādas tīkla interfeisa kartes Ethernet tīkla adapterim:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Serveris (82545EM)
- Intel Pro/1000 T serveris (82543GC)
- Paravirtualizēts tīkla adapteris (virtio-net)

Emulētās tīkla kartes ļauj viesa operētājsistēmām darboties bez nepieciešamības meklēt un instalēt tīkla aparatūras draiverus, jo tās ir pieejamas kā daļa no viesu OS. Īpašs paravirtualizēts tīkla adapteris uzlabo tīkla veiktspēju, samazinot nepieciešamību saskaņot konkrētu aparatūras interfeisu. Tāpēc tas prasa īpašu vadītāja atbalstu viesā.


## Atsauces 

* [VirtualBox — Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)



