{
  "date": "2021-08-11",
  "keywords": [
"vdi fil",
"vdi filformat",
"hvad er en vdi-fil",
"fil",
"vdi eksempel",
"vdi filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om VDI-filformater og API'er, der kan oprette og åbne VDI-filer.",
  "title": "VDI - VirtualBox Virtual Disk Image File",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vd-dai"
}
},
  "lastmod": "2021-08-11"
}

## Hvad er en VDI fil?
En fil med filtypenavnet .vdi er et virtuelt diskbillede; specifikt for Oracles open source desktop-virtualiseringsprogram kaldet VirtualBox. VDI-filerne bruges til at starte den virtuelle VirtualBox-maskine. VM'erne giver brugerne mulighed for at køre yderligere operativsystemer eller programmer på en enkelt computer. Derfor er fordelen ved VDI-filer, at brugere kan gemme disse diskbilledfiler på deres harddisk og kan køre disse ved hjælp af emulatorer, når de har brug for det.

## VDI filformat
Virtual Disk Image (VDI) er det primære diskfilformat for en aktivt udviklet, open source Oracle VM kendt som VirtualBox, som er et virtualiseringsprodukt i virksomhedsklassen. VDI-filformatet er designet til at lave et bærbart diskbillede, som nemt kan køres ved hjælp af andre virtualiseringsprogrammer. Det understøtter både dynamisk allokeret og fast størrelse opbevaring. Det giver dig mulighed for at udvide en billedfil, efter at den er blevet oprettet, selvom den allerede indeholder data.

### Diskvirtualisering
Systemet emulerer harddiske i VDI-diskimage-format. En VirtualBox VM kan bruge tidligere diske, der er oprettet i Microsoft Virtual PC eller VMware, såvel som sit eget oprindelige format. VirtualBox er også i stand til at oprette forbindelse til iSCSI-mål og rå partitionering på værten, ved at bruge enten som virtuelle harddiske. VirtualBox emulerer IDE (PIIX4- og ICH6-controllere), SATA (ICH8M-controller), SAS-controllere, som harddiske kan tilsluttes og SCSI.

Supporten er tilgængelig for Open Virtualization Format (OVF) siden version 2.2.0 af VirtualBox. Både værtsforbundne fysiske enheder og ISO-billeder kan monteres som cd- eller dvd-drev.
Som standard understøtter VirtualBox grafik via et VESA-kompatibelt brugerdefineret virtuelt grafikkort.

### Virtualiseringsunderstøttelse for Ethernet
VirtualBox virtualiserer følgende netværkskort til en Ethernet-netværksadapter:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T Server (82543GC)
- Paravirtualiseret netværksadapter (virtio-net)

De emulerede netværkskort gør det muligt for gæsteoperativsystemer at køre uden behov for at søge og installere drivere til netværkshardware, da de er tilgængelige som en del af gæsteoperativsystemet. En speciel paravirtualiseret netværksadapter forbedrer netværkets ydeevne ved at skære ned på behovet for at matche en specifik hardwaregrænseflade. Derfor kræver det særlig chaufførstøtte hos gæsten.


## Referencer 

* [VirtualBox - af Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)



