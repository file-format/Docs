{
  "date": "2021-08-11",
  "keywords": [
    "vdi file",
    "vdi file format",
    "what is a vdi file",
    "file",
    "vdi example",
    "vdi file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about VDI file format and APIs that can create and open VDI files.",
  "title": "VDI - VirtualBox Virtual Disk Image File",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vdi"
    }
  },
  "lastmod": "2021-08-11"
}

## What is a VDI file?
A file with .vdi extension is a virtual disk image; specific to the Oracle's open source desktop virtualization program called VirtualBox. The VDI files are used to start the VirtualBox virtual machine. The VMs allow the users to run additional operating systems or programs on a single computer. Hence, the benefit of VDI files is that users can save these disc image files on their hard disk and can run these using emulators whenever they need.

## VDI file format
Virtual Disk Image (VDI) is the primary disk file format for an actively developed, open-source Oracle VM known as VirtualBox, which is an enterprise-class virtualization product. The VDI file format is designed to make a portable disc image which can be easily run using other virtualization programs. It supports both dynamically allocated and fixed-size storage. It allows you to expand an image file after it has been created, even if it already contains data.

### Disc virtualization
The system emulates hard disks in VDI disk image format. A VirtualBox VM can use earlier disks created in Microsoft Virtual PC or VMware, as well as its own native format. The VirtualBox is also capable in connecting to iSCSI targets and raw partitioning on the host, using either as virtual hard disks. VirtualBox emulates IDE (PIIX4 and ICH6 controllers),SATA (ICH8M controller), SAS controllers to which hard drives can be attached and SCSI. 

The support is available for Open Virtualization Format (OVF) since version 2.2.0 of VirtualBox. Both host-connected physical devices and ISO images can be mounted as CD or DVD drives.
By default VirtualBox supports graphics through a VESA compatible custom virtual graphics card.

### Virtualization support for Ethernet
VirtualBox virtualizes the following Network Interface Cards for an Ethernet network adapter:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Desktop (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T Server (82543GC)
- Paravirtualized network adapter (virtio-net)

The emulated network cards enable guest OSs to run without the need to search and install drivers for networking hardware as they are available as part of the guest OS. A special paravirtualized network adapter improves the network performance by cutting down the need to match a specific hardware interface. Therefore, it requires special driver support in the guest.


## References 

* [VirtualBox - by Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)

