{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about VHDX file format and APIs that can create and open VHDX files.",
  "title": "VHDX File Format - What is a VHDX file?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhdx"
    }
  },
  "lastmod": "2022-07-22"
}

## What is a VHDX file?

A VHDX file is a disk image file in the Virtual Hard Disk v2 file format. It contains an entire operating system that can be loaded and used as any normal machine for testing of software or running software that requires a specific operating system. A VHDX, despite being a full disk image, is stored in a single file. Virtual machine software such as Parallels Desktop, Windows Virtual Machine and Virtual Box can load and open the disk image.

VHDX file can be converted to [VHD](/disc-and-media/vhd/) with Hyper-V Manager, or to [VDI](/disc-and-media/vdi/) with VirtualBox.

## VHDX File Format - More Information

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### Support for Virtual Hard Disks in VHDX

It supports three types of virtual hard disks.

 1. **Fixed Virtual Hard Disk** - Virtual hard disk with fixed data size allocated. The size of the virtual hard disk does not change with addition or removal of data.

 1. **Dynamic Virtual Hard Disk** - Virtual hard disk with dynamic disc size. It size is at any time is as large as the actual data written to it and metadata. Its file size dynamically increases as data is added or removed from it.

 1. **Differencing Virtual Hard Disk** - Represents the current of the virtual hard disk as a set of modified blocks in comparison to a parent virtual hard disk file.

## References

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - by Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))
