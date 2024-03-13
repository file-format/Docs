{
  "date": "2022-05-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBML Fayl Format - Opera Mini Saxlanmış Veb Səhifə Faylı",
  "description": "OBML faylının nə olduğunu və OBML faylını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle": "OBML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-obm-azl"
}
},
  "lastmod": "2022-05-19"
}

## OBML faylı nədir?

OBML (Opera Binary Markup Language) faylı Opera Mini mobil veb brauzeri tərəfindən saxlanılan veb-səhifənin oflayn versiyasıdır. Bu, oflayn rejimdə xüsusi cihazlarda göstərilmək üçün səhifənin bütün elementlərini özündə cəmləşdirən [HTML](/web/html/) fayllarının müstəqil, yığcam versiyasıdır. OBML fayl formatı geniş şəkildə istifadə edilən OBML15 və OBML16 ilə bir neçə versiyaya yüksəldilib. Nəzərə alınmalı vacib məqam hər Opera Mini versiyasının yalnız bir OBML formatına uyğun olmasıdır. Beləliklə, Opera Mini-nin təkmilləşdirilməsi əvvəllər saxlanmış səhifələri oxunaqlı edəcək. OBML faylları HTML və [PDF](/pdf/) formatına çevrilə bilər.

## OBML fayl formatı

OBML fayl formatı Opera-nın xüsusi fayl formatında saxlanılır və onun fayl formatının spesifikasiyası ictimaiyyətə açıq deyil. Bununla belə, [OMBL format](https://github.com/grawity/obml-parser/blob/master/obml.md) strukturunu aşağıdakı kimi deşifrə etmək üçün tərs dizayn edilmişdir.

### OBML Məlumat Növləri

Əks mühəndislik nəticələrinə görə, OBML aşağıdakı primitiv növlərdən istifadə edir:

 * `bayt` – işarəsiz tam ədəd (1 bayt)
 * `qısa` – işarəli tam ədəd (2 bayt, böyük-endian)
 * `orta` – işarəli tam ədəd (3 bayt, böyük-endian)
 * `blob` – { uzunluq: qısa, məlumat: bayt[uzunluq] }
 * `char` – ASCII simvolu olan bayt
 * `string` – UTF-8 kodlu mətni ehtiva edən blob

### OBML Başlığı

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
## İstinadlar

* [OMBL formatı](https://github.com/grawity/obml-parser/blob/master/obml.md)


