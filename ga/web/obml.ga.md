{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid OBML - Comhad Leathanach Gréasáin Sábháilte Opera Mini",
  "description": "Foghlaim faoi cad is comhad OBML agus APIs ann ar féidir comhad OBML a chruthú agus a oscailt.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-gal"
}
},
  "lastmod": "2022-05-19"
}

## Cad is comhad OBML ann?

Leagan as líne de leathanach gréasáin a shábháiltear ag brabhsálaí gréasáin soghluaiste Opera Mini é comhad OBML (Opera Binary Markup Language). Is leagan féinchuimsitheach, dlúth é de na comhaid [HTML](/web/html/) ina bhfuil gnéithe uile an leathanaigh le taispeáint ar ghléasanna ar leith agus tú as líne. Tá formáid comhaid OBML uasghrádaithe go leaganacha éagsúla agus OBML15 agus OBML16 in úsáid i gcoitinne. Pointe tábhachtach le tabhairt san áireamh ná nach bhfuil gach leagan de Opera Mini comhoiriúnach ach le formáid OBML amháin. Mar sin, fágfaidh uasghrádú Opera Mini na leathanaigh a sábháladh roimhe seo inléite. Is féidir comhaid OBML a thiontú go HTML agus [PDF](/pdf/).

## Formáid Chomhaid OBML

Déantar formáid comhaid OBML a shábháil i bhformáid comhaid dílseánaigh Opera agus níl a shonraíochtaí formáid comhaid ar fáil go poiblí. Mar sin féin, rinneadh innealtóireacht droim ar ais do [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) chun a struchtúr a dhíchódú mar a leanas.

### Cineálacha Sonraí OBML

De réir na dtorthaí a ndearnadh innealtóireacht droim ar ais, úsáideann OBML na cineálacha primitive seo a leanas:

 * `beart` - slánuimhir gan síniú (1 beart)
 * `gearr` - slánuimhir sínithe (2 beart, endian mór)
 * `meán` - slánuimhir sínithe (3 bytes, mór-endian)
 * `blob` - { fad: gearr, sonraí: beart[fad] }
 * `char` – beart ina bhfuil carachtar ASCII
 * `teaghrán` – blob ina bhfuil téacs ionchódaithe UTF-8

### Ceanntásc OBML

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
## Tagairtí

* [Formáid OMBL]( https://github.com/grawity/obml-parser/blob/master/obml.md)


