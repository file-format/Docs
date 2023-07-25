{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Pesan Email",
  "description":"Pelajari tentang format file EML dan API yang dapat membuat dan membuka file EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Apa itu file EML?

Format file EML mewakili pesan email yang disimpan menggunakan Outlook dan aplikasi lain yang relevan. Hampir semua klien email mendukung format file ini karena sesuai dengan Standar Format Pesan Internet RFC-822. Microsoft Outlook adalah perangkat lunak default untuk membuka jenis pesan EML. File EML dapat digunakan untuk menyimpan ke disk serta mengirim ke penerima menggunakan protokol komunikasi.

## Sejarah Singkat EML

Spesifikasi format file EML tersedia sesuai [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Format Standar. Sebelum RFC-822, RFC-733 mengatur aturan pertukaran pesan jaringan hingga pada tahun 1982, yang pertama dibuat sebagai peningkatan ke lateral dengan menetapkan standar ARPA. Pada saat yang sama, Microsoft membuat modul COM sendiri untuk pengembangan klien emailnya sendiri yaitu Outlook Express. RFC-822 mengambil jalur untuk ditetapkan sebagai format berpemilik ketika Microsoft menyimpang dari standar terbuka dan membuat format file [PST](/id/email/pst/) tempat email disimpan dalam format database yang sangat terstruktur. Hal ini mengakibatkan masalah bagi pengguna klien email non-Microsoft saat email diteruskan dari Microsoft Outlook.

Itu pada tahun 2001 ketika standar 822 ditingkatkan menjadi 2822 - Format Pesan Internet yang saat ini digunakan untuk membuat, membaca, dan mengirim pesan EML dalam format MIME RFC-822.

## Spesifikasi Format File EML

File EML terdiri dari dua bagian yang berbeda:

* Header - Berisi informasi tentang header pesan
* Badan Pesan - Berisi serangkaian informasi yang dapat mencakup konten pesan, gambar tersemat, dan lampiran

### Informasi Tajuk ###

File EML terdiri dari informasi Header dan badan pesan opsional. Setiap baris header di EML memiliki dua bagian yang dipisahkan oleh tanda titik dua ":". Yang pertama disebut Nama Header dan yang mengikuti titik dua adalah badan header. Misalnya, tajuk tersebut meliputi:

* Alamat email pengirim
* Alamat email penerima
* Subjek Email
* Stempel waktu dan tanggal pesan

**Contoh Tajuk**

Dari:<John@bmw.eml.light.com>

Ke:<Andy@fileformat.com>

Tanggal: Kam, 8 Mar 2018 10:43:37 +0100

Subyek: lampu bmw eml

### Badan Pesan ###

Badan pesan EML berisi informasi utama email dalam bentuk teks, hyperlink, dan lampiran. Badan email dapat berisi teks biasa yang dapat dibaca tetapi tidak perlu. Dalam hal ini, badan pesan bisa kosong atau berisi data lampiran yang disandikan.

Isi badan pesan dijelaskan oleh Tipe-Kontennya yang memungkinkan aplikasi membaca untuk membaca informasi dalam format masing-masing. Ini sebenarnya mewakili sifat dan format dokumen. Struktur tipe MIME atau tipe konten sangat sederhana; itu terdiri dari tipe dan subtipe, dua string, dipisahkan oleh '/'. Tidak ada ruang yang diperbolehkan. `tipe` mewakili kategori dan dapat berupa tipe diskrit atau multibagian. `Subtipe` khusus untuk setiap jenis. Daftar tipe, yang termasuk dalam kategori Content-Type, panjang tetapi beberapa tipe konten yang penting adalah sebagai berikut:


|**Tipe**|**Deskripsi**|**Contoh Subtipe**
---|---|---|
|text|Mewakili format yang dapat dibaca manusia|text/plain, text/html, text/css, text/javascript
|gambar|Mewakili gambar jenis apa pun kecuali video|gambar/bmp, gambar/png, gambar/jpg, gambar/gif
|audio|Mewakili semua format file audio|audio/mdi, audio/wav
|application|Mewakili segala jenis data biner|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Representasi Lampiran di Badan EML ###

Badan EML berisi batasan untuk setiap jenis konten yang dikandungnya. Lampiran dalam badan pesan diidentifikasi oleh Content-Type dan Content-Disposition seperti yang ditunjukkan pada contoh berikut:

Tipe-Konten: teks/polos; charset#"windows-1252"; nama#"apple app store.txt"
Konten-Disposisi: lampiran; namafile#"apple app store.txt"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd02

Seperti dapat dilihat, Content-Disposition yang diatur ke lampiran memungkinkan aplikasi membaca untuk mendapatkan informasi lampiran seperti nama file lampiran dan pengkodean transfer. Informasi header lampiran diikuti oleh konten lampiran yang disandikan yang akan dibaca.

#### Contoh SpreadSheet sebagai Lampiran ####

Tipe Konten: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; nama#"english_spodr.xlsx"
Konten-Disposisi: lampiran; nama file#"english_spodr.xlsx"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd43

## Referensi

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

