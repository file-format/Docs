{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ZIM File Format - OpenZIM Archive File",
  "description":"Learn about ZIM file format and APIs that can create and open ZIM files.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2019-12-09"
}

## What is a ZIM file? ##

Files with .zim extension are archives created to store Wiki content offline. It is considered as the most suitable open file format for storing Wikipedia on a USB. It stores site contents in a compact format. Its name comes from "Zeno IMproved" which was the earlier Zeno file format. ZIM is maintained by [openZIM ](https://openzim.org/)project which is sponsored by Wikimedia CH, and supported by the Wikimedia Foundation. ZIM files can be opened by applications such as Kiwix and ZIMReader. OpenZIM project has hosted the implementation of ZIM file format on [Github](https://github.com/openzim) for contribution from OpenSource community.

## ZIM File Format Specifications

ZIM file format was developed on top of [Zeno file format](https://openzim.org/wiki/Zeno_file_format) and is not backwards compatible. The format specifications of ZIM file format are [available online](https://openzim.org/wiki/ZIM_file_format) by openZIM for developer's reference. OpenZIM has provided C++ open source implementation, [LibZim](https://openzim.org/wiki/Zimlib), for reading and writing ZIM files.

ZIM file format uses LZMA2 compression to make the content compact.

{{< figure src="../ZIM_File_Format.png" alt="ZIM File Format" >}}


### ZIM Header

A ZIM file starts with a header that is at offset 0. All the constituents are based on little-endian and all the integers are unsigned integers i.e. uint_16, uint_32, uint_64.

|Field Name	|Type|	Offset|	Length|	Description|
---|---|---|---|---|
|magicNumber|	integer|	0|	4|	Magic number to recognise the file format, must be 72173914 (0x44D495A)|
|majorVersion|	integer|	4|	2|	Major version of the ZIM file format (5 or 6)|
|minorVersion|	integer|	6|	2|	Minor version of the ZIM file format|
|uuid|	integer|	8|	16|	unique id of this zim file|
|articleCount|	integer|	24|	4|	total number of articles|
|clusterCount|	integer|	28|	4|	total number of clusters|
|urlPtrPos|	integer|	32|	8|	position of the directory pointerlist ordered by URL|
|titlePtrPos|	integer|	40|	8|	position of the directory pointerlist ordered by Title|
|clusterPtrPos|	integer|	48|	8|	position of the cluster pointer list|
|mimeListPos|	integer|	56|	8|	position of the MIME type list (also header size)|
|mainPage|	integer|	64|	4|	main page or 0xffffffff if no main page|
|layoutPage|	integer|	68|	4|	layout page or 0xffffffffff if no layout page|
|checksumPos|	integer|	72|	8|	pointer to the md5checksum of this file without the checksum itself. This points always 16 bytes before the end of the file.|

## References ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)
