{
  "date": "2021-04-08",
  "keywords": [
    "rpm file",
    "rpm file format",
    "what is a rpm file",
    "file",
    "rpm example",
    "rpm file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "RPM - Red Hat Package Manager File",
  "description": "Learn about RPM file format and APIs that can create and open RPM files.",
  "linktitle": "RPM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-rpm"
    }
  },
  "lastmod": "2021-04-09"
}

## What is a RPM file?

A file with .rpm extension is a Red Hat Linux operating system package for installations of programs on Linux systems. The Red Hat Package Manager uses the RPM file format and is free and open-source package management system. Though RPM files can be used as it is for installation of programs, these can be converted to other package formats such as [DEB](/compression/deb/) using Debian program called Alien.

## RPM File Format

An RPM file is a binary that can contain a set of files. Most of the times, RPM files are "binary RPMs" which are the compiled executables of the software. The RPM file can contain source RPMs (SRPMs) that can be used to build the package from the source code. The RPM file format consists of four sections.

 * Lead - It identifies the file as an RPM file
 * Signature - It can be used to ensure integrity and/or authenticity
 * Header - Contains metadata including package name, version, architecture, file list, etc.
 * File Archive - Also known as payload, which usually is in cpio format, compressed with [GZIP](/compression/gz/)

## References

* [RPM - Wikipedia](https://rpm.org)
* [RPM Documentation](https://rpm.org/documentation.html)
