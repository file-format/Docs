{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OBML File Format - Opera Mini Saved Webpage File",
  "description" : "Learn about what is a OBML file and APIs that can create and open OBML file.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2022-05-19"
}

## What is an OBML file?

An OBML (Opera Binary Markup Language) file is an offline version of a webpage saved by Opera Mini mobile web browser. It is a self-contained, compact version of the [HTML](/web/html/) files that contains all the elements of the page for display on specific devices while offline. The OBML file format has upgraded to several versions with OBML15 and OBML16 being used at large. An important point to keep in consideration is that each Opera Mini version is only compatible with one OBML format. Thus, upgrading of Opera Mini will leave previously saved pages readable. OBML files can be converted to HTML and [PDF](/pdf/).

## OBML File Format

OBML file format is saved in Opera's proprietary file format and its file format specifications are not available publicly. However, [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) was reverse engineered to decode its structure as follow.

### OBML Data Types

As per the reverse engineered results, OBML uses the following primitive types:

 * `byte` – unsigned integer (1 byte)
 * `short` – signed integer (2 bytes, big-endian)
 * `medium` – signed integer (3 bytes, big-endian)
 * `blob` – { length: short, data: byte[length] }
 * `char` – a byte containing an ASCII character
 * `string` – a blob containing UTF-8 encoded text

### OBML Header

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## References

* [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md)
