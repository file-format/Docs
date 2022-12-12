{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru OBML - soubor webové stránky uložené v Opeře Mini",
  "description" :"Zjistěte, co je soubor OBML a rozhraní API, která mohou vytvořit a otevřít soubor OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Co je soubor OBML?

Soubor OBML (Opera Binary Markup Language) je offline verze webové stránky uložená mobilním webovým prohlížečem Opera Mini. Je to samostatná kompaktní verze souborů [HTML](/cs/web/html/), která obsahuje všechny prvky stránky pro zobrazení na konkrétních zařízeních v režimu offline. Formát souboru OBML byl upgradován na několik verzí, přičemž se obecně používají OBML15 a OBML16. Důležitým bodem, který je třeba mít na paměti, je, že každá verze Opery Mini je kompatibilní pouze s jedním formátem OBML. Upgrade Opery Mini tedy ponechá dříve uložené stránky čitelné. Soubory OBML lze převést do HTML a [PDF](/cs/pdf/).

## Formát souboru OBML

Formát souboru OBML je uložen v proprietárním formátu souboru Opery a jeho specifikace formátu souboru nejsou veřejně dostupné. Nicméně [formát OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) byl reverzně navržen tak, aby dekódoval jeho strukturu následovně.

### Datové typy OBML

Podle výsledků zpětného inženýrství používá OBML následující primitivní typy:

* `byte` – celé číslo bez znaménka (1 bajt)
* `short` – celé číslo se znaménkem (2 bajty, big-endian)
* `medium` – celé číslo se znaménkem (3 bajty, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – bajt obsahující znak ASCII
* `string` – blob obsahující text v kódování UTF-8

### Záhlaví OBML

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
## Reference

* [formát OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

