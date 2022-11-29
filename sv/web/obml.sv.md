{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML-filformat - Opera Mini sparad webbsidafil",
  "description" :"Läs mer om vad en OBML-fil och API:er är som kan skapa och öppna OBML-fil.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Vad är en OBML fil?

En OBML-fil (Opera Binary Markup Language) är en offlineversion av en webbsida som sparas av Opera Minis mobilwebbläsare. Det är en fristående, kompakt version av [HTML](/sv/web/html/)-filerna som innehåller alla delar av sidan för visning på specifika enheter offline. OBML-filformatet har uppgraderats till flera versioner med OBML15 och OBML16 som används i stort. En viktig punkt att tänka på är att varje Opera Mini-version endast är kompatibel med ett OBML-format. Således kommer uppgradering av Opera Mini att göra tidigare sparade sidor läsbara. OBML-filer kan konverteras till HTML och [PDF](/sv/pdf/).

## OBML filformat

OBML-filformatet sparas i Operas proprietära filformat och dess filformatspecifikationer är inte tillgängliga offentligt. [OMBL-format](https://github.com/grawity/obml-parser/blob/master/obml.md) var dock omvänd konstruerad för att avkoda dess struktur enligt följande.

### OBML-datatyper

Enligt de omvända konstruerade resultaten använder OBML följande primitiva typer:

* `byte` – heltal utan tecken (1 byte)
* "kort" – heltal med tecken (2 byte, big-endian)
* `medium` – heltal med tecken (3 byte, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – en byte som innehåller ett ASCII-tecken
* `sträng` – en blob som innehåller UTF-8-kodad text

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
## Referenser

* [OMBL-format](https://github.com/grawity/obml-parser/blob/master/obml.md)

