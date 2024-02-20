{
  "date": "2021-08-10",
  "keywords": [
    ".ova file",
    "file format",
    "what is an .ova file",
    "file",
    "file extension"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about what is a .ova file format and APIs that can create and open ova files.",
  "title": "OVA File Format - Open Virtual Appliance File",
  "linktitle": "OVA",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ova"
    }
  },
  "lastmod": "2022-01-03"
}

## What is an OVA file?

An OVA (Open Virtual Appliance) file is an OVF directory saved as an archive using the .tar archiving format. It is a virtual appliance package file that contains files for distribution of software that runs on a virtual machine. An OVA package contains a [.ovf](/disc-and-media/ovf/) descriptor file, certificate files, an optional [.mf](/programming/mf/) file along with other related files. OVA files have media type as application/ovf.

## OVA File Format

As mentioned, an OVA file is an archive file that is created using the OVF directory in TAR file format. The file itself is saved as a binary file. Most virtualization platforms, such as VMware, Microsoft, Oracle, and Citrix, can install virtual appliances from an OVF file that is a descriptor file having the details of the image to be loaded in virtual machine.

## Advantages of an OVA File

* OVA files are compressed, allowing for faster downloads.
* The vSphere Client validates an OVA file before importing it, and ensures that it is compatible with the intended destination server. If the appliance is incompatible with the selected host, it cannot be imported and an error message appears.
* OVA can encapsulate multi-tiered applications and more than one virtual machine.

## References

* [OVA File Formats and Templates](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
* [OVF File Format Specifications](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)
