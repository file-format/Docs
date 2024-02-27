{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om VHDX-filformat og API'er, der kan oprette og åbne VHDX-filer.",
  "title": "VHDX-filformat - Hvad er en VHDX-fil?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-dax"
}
},
  "lastmod": "2022-07-22"
}

## Hvad er en VHDX fil?

En VHDX-fil er en diskbilledfil i filformatet Virtual Hard Disk v2. Den indeholder et helt operativsystem, der kan indlæses og bruges som enhver normal maskine til test af software eller kørende software, der kræver et specifikt operativsystem. En VHDX er, på trods af at den er et fuld diskbillede, gemt i en enkelt fil. Virtuel maskine software såsom Parallels Desktop, Windows Virtual Machine og Virtual Box kan indlæse og åbne diskbilledet.

VHDX-fil kan konverteres til [VHD](/disc-and-media/vhd/) med Hyper-V Manager eller til [VDI](/disc-and-media/vdi/) med VirtualBox.

## VHDX-filformat - flere oplysninger

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### Understøttelse af virtuelle harddiske i VHDX

Den understøtter tre typer virtuelle harddiske.

 1. **Fixed Virtual Hard Disk** - Virtuel harddisk med fast datastørrelse allokeret. Størrelsen på den virtuelle harddisk ændres ikke ved tilføjelse eller fjernelse af data.

 1. **Dynamisk virtuel harddisk** - Virtuel harddisk med dynamisk diskstørrelse. Dens størrelse er til enhver tid lige så stor som de faktiske data, der er skrevet til den og metadata. Dens filstørrelse øges dynamisk, efterhånden som data tilføjes eller fjernes fra den.

 1. **Differentiering af virtuel harddisk** - Repræsenterer strømmen af den virtuelle harddisk som et sæt af modificerede blokke i sammenligning med en overordnet virtuel harddiskfil.

## Referencer

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - af Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))


