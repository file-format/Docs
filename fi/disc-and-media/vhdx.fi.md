{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Opi VHDX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VHDX-tiedostoja.",
  "title": "VHDX-tiedostomuoto - Mikä on VHDX-tiedosto?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-fix"
}
},
  "lastmod": "2022-07-22"
}

## Mikä on VHDX-tiedosto?

VHDX-tiedosto on levykuvatiedosto Virtual Hard Disk v2 -tiedostomuodossa. Se sisältää koko käyttöjärjestelmän, joka voidaan ladata ja jota voidaan käyttää normaalina koneena ohjelmistojen testaamiseen tai ajettaessa ohjelmistoja, jotka vaativat tietyn käyttöjärjestelmän. Vaikka VHDX on täysi levykuva, se tallennetaan yhteen tiedostoon. Virtuaalikoneohjelmistot, kuten Parallels Desktop, Windows Virtual Machine ja Virtual Box, voivat ladata ja avata levyvedoksen.

VHDX-tiedosto voidaan muuntaa muotoon [VHD](/disc-and-media/vhd/) Hyper-V Managerilla tai [VDI](/disc-and-media/vdi/):ksi VirtualBoxilla.

## VHDX-tiedostomuoto – lisätietoja

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### Tuki virtuaalisille kiintolevyille VHDX:ssä

Se tukee kolmenlaisia virtuaalisia kiintolevyjä.

 1. **Kiinteä virtuaalinen kiintolevy** - Virtuaalinen kiintolevy, johon on varattu kiinteä datakoko. Virtuaalikiintolevyn koko ei muutu, kun tietoja lisätään tai poistetaan.

 1. **Dynamic Virtual Hard Disk** - Virtuaalinen kiintolevy, jossa on dynaaminen levykoko. Sen koko on milloin tahansa yhtä suuri kuin siihen kirjoitettu todellinen data ja metatiedot. Sen tiedostokoko kasvaa dynaamisesti, kun siihen lisätään tai poistetaan tietoja.

 1. **Differing Virtual Hard Disk** - Edustaa virtuaalisen kiintolevyn virtaa modifioitujen lohkojen joukona verrattuna virtuaalisen kiintolevyn ylätiedostoon.

## Viitteet

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD – Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))


