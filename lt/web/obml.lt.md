{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBML failo formatas – „Opera Mini“ išsaugotas tinklalapio failas",
  "description": "Sužinokite, kas yra OBML failas ir API, kurios gali sukurti ir atidaryti OBML failą.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-ltl"
}
},
  "lastmod": "2022-05-19"
}

## Kas yra OBML failas?

OBML (Opera Binary Markup Language) failas yra neprisijungus pasiekiama tinklalapio versija, išsaugota naudojant Opera Mini mobiliąją žiniatinklio naršyklę. Tai savarankiška, kompaktiška [HTML](/web/html/) failų versija, kurioje yra visi puslapio elementai, skirti rodyti konkrečiuose įrenginiuose neprisijungus. OBML failo formatas buvo atnaujintas iki kelių versijų, plačiai naudojamos OBML15 ir OBML16. Svarbu atsižvelgti į tai, kad kiekviena Opera Mini versija yra suderinama tik su vienu OBML formatu. Taigi, atnaujinus Opera Mini, anksčiau išsaugoti puslapiai bus skaitomi. OBML failus galima konvertuoti į HTML ir [PDF](/pdf/).

## OBML failo formatas

OBML failo formatas išsaugomas patentuotu Opera failo formatu ir jo failo formato specifikacijos nėra viešai prieinamos. Tačiau [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) buvo apverstas, kad iššifruotų jo struktūrą taip.

### OBML duomenų tipai

Remiantis atvirkštinės inžinerijos rezultatais, OBML naudoja šiuos primityvius tipus:

 * baitas – sveikasis skaičius be ženklo (1 baitas)
 * short – sveikasis skaičius su ženklu (2 baitai, didelis endianas)
 * vidutinis – sveikasis skaičius su ženklu (3 baitai, big-endianas)
 * blob – {ilgis: trumpas, duomenys: baitas[ilgis]}
 * char – baitas, kuriame yra ASCII simbolis
 * eilutė – blobas, kuriame yra UTF-8 koduotas tekstas

### OBML antraštė

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
## Nuorodos

* [OMBL formatas](https://github.com/grawity/obml-parser/blob/master/obml.md)


