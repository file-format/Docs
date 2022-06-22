{
  "date" : "2021-08-10",
  "keywords" : [ ".ovf file", "file format", "what is an .ovf file", "file", "file extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about what is a .ovf file format and APIs that can create and open OVF files.",
  "title" : "OVF File Format - Open Virtualization File",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2022-01-03"
}

## What is an OVF file?

An OVF file is a text file that contains information about the packaging and distribution of a software that runs on a virtual machine. It is formatted as per the [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) that describes all the requirements (such as security, portability, efficiency and extendibility) for running applications on virtual machines. The International Organization for Standardization (ISO) has adopted OVF as ISO 17203 standard.

## Brief History of OVF File Format

OVF file format was introduced by DMTF (Distributed Management Task Force) that creates open manageability standards. It is independent of any particular hypervisor or instruction set architecture. The OVF package contains one or more virtual systems, each of which can be deployed to a virtual machine.

## OVF File Format - More Information

An OVF package consists of multiple files placed in a single directory. Among these, it ocntains exactly one OVF descriptor (with extension .ovf) file that is stored in [XML](/web/xml/) file format. It describes the packaged virtual machine information and metadata information about the OVF package such as:

 * name
 * hardware requirements
 * references to the other files in the OVF package, and
 * human-readable descriptions

Other files that can be found in an OVF package include one or more disk images and optionally certificate files and other auxiliary files.

## References

* [Open Virtualization Format - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF File Format Specifications](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)
