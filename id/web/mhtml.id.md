{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml", "file mhtml", "format file mhtml", "jenis file mhtml", "file", "ketik", "apa itu file mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Berkas MIME HTML",
  "description":"Pelajari tentang format file MHTML dan API yang dapat membuat dan membuka file MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file MHTML?

File dengan ekstensi MHTML mewakili format arsip halaman web yang dapat dibuat oleh sejumlah aplikasi berbeda. Format ini dikenal sebagai format arsip karena menyimpan kode **[HTML](/id/web/html/)** web dan resource terkait dalam satu file. Sumber daya ini mencakup semua yang terkait dengan halaman web seperti gambar, applet, animasi, file audio, dan sebagainya. File MHTML dapat dibuka di berbagai aplikasi seperti Internet Explorer dan Microsoft Word. Microsoft Windows menggunakan format file MHTML untuk merekam skenario masalah yang diamati selama penggunaan aplikasi apa pun di Windows yang menimbulkan masalah. Format file MHTML menyandikan konten halaman yang mirip dengan spesifikasi yang ditentukan dalam message/rfc822 yang merupakan spesifikasi terkait email teks biasa. Spesifikasi sebenarnya dari format ini dirincikan oleh [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Format Berkas MHTML

MHTML juga dikenal sebagai Enkapsulasi MIME dari dokumen HTML Agregat karena kemampuannya untuk menyandikan halaman web HTML bersama dengan sumber dayanya ke arsip web tunggal. Sesuai dengan spesifikasi RFC 2557, dokumen agregat adalah pesan berkode MIME yang berisi sumber daya root (objek) serta sumber daya lain yang ditautkan melalui URI. Sumber daya lain tersebut dapat berupa representasi gambar sebaris, lembar gaya, applet, dll. Selain itu, ini dapat menjadi akar dari dokumen multimedia lainnya. Spesifikasi dokumen lengkap untuk format file MHTML dijelaskan dalam [RFC 2557](https://tools.ietf.org/html/rfc2557) dan harus dirujuk untuk segala jenis pengembangan aplikasi untuk membaca/menulis format file ini. Standar tersebut menetapkan bahwa bagian tubuh yang akan direferensikan dapat diidentifikasi baik oleh Content-ID atau Content-Location.

### Header Konten MIME

Header konten MIME, Content-Location, ditentukan untuk menyelesaikan referensi URI ke sumber daya di bagian tubuh lainnya. Header ini dapat muncul di judul pesan atau konten apa pun.

### Tajuk Lokasi-Konten

Content-Location adalah representasi dari URI yang memberi label konten bagian tubuh di mana ia ditempatkan. Nilainya bisa berupa URI absolut atau relatif. Ini dapat digunakan untuk melabeli sumber daya yang tidak dapat diambil kembali oleh beberapa atau semua penerima pesan. Satu pesan hanya diperbolehkan memiliki satu header Content-Location saja. Contoh struktur multibagian/terkait yang berisi bagian tubuh dengan label Content-Location dan Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI Agregat MHTML

URI agregat MHTML berbeda dari URI akarnya. Bidang tajuk Lokasi-Konten harus berlaku untuk keseluruhan agregat jika digunakan dalam tajuk multibagian/tajuk terkait. Demikian pula, kumpulan sumber daya yang diambil dapat berbeda dari kumpulan sumber daya yang diambil menggunakan Content-Locations dari bagian-bagiannya saat URI yang mengacu pada agregat MHTML digunakan untuk mengambil agregat ini. Misalnya, mengambil agregat MHTML mungkin mengembalikan versi lama, sementara mengambil root URI dan objek tertaut in-line-nya mungkin mengembalikan versi yang lebih baru.

## Referensi

* [Enkapsulasi MIME Dokumen Agregat - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Format File MHTML - Oleh Wikipedia](https://en.wikipedia.org/wiki/MHTML)

