{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier OBML - fișierul paginii web salvate Opera Mini",
  "description" :"Aflați despre ce este un fișier OBML și API-urile care pot crea și deschide fișierul OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Ce este un fișier OBML?

Un fișier OBML (Opera Binary Markup Language) este o versiune offline a unei pagini web salvate de browserul web mobil Opera Mini. Este o versiune autonomă, compactă a fișierelor [HTML](/ro/web/html/), care conține toate elementele paginii pentru afișare pe anumite dispozitive în timp ce sunteți offline. Formatul de fișier OBML a fost actualizat la mai multe versiuni, OBML15 și OBML16 fiind utilizate în general. Un punct important de luat în considerare este că fiecare versiune Opera Mini este compatibilă doar cu un format OBML. Astfel, actualizarea Opera Mini va lăsa paginile salvate anterior lizibile. Fișierele OBML pot fi convertite în HTML și [PDF](/ro/pdf/).

## Format de fișier OBML

Formatul de fișier OBML este salvat în formatul de fișier proprietar al Opera, iar specificațiile de format de fișiere ale acestuia nu sunt disponibile public. Cu toate acestea, [formatul OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) a fost proiectat invers pentru a-și decoda structura după cum urmează.

### Tipuri de date OBML

Conform rezultatelor de inginerie inversă, OBML utilizează următoarele tipuri primitive:

* `byte` – întreg fără semn (1 octet)
* `short` – întreg cu semn (2 octeți, big-endian)
* „mediu” – întreg cu semn (3 octeți, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – un octet care conține un caracter ASCII
* `șir` – un blob care conține text codificat UTF-8

### Antet OBML

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
## Referințe

* [Format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

