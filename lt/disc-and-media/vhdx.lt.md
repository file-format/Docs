{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie VHDX failo formatą ir API, kurios gali kurti ir atidaryti VHDX failus.",
  "title": "VHDX failo formatas – kas yra VHDX failas?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-ltx"
}
},
  "lastmod": "2022-07-22"
}

## Kas yra VHDX failas?

VHDX failas yra disko vaizdo failas virtualiojo standžiojo disko v2 failo formatu. Jame yra visa operacinė sistema, kurią galima įkelti ir naudoti kaip bet kurį įprastą įrenginį programinei įrangai arba programinei įrangai, kuriai reikia konkrečios operacinės sistemos, išbandyti. Nepaisant to, kad VHDX yra viso disko vaizdas, jis yra saugomas viename faile. Virtualios mašinos programinė įranga, pvz., Parallels Desktop, Windows Virtual Machine ir Virtual Box, gali įkelti ir atidaryti disko vaizdą.

VHDX failą galima konvertuoti į [VHD](/disc-and-media/vhd/) naudojant Hyper-V Manager arba į [VDI](/disc-and-media/vdi/) naudojant VirtualBox.

## VHDX failo formatas – daugiau informacijos

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### Virtualių standžiųjų diskų palaikymas VHDX

Jis palaiko trijų tipų virtualius standžiuosius diskus.

 1. **Fiksuotas virtualus standusis diskas** – virtualus standusis diskas su fiksuotu duomenų dydžiu. Pridedant ar pašalinant duomenis, virtualaus standžiojo disko dydis nesikeičia.

 1. **Dynamic Virtual Hard Disk** – virtualus standusis diskas su dinaminio disko dydžiu. Jo dydis bet kuriuo metu yra tiek pat, kiek į jį įrašyti faktiniai duomenys ir metaduomenys. Jo failo dydis dinamiškai didėja, kai duomenys pridedami arba iš jo pašalinami.

 1. **Skirtingas virtualus standusis diskas** – rodo virtualiojo standžiojo disko srovę kaip modifikuotų blokų rinkinį, palyginti su pagrindinio virtualiojo standžiojo disko failu.

## Nuorodos

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD – pateikė Vikipedija](https://en.wikipedia.org/wiki/VHD_(file_format))


