{
  "date": "2021-08-11",
  "keywords": [
"vdi failą",
"vdi failo formatas",
"kas yra vdi failas",
"failą",
"vdi pavyzdys",
"vdi failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie VDI failo formatą ir API, kurios gali kurti ir atidaryti VDI failus.",
  "title": "VDI – „VirtualBox“ virtualaus disko vaizdo failas",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vd-lti"
}
},
  "lastmod": "2021-08-11"
}

## Kas yra VDI failas?
Failas su plėtiniu .vdi yra virtualaus disko vaizdas; būdinga Oracle atvirojo kodo darbalaukio virtualizacijos programai VirtualBox. VDI failai naudojami virtualiai VirtualBox mašinai paleisti. VM leidžia vartotojams paleisti papildomas operacines sistemas ar programas viename kompiuteryje. Taigi, VDI failų pranašumas yra tas, kad vartotojai gali išsaugoti šiuos disko vaizdo failus savo standžiajame diske ir, kai tik reikia, gali juos paleisti naudodami emuliatorius.

## VDI failo formatas
Virtualusis disko vaizdas (VDI) yra pagrindinis disko failo formatas aktyviai kuriamam atvirojo kodo Oracle VM, žinomas kaip VirtualBox, kuris yra įmonės klasės virtualizacijos produktas. VDI failo formatas yra skirtas sukurti nešiojamojo disko vaizdą, kurį būtų galima lengvai paleisti naudojant kitas virtualizacijos programas. Jis palaiko tiek dinamiškai paskirstytą, tiek fiksuoto dydžio saugyklą. Tai leidžia išplėsti vaizdo failą, kai jis buvo sukurtas, net jei jame jau yra duomenų.

### Disko virtualizavimas
Sistema emuliuoja standžiuosius diskus VDI disko vaizdo formatu. VirtualBox VM gali naudoti ankstesnius diskus, sukurtus Microsoft Virtual PC arba VMware, taip pat savo vietinį formatą. VirtualBox taip pat gali prisijungti prie iSCSI taikinių ir neapdoroto pagrindinio kompiuterio skaidymo, naudojant kaip virtualius standžiuosius diskus. VirtualBox emuliuoja IDE (PIIX4 ir ICH6 valdiklius), SATA (ICH8M valdiklį), SAS valdiklius, prie kurių galima prijungti standžiuosius diskus, ir SCSI.

Atvirojo virtualizacijos formato (OVF) palaikymas pasiekiamas nuo 2.2.0 VirtualBox versijos. Tiek prie pagrindinio kompiuterio prijungti fiziniai įrenginiai, tiek ISO atvaizdai gali būti montuojami kaip CD arba DVD įrenginiai.
Pagal numatytuosius nustatymus VirtualBox palaiko grafiką per su VESA suderinamą tinkintą virtualią grafikos plokštę.

### Virtualizavimo palaikymas Ethernet
VirtualBox virtualizuoja šias tinklo sąsajos plokštes Ethernet tinklo adapteriui:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
– Intel Pro/1000 MT Desktop (82540EM)
– Intel Pro/1000 MT Server (82545EM)
– Intel Pro/1000 T Server (82543GC)
- Paravirtualizuotas tinklo adapteris (virtio-net)

Emuliuojamos tinklo plokštės leidžia svečio OS veikti be reikalo ieškoti ir įdiegti tinklo aparatinės įrangos tvarkykles, nes jos yra kaip svečių OS dalis. Specialus paravirtualizuotas tinklo adapteris pagerina tinklo našumą, sumažindamas poreikį suderinti konkrečią aparatinės įrangos sąsają. Todėl svečiui reikalingas specialus vairuotojo palaikymas.


## Nuorodos 

* [VirtualBox – Vikipedija](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)



