{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML-bestandsindeling - Opera Mini opgeslagen webpaginabestand",
  "description" :"Meer informatie over wat een OBML-bestand is en API's die een OBML-bestand kunnen maken en openen.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Wat is een OBML-bestand?

Een OBML-bestand (Opera Binary Markup Language) is een offline versie van een webpagina die is opgeslagen door de mobiele webbrowser Opera Mini. Het is een op zichzelf staande, compacte versie van de [HTML](/nl/web/html/)-bestanden die alle elementen van de pagina bevat voor weergave op specifieke apparaten terwijl ze offline zijn. Het OBML-bestandsformaat is geüpgraded naar verschillende versies waarbij OBML15 en OBML16 in het algemeen worden gebruikt. Een belangrijk punt om in overweging te nemen is dat elke Opera Mini-versie slechts compatibel is met één OBML-formaat. Als u Opera Mini upgradet, blijven eerder opgeslagen pagina's dus leesbaar. OBML-bestanden kunnen worden geconverteerd naar HTML en [PDF](/nl/pdf/).

## OBML-bestandsindeling

Het OBML-bestandsformaat wordt opgeslagen in het eigen bestandsformaat van Opera en de specificaties voor het bestandsformaat zijn niet openbaar beschikbaar. [OMBL-formaat](https://github.com/grawity/obml-parser/blob/master/obml.md) is echter reverse-engineered om de structuur als volgt te decoderen.

### OBML-gegevenstypen

Volgens de reverse-engineering-resultaten gebruikt OBML de volgende primitieve typen:

* `byte` – geheel getal zonder teken (1 byte)
* `short` – ondertekend geheel getal (2 bytes, big-endian)
* `medium` – ondertekend geheel getal (3 bytes, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – een byte met een ASCII-teken
* `string` – een blob met UTF-8-gecodeerde tekst

### OBML-koptekst

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
## Referenties

* [OMBL-formaat](https://github.com/grawity/obml-parser/blob/master/obml.md)

