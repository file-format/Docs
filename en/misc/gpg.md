{
  "date" : "2022-02-17",
  "keywords" : ["gpg file", "gpg file format", "what is a gpg file", "file", "gpg example", "gpg file extension","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GPG File - GNU Privacy Guard Public Keyring File",
  "description":"Learn about GPG file and APIs that can create and open GPG files.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-02-17"
}

## What is a GPG file?

A GPG file is an encryption/decryption key file that is used by GNU Privacy Guard (GnuPG) encryption program. The GnuPC program itself is based on the OpenPGP standard as defined RFC4880 and is also known as PGP. The key to successful usage of GPG in modern operating system is its versatile key management system. The command line utility of GPG lets it easily integrate with other applications.

## GPG File Format

GPG files are saved as encrypted binary files and of course they are not human readable. To decrypt an encrypted GPG file, you need to use the same secure key. And that is why the internal file format of these files is not known.

## Encrypt and Decrypt Files with GPG on Linux

The GPG command line utility can be used to encrypt and decrypt files on Linux.

### Encrypting a File

A file can be encrypted using the gpg command with the -c (create) option as shown below.

```
gpg -c file1.txt
```
Running this command asks for a keyphrase with which to encrypt the contents of the original file `file1.txt`. This results in creation of the encrypted file file1.txt.gpg.

### Decrypting and Extracting a File

In order to decrypt and extract an encrypted file, the following command can be used.

```
gpg cfile.txt.gpg
```

## References

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)
