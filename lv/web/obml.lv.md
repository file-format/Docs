{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBML faila formāts — Opera Mini saglabātais tīmekļa lapas fails",
  "description": "Uzziniet, kas ir OBML fails un API, kas var izveidot un atvērt OBML failu.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-lvl"
}
},
  "lastmod": "2022-05-19"
}

## Kas ir OBML fails?

OBML (Opera Binary Markup Language) fails ir tīmekļa lapas bezsaistes versija, kas saglabāta, izmantojot Opera Mini mobilo tīmekļa pārlūkprogrammu. Tā ir autonoma, kompakta [HTML](/web/html/) failu versija, kurā ir visi lapas elementi, kas paredzēti attēlošanai noteiktās ierīcēs bezsaistē. OBML faila formāts ir jaunināts uz vairākām versijām, plaši izmantojot OBML15 un OBML16. Svarīgs punkts, kas jāņem vērā, ir tas, ka katra Opera Mini versija ir saderīga tikai ar vienu OBML formātu. Tādējādi, jauninot Opera Mini, iepriekš saglabātās lapas būs lasāmas. OBML failus var konvertēt uz HTML un [PDF](/pdf/).

## OBML faila formāts

OBML faila formāts tiek saglabāts Opera patentētajā faila formātā, un tā faila formāta specifikācijas nav pieejamas publiski. Tomēr [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) tika izstrādāta apgrieztā veidā, lai atšifrētu tās struktūru, kā norādīts tālāk.

### OBML datu tipi

Saskaņā ar apgrieztās inženierijas rezultātiem OBML izmanto šādus primitīvos veidus:

 * baits — neparakstīts vesels skaitlis (1 baits)
 * īss — vesels skaitlis ar zīmi (2 baiti, lielais endians)
 * vidējs — vesels skaitlis ar zīmi (3 baiti, lielais endians)
 * blob — {garums: īss, dati: baits[garums]}
 * char — baits, kas satur ASCII rakstzīmi
 * virkne — lāse, kas satur UTF-8 kodētu tekstu

### OBML galvene

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
## Atsauces

* [OMBL formāts](https://github.com/grawity/obml-parser/blob/master/obml.md)


