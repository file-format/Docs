{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML fájlformátum - Opera Mini mentett weboldal fájl",
  "description" :"További információ arról, hogy mi az OBML-fájl és az API-k, amelyek létrehozhatnak és megnyithatnak OBML-fájlt.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Mi az OBML fájl?

Az OBML (Opera Binary Markup Language) fájl az Opera Mini mobilböngésző által mentett weboldal offline változata. Ez a [HTML](/hu/web/html/) fájlok önálló, kompakt változata, amely tartalmazza az oldal összes elemét, hogy offline módban is megjelenhessenek bizonyos eszközökön. Az OBML fájlformátum több verzióra frissítve, az OBML15 és az OBML16 széles körben használatos. Fontos figyelembe venni, hogy minden Opera Mini verzió csak egy OBML formátummal kompatibilis. Így az Opera Mini frissítése a korábban mentett oldalakat olvashatóvá teszi. Az OBML fájlok konvertálhatók HTML és [PDF](/hu/pdf/) formátumba.

## OBML fájlformátum

Az OBML fájlformátum az Opera szabadalmaztatott fájlformátumában van mentve, és a fájlformátum specifikációi nem érhetők el nyilvánosan. Az [OMBL-formátum](https://github.com/grawity/obml-parser/blob/master/obml.md) azonban visszafejtve lett, hogy a következő módon dekódolja a szerkezetét.

### OBML adattípusok

A visszafejtett eredmények szerint az OBML a következő primitív típusokat használja:

* "byte" – előjel nélküli egész szám (1 bájt)
* "short" – előjeles egész szám (2 bájt, big-endian)
* "közepes" – előjeles egész szám (3 bájt, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – ASCII karaktert tartalmazó bájt
* "karakterlánc" – UTF-8 kódolású szöveget tartalmazó blob

### OBML fejléc

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
## Hivatkozások

* [OMBL formátum](https://github.com/grawity/obml-parser/blob/master/obml.md)

