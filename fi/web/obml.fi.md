{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBML-tiedostomuoto - Opera Minin tallennettu verkkosivutiedosto",
  "description": "Opi mikä on OBML-tiedosto ja API:t, jotka voivat luoda ja avata OBML-tiedoston.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-fil"
}
},
  "lastmod": "2022-05-19"
}

## Mikä on OBML-tiedosto?

OBML (Opera Binary Markup Language) -tiedosto on Opera Mini -mobiiliselaimen tallentama verkkosivun offline-versio. Se on itsenäinen, kompakti versio [HTML](/web/html/)-tiedostoista, joka sisältää kaikki sivun elementit, jotka voidaan näyttää tietyillä laitteilla offline-tilassa. OBML-tiedostomuoto on päivitetty useisiin versioihin, joissa OBML15 ja OBML16 ovat käytössä yleisesti. Tärkeä huomioitava seikka on, että jokainen Opera Mini -versio on yhteensopiva vain yhden OBML-muodon kanssa. Siten Opera Minin päivitys jättää aiemmin tallennetut sivut luettavaksi. OBML-tiedostot voidaan muuntaa HTML- ja [PDF](/pdf/)-muotoon.

## OBML-tiedostomuoto

OBML-tiedostomuoto on tallennettu Operan omaan tiedostomuotoon ja sen tiedostomuotomääritykset eivät ole saatavilla julkisesti. {{HYPERLINKKI}} kuitenkin käännettiin purkamaan sen rakenne seuraavasti.

### OBML-tietotyypit

Palautettujen tulosten mukaan OBML käyttää seuraavia primitiivityyppejä:

 * tavu – etumerkitön kokonaisluku (1 tavu)
 * short – etumerkillä varustettu kokonaisluku (2 tavua, big-endian)
 * medium – etumerkillä varustettu kokonaisluku (3 tavua, big-endian)
 * `blob` – { pituus: lyhyt, data: tavu[pituus] }
 * char – tavu, joka sisältää ASCII-merkin
 * merkkijono – blob, joka sisältää UTF-8-koodattua tekstiä

### OBML-otsikko

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
## Viitteet

* [OMBL-muoto](https://github.com/grawity/obml-parser/blob/master/obml.md)


