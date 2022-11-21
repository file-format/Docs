{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File OBML - File Halaman Web Tersimpan Opera Mini",
  "description" :"Pelajari tentang apa itu file OBML dan API yang dapat membuat dan membuka file OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Apa itu file OBML?

File OBML (Opera Binary Markup Language) adalah versi offline halaman web yang disimpan oleh browser web seluler Opera Mini. Ini adalah versi file [HTML](/id/web/html/) mandiri dan ringkas yang berisi semua elemen halaman untuk ditampilkan di perangkat tertentu saat offline. Format file OBML telah ditingkatkan ke beberapa versi dengan OBML15 dan OBML16 digunakan secara luas. Hal penting yang perlu diperhatikan adalah bahwa setiap versi Opera Mini hanya kompatibel dengan satu format OBML. Dengan demikian, pemutakhiran Opera Mini akan membuat halaman yang disimpan sebelumnya dapat dibaca. File OBML dapat dikonversi ke HTML dan [PDF](/id/pdf/).

## Format File OBML

Format file OBML disimpan dalam format file milik Opera dan spesifikasi format filenya tidak tersedia untuk umum. Namun, [format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) direkayasa balik untuk mendekodekan strukturnya sebagai berikut.

### Tipe Data OBML

Sesuai hasil rekayasa balik, OBML menggunakan tipe primitif berikut:

* `byte` – bilangan bulat tak bertanda (1 byte)
* `short` – bilangan bulat bertanda (2 byte, big-endian)
* `medium` – bilangan bulat bertanda (3 byte, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – sebuah byte yang berisi karakter ASCII
* `string` – gumpalan berisi teks yang disandikan UTF-8

### Tajuk OBML

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
## Referensi

* [format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

