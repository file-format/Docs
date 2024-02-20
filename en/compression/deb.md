{
  "date": "2021-04-08",
  "keywords": [
    "deb file",
    "deb file format",
    "what is a deb file",
    "file",
    "deb example",
    "deb file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "DEB - Bzip Compressed Tar Archive",
  "description": "Learn about DEB file format and APIs that can create and open DEB files.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-deb"
    }
  },
  "lastmod": "2021-04-09"
}

## What is a DEB file?

A file with .deb extension is a Debian binary package file format available for distribution of software packages on Linux OS. It consists of two [TAR](/compression/tar/) archive files. The DPKG provides the mechanism to read and install the DEB packages. DEB packages can be installed using the APT package  software management interface. DEB files have Internet Media Type as `application/vnd.debian.binary-package`.

## DEB File Format

A DEB file consists of two [TAR](/compression/tar/) archive files. One archive holds the control information and another contains the installable data.

### Package Organization

The DEB file is an **ar** archive file that has a magic value of `!<arch>`. Since Debian 0.93, the archiving mechanism of DEB files contains three files in a specific order.

 1. `Debian Binary` - It is destined to have a series of lines, separated by newlines. At present, only a single line is present that describes the version number. The current version number is 2.0.
 1. `Control Archive` - It contains a control.tar archive that has maintainer scripts and meta-information about the package such as package name, version, dependencies and maintainer.
 1. `Data Archive` - It is a tar archive named data.tar and contains the actual installable media files. The archive can be compressed with gz, bz2, lzma or xz, and the file extension of data archive changes accordingly.

### Control Archive

The control archive can include contents as follow.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * `md5sums` -  It contains MD5 checksums of all files in the package in order to detect corrupt or incomplete files.
 * `conffiles` - It lists the files of the package that should be treated as configuration files. Configuration files are not overwritten during an update unless specified.
 * `preinst`, postinst, prerm and postrm - Optional scripts that are executed before or after installing or removing the package
 * `config` is an optional script that supports the debconf configuration mechanism.
 * `shlibs` - It is a list of shared library dependencies.

## References

* [DEB - Wikipedia](https://en.wikipedia.org/wiki/Deb_(file_format))
* [Debian binary package format](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)
