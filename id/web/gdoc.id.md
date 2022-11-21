{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File GDOC - Pintasan Google Dokumen",
  "description":"Pelajari tentang apa itu file GDOC dan API yang dapat membuat dan membuka file GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Apa itu file GDOC?

File GDOC adalah file pintasan yang mengarah ke file yang terletak di Google Drive, layanan penyimpanan dokumen berbasis cloud. Saat klien Google Drive diinstal di komputer dan dokumen dibuat di dalamnya, drive membuat dokumen di penyimpanan cloud online dan menulis [URL](/id/web/url/) dokumen ini di file GDOC di Google lokal folder drive. Saat file pintasan ini diklik dua kali, browser web default membuka dokumen dari lokasi [URL](/id/web/url/). Jika file pintasan ini dipindahkan dari folder ini, tautan ke dokumen online terputus.

## Format File GDOC - Informasi Lebih Lanjut

File GDOC berisi pintasan ke dokumen online yang ditulis dalam format file [JSON](/id/web/json/). Browser yang membuka file GDOC membaca informasi URL dan membuka dokumen tertaut untuk ditampilkan asalkan pengguna masuk ke akun Google tempat dokumen disimpan. File GDOC tidak berisi konten dokumen.

### Contoh Berkas GDOC

File GDOC dapat dibuka di editor teks dan isinya seperti berikut.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Seperti dapat dilihat, isinya diformat dalam JSON yang memiliki URL dokumen dan ID dokumen terkait.

## Referensi

* [Google Dokumen tidak membuka file gdoc atau docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=id )

