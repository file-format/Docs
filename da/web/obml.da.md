{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBML-filformat - Opera Mini-gemt websidefil",
  "description": "Lær om, hvad en OBML-fil og API'er er, der kan oprette og åbne OBML-fil.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-dal"
}
},
  "lastmod": "2022-05-19"
}

## Hvad er en OBML fil?

En OBML-fil (Opera Binary Markup Language) er en offlineversion af en webside, der er gemt af Opera Mini-mobilwebbrowseren. Det er en selvstændig, kompakt version af [HTML](/web/html/)-filerne, der indeholder alle elementerne på siden til visning på bestemte enheder, mens den er offline. OBML-filformatet er opgraderet til flere versioner, hvor OBML15 og OBML16 bruges som helhed. Et vigtigt punkt at huske på er, at hver Opera Mini-version kun er kompatibel med ét OBML-format. Således vil opgradering af Opera Mini efterlade tidligere gemte sider læsbare. OBML-filer kan konverteres til HTML og [PDF](/pdf/).

## OBML filformat

OBML-filformatet gemmes i Operas proprietære filformat, og dets filformatspecifikationer er ikke offentligt tilgængelige. Imidlertid blev [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) omvendt manipuleret for at afkode dens struktur som følger.

### OBML-datatyper

I henhold til de omvendt manipulerede resultater bruger OBML følgende primitive typer:

 * byte – heltal uden fortegn (1 byte)
 * kort - heltal med fortegn (2 bytes, big-endian)
 * `medium` – heltal med fortegn (3 bytes, big-endian)
 * `blob` – { length: short, data: byte[length] }
 * `char` – en byte, der indeholder et ASCII-tegn
 * streng – en klat, der indeholder UTF-8-kodet tekst

### OBML-header

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
## Referencer

* [OMBL-format](https://github.com/grawity/obml-parser/blob/master/obml.md)


