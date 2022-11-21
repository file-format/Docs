{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "File", "Ekstensi", "Format File", "Ekstensi File", "html yang dapat diperluas"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Format File Bahasa Markup Hiperteks yang Dapat Diperluas",
  "description":"Pelajari tentang apa itu format file XHTML dan API yang dapat membuat dan membuka file XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu berkas XHTML?

XHTML adalah format file berbasis teks dengan markup dalam XML, menggunakan formulasi ulang HTML 4.0. File-file ini sangat cocok untuk dibuka atau dilihat di browser web. XHTML dirancang agar lebih terstruktur, lebih sedikit scripting, generik; menggunakan semua fasilitas XML yang ada dan lebih banyak perangkat yang independen. XHTML menyediakan kumpulan elemen dan atribut yang bermanfaat, dengan opsi ekstensi yang dikombinasikan dengan style sheet. Atribut digunakan dari kumpulan atribut metadata. XHTML memberikan fleksibilitas dan aksesibilitas dengan mensubordinasikan semua elemen presentasi **[HTML](/id/web/html/)** ke style sheet. Lembar gaya lebih serbaguna daripada elemen presentasi ini. Spesifikasi untuk HTML 4.01, HTML5 dan XHTML sedang dikembangkan secara dinamis oleh World Wide Web Consortium (W3C).

## Sejarah Singkat Format File XHTML

Sejarah XHTML dimulai dengan draft dokumen yang dirilis pada bulan Desember 1998 oleh World Wide Web Consortium. Dokumen ini mengacu pada "Reformulating HTML in XML", sebuah spesifikasi yang disebut XHTML 1.0. Spesifikasi baru ini memformulasi ulang HTML dalam XML menggunakan elemen atau atribut yang ada. Pada Mei 1999, Konsorsium W3 menyatakan bahwa HTML 4.0 telah dibentuk ulang sebagai aplikasi XML. yaitu XHTML. Pada tanggal 26 Januari 2000, spesifikasi pertama yang mendefinisikan XHTML 1.0 dirilis oleh W3C. Selanjutnya pada tanggal 31 Mei 2001, W3C mengumumkan XHTML sebagai bahasa independen dan mulai mengerjakan pengembangan HTML 5.0. Namun, pada tahun 2005, sebuah kelompok kerja (WHATWG) dibentuk yang bertujuan untuk meningkatkan HTML biasa terlepas dari XHTML. WHATWG akhirnya mulai mengerjakan HTML5 secara paralel dengan XHTML 2.

## Format File XHTML

XHTML adalah format, yang merupakan kumpulan dari berbagai jenis dokumen dan modul yang meniru, mengkategorikan, dan memperluas HTML 4. File dalam XHTML berbasis XML, dan ditujukan untuk bekerja dengan agen pengguna berdasarkan XML. File XHTML sesuai dengan XML. Alat XML standar digunakan untuk melihat, mengedit, dan memvalidasi file XHTML. Model Objek Dokumen HTML atau Model Objek Dokumen XML [DOM] aplikasi yang bergantung dapat beroperasi melalui dokumen XHTML. Memilih XHTML hari ini, pengembang konten dapat menikmati semua manfaat terkait XML tanpa mengkhawatirkan kompatibilitas maju atau mundur konten mereka.

Satu set elemen terkait membangun modul dalam XHTML. Modul formulir atau tabel dapat berisi berbagai elemen formulir atau tabel yang dapat ditampilkan di halaman web. Modularisasi bertujuan untuk mengisolasi elemen HTML menjadi sekumpulan elemen terkait. Sehingga pengembang konten dapat memanfaatkan pemilihan modul untuk berbagai jenis perangkat. Selain itu, modul memungkinkan agen pengguna untuk memilih elemen tanpa kehilangan konsistensi dengan standar XHTML. Persyaratan parsing XHTML sama dengan XML sementara HTML mempraktikkannya sendiri.

### Kesesuaian Dokumen

XHTML2 menawarkan spesifikasi yang sesuai dengan dokumen XHTML 1.0, yang menggunakan elemen ruang nama dan atribut dari XML dan XHTML 1.0. Kesesuaian Dokumen terdiri dari dua jenis.

Dokumen yang Sangat Sesuai adalah berbasis XML yang hanya membutuhkan layanan wajib yang ditentukan dalam spesifikasi ini. Kriteria berikut harus dipenuhi untuk file XHTML:

* File harus sesuai dengan batasan yang ditentukan dalam DTD dan Lampiran B.
* Elemen dasar file harus html.
* Elemen dasar file harus berisi deklarasi untuk namespace XHTML dan harus didefinisikan sebagai:

```
http://www.w3.org/1999/xhtml.
```

* Elemen dasar dapat ditulis sebagai:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Lebih awal dari elemen dasar, DOCTYPE harus dideklarasikan, yang pengidentifikasi publiknya harus merujuk salah satu dari tiga definisi tipe dokumen (DTD). Pengidentifikasi sistem dapat dimodifikasi untuk mematuhi konvensi sistem saat ini.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Dalam dokumen XML, tidak perlu menentukan deklarasi XML di semua dokumen; namun pengembang konten tertarik untuk menggunakan deklarasi XML di semua dokumen XHTML mereka. Deklarasi ini wajib baik ketika pengkodean karakter dokumen berbeda dari UTF-8/16 atau tidak ada pengkodean yang ditentukan oleh protokol yang mengatur. Contoh dokumen XHTML berikut mendefinisikan deklarasi XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Agen pengguna yang sesuai harus memenuhi aturan berikut:

* Parsing dan evaluasi dokumen XHTML dilakukan oleh agen pengguna yang memastikan konsistensinya dengan Rekomendasi XML 1.0.
* Dalam hal memvalidasi agen pengguna, ia harus memeriksa validitas dokumen untuk DTD yang direferensikan menurut XML. Saat file XHTML diproses oleh agen pengguna sebagai XML umum, fitur ID tipe akan dikenali sebagai pengidentifikasi fragmen.

Jika agen pengguna menabrak elemen yang tidak dikenal, berikut adalah kriteria wajib yang harus dipenuhinya

* memproses konten elemen yang tidak diketahui itu
* abaikan atribut dan nilainya
* Gunakan nilai atribut yang disediakan sebagai default.

Ketika agen pengguna menemukan deklarasi referensi entitas yang belum diproses sebelumnya, maka itu harus diproses sebagai karakter (dimulai dengan tanda “&” dan diakhiri dengan titik koma). Selama pemrosesan konten, referensi karakter atau entitas karakter yang dapat diprediksi oleh agen pengguna tetapi tidak dapat dirender dapat menggunakan perenderan alternatif apa pun yang menghasilkan makna serupa. Dalam kasus seperti itu, dokumen harus ditampilkan dengan cara yang membuat pengguna jelas tentang fakta bahwa proses rendering belum normal. Untuk memproses spasi, agen pengguna perlu melihat definisi dari karakter CSS [CSS2].

## Kompatibilitas mundur XHTML

Kompatibilitas mundur dokumen XHTML 1. berpengalaman dengan agen pengguna HTML 4, jika aturan yang tepat diikuti. XHTML 1.1 sepenuhnya kompatibel kecuali anotasi ruby, meskipun umumnya diabaikan oleh browser HTML 4. XHTML 2.0 relatif kurang kompatibel, namun masalahnya telah diatasi sampai batas tertentu melalui penggunaan skrip.

## Referensi

* [Sejarah XHTML: Dari 1990-an hingga Hari Ini](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

