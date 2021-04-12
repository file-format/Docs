{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DAR - Disk Archiver File Format",
  "description":"Learn about DAR file format and APIs that can create and open DAR files.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-09"
}

## What is a DAR file?

A file with .dar extension is a compressed archive created using the DAR Disk archive. It can create backup/archive for full disk or a group of files. It was created to replace the [TAR](/compression/tar/) file format on UNIX OS and can be created as split archive files for large number of files. DAR archive supports option of deleting files from the system which are linked to the main files in the archive. Its capabilities of providing differential, Incremental, and Decremental backup makes it superior than TAR files.

## DAR File Format

DAR files are compressed archives that can use any per-file compression such as [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz or lzma. The exact file format of a DAR file depends on which type of formatting is used to compress the contents of the archive. It also allows optional Blowfish, Twofish, AES, Serpent, Camellia encryption, and public key encryption and signature (OpenPGP).

### DAR Features

Some of the features of DAR file format are as follow.

 * Takes care of any type of inode (directory, plain files, symlinks, special devices, named pipes, sockets, doors, ...)
 * Takes care of hard-linked inodes (hard-linked plain files, char devices, block devices, hard-linked symlinks)
 * Takes care of sparse files
 * Takes care of Linux file Extended Attributes,
 * Takes care of Linux file ACL
 * Takes care of Mac OS X file forks
 * Takes care of some filesystem specific attributes like Birthdate of HFS+ filesystem and immutable, data-journaling, secure-deletion, no-tail-merging, undeletable, noatime attributes of ext2/3/4 filesystem.
 * Per-file compression with gzip, bzip2, lzo, xz or lzma (as opposed to compressing the whole archive). An individual can choose not to compress already compressed files based on their filename suffix.
 * Fast-extracting of files from anywhere in the archive
 * Fast listing of archive contents through saving the catalogue of files in the archive
 * Live filesystem backup: detects when a file has been modified while it was read for backup and can retry saving it up to a given maximum number of retries
 * Hash file (MD5, SHA1 or SHA-512) generated on-fly for each slice, the resulting file is compatible with md5sum or sha1sum, to be able to quickly check each slice's integrity
 * Filesystem independent: it may be used to restore a system to a partition of a different size and/or to a partition with a different filesystem[5]

## How to open DAR file?

DAR files can be opened on Linux Operating System. Some of the software applications that can open RVT files include:

 * DAR (Disk Archive)
 * KDar - the KDE Disk Archiver

## References

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))
