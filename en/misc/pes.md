{
  "date": "2021-07-29",
  "keywords": [
    "pes file",
    "pes file format",
    "what is a pes file",
    "file",
    "pes example",
    "pes file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PES File Format - Brother PE Embroidery Format",
  "description": "Learn about PES file format and APIs that can create and open PES files.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pes"
    }
  },
  "lastmod": "2021-07-29"
}

## What is a PES Embroidery file?

The PES embroidery file is a design file that contains instructions for the embroidery/sewing machines. It was developed by Brother Industries for their embroidery machines but were later formalized as general file format. PES files are used by sewing machines to read instructions for stitching a patterns on fabric. These files serve two purposes; first providing design information for PE-Design application developed by Brother Industries and second, providing design name, colors, and embroidery machine codes such as "stop", "jump", and "trim".

## PES File Format - More Information

A PES file is saved to disc in binary file format. It contains multiple sections that has sewing information stored using predefined method. The PES file format is as follow.

 * Version Data - Gives version information and can be any value `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
 * PEC Seek Value - A 4 byte little-endian integer following immediately the version data and represents the seek value for the PEC section that contains design details Information
 * PSE Section - Contains design information relevant to the Brother PE-Design and may be other sewing applications
 * PCE Section - Can be anywhere in the PSE file but referenced by the PEC Seek Value.

## Type of Sewing Machines using PES File

PES files are primarily created by the PE-Design Software used with the Brother sewing machines. Some other machines that may support PES files include Babylock and Bernina home embroidery machines.

## How to Convert PSE Files?

The PE-Design software application can [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) to other formats such as .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd, or .xxx. It can be done using the PE-Design application by opening the file and selecting the Conversion format.

## References

* [PE Design - Instructio Manual](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)
