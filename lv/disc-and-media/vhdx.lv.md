{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par VHDX failu formātu un API, kas var izveidot un atvērt VHDX failus.",
  "title": "VHDX faila formāts — kas ir VHDX fails?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-lvx"
}
},
  "lastmod": "2022-07-22"
}

## Kas ir VHDX fails?

VHDX fails ir diska attēla fails virtuālā cietā diska v2 faila formātā. Tajā ir visa operētājsistēma, kuru var ielādēt un izmantot kā jebkuru parastu iekārtu programmatūras testēšanai vai programmatūras palaišanai, kurai nepieciešama noteikta operētājsistēma. Lai gan VHDX ir pilns diska attēls, tas tiek saglabāts vienā failā. Virtuālās mašīnas programmatūra, piemēram, Parallels Desktop, Windows Virtual Machine un Virtual Box, var ielādēt un atvērt diska attēlu.

VHDX failu var konvertēt uz [VHD](/disc-and-media/vhd/), izmantojot Hyper-V Manager, vai par [VDI](/disc-and-media/vdi/), izmantojot VirtualBox.

## VHDX faila formāts — plašāka informācija

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### Atbalsts virtuālajiem cietajiem diskiem VHDX

Tā atbalsta trīs veidu virtuālos cietos diskus.

 1. **Fiksēts virtuālais cietais disks** — virtuālais cietais disks ar piešķirto fiksēto datu lielumu. Virtuālā cietā diska lielums nemainās, pievienojot vai noņemot datus.

 1. **Dynamic Virtual Hard Disk** — virtuālais cietais disks ar dinamisku diska izmēru. Tā lielums jebkurā laikā ir tikpat liels kā tajā ierakstītie faktiskie dati un metadati. Tā faila lielums dinamiski palielinās, kad dati tiek pievienoti vai noņemti no tā.

 1. **Atšķirīgais virtuālais cietais disks** — attēlo virtuālā cietā diska strāvu kā modificētu bloku kopu salīdzinājumā ar vecāks virtuālā cietā diska failu.

## Atsauces

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD — Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))


