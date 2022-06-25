{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PET File Format - Puppy Linux Install Package File",
  "description":"Learn about PET file format and APIs that can create and open PET files.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-06-23"
}

## What is a Linux PET file?

A PET file is an application installation package file created and used with PuppyLinux variant of Linux Operating System. It is created as a compressed [TGZ](/compression/tgz/) file that reduces the file size of the compressed archive. The integrity of PET file format is ensured by the md5sum checksum that is appended to the end of the file for verification at the remote end. PET files can be extracted using the standard TGZ file extractor and WinRAR. PET files replaced the old [PUP](/compression/pup/) package installation files.

## PET File Format

PET files are saved to disc as compressed archives in binary file format. However, the internal file format details of PET file format is not known. Similar to [.exe](/executable/exe/) and [.msi](/executable/msi/) package installation files, the PET files start an installation when they are executed.

## References

 * [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
 * [Index of PuppyLinux PET packages](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)
