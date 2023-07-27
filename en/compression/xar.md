{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - Extensible Archive File Format",
  "description":"Learn about XAR file format and APIs that can create and open XAR files.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-13"
}

## What is an XAR file?

A file with .xar (Extensible Archive Format) extension is a UNIX archive that may be in compressed or non-compressed format. It is also used on Mac OS for installation of packages. XAR is open-source and been part of Mac OS X 10.5 for usage with Safari browser.

## XAR File Format

A [XAR](https://github.com/mackyle/xar/wiki/xarformat) file has three main regions.

 * Header
 * Table of Contents
 * Heap

### XAR Header

The XAR header is structured as follow.

|Field|Data Type|Size in Bytes|
---|---|---|
|Magic|Unsigned Int 32|4|
|Size|Unsigned Int 16|2|
|Version|Unsigned Int 16|2|
|TOC Length Compressed|Unsigned Int 64|8|
|TOC Length UnCompressed|Unsigned Int 64|8|
|Checksum|Unsigned Int 32|4|
|Message Digest Name |Null Terminated||

The C structure of XAR header can be defined as follow.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
Note that all fields of the header (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) are always stored in XAR files in network byte (aka big endian) order.

### XAR Table of Contents (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. It is stored in the beginning of the file, making it easy to scan through the archive to extract individual file. The XAR archive lets you compress/encode the individual files in the archive independently using different compression schemes such as [GZIP](/compression/gz/), [BZIP2](/compression/bz2/), and other similar.  

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### Heap

The heap starts immediately after the compressed toc. It is an unstructured heap of data referenced by the TOC. The Offset values listed in TOC start from the beginning of the heap. The length values in the toc refer to the actual number of bytes stored in the heap (compressed or not) whereas the size value refers to the extracted size of the item (after decompressing if necessary).

## References

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))
