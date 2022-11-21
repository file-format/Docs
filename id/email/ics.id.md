{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Format Berkas iCalendar",
  "description":"Pelajari tentang format file ICS dan API yang dapat membuat dan membuka file ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file ICS?

Spesifikasi Objek Inti Kalender dan Penjadwalan Internet (iCalendar) adalah standar internet (RFC 2445) untuk bertukar dan menyebarkan acara dan penjadwalan kalender. Format iCalendar dapat dioperasikan, sehingga memastikan pertukaran informasi kalender di antara pengguna yang memiliki aplikasi email berbeda. iCalendar memformat input data sebagai Multipurpose Internet Mail Extensions (MIME) dan memfasilitasi pertukaran objek melalui protokol transport yang berbeda. Protokol transport ini dapat berupa SMTP, HTTP, komunikasi asinkron point-to-point, dan transport jaringan berbasis media fisik.

iCalendar memungkinkan pengguna untuk berbagi acara, tugas yang bergantung pada tanggal/waktu, dan informasi bebas/sibuk melalui email ke pengguna lain yang dapat membalas. File iCalendar disimpan menggunakan sufiks ".ics" ".iCalendar" atau ".ifb" dengan jenis MIME "text/calendar". iCalendar dijaga agar mandiri tanpa ketergantungan protokol transport. Server web (dengan protokol HTTP) dapat mengangkut informasi iCalendar dan halaman web dapat berisi data iCalendar dalam bentuk tersemat menggunakan iCalendar.

## Sejarah Singkat Format File ICS

Pada tahun 1998, Internet Engineering Task Force (IETF) menetapkan iCalendar sebagai standar (RFC 2445). Standar tersebut didokumentasikan oleh Frank Dawson (Lotus Notes Corporation) dan Derik Stenerson (Microsoft). Pada tahun 2009, standar tersebut kembali disempurnakan oleh Bernard Desruisseaux (Oracle) sebagai RFC 5545. Kali ini beberapa fitur baru ditambahkan dan beberapa fitur yang ketinggalan zaman tidak digunakan lagi. Pada tahun 2016, RFC 7986 dirilis dan ditambah dengan RFC iCalendar asli. RFC 7986 menambahkan karakteristik baru ke objek VCALENDAR utama dan fitur pendukung baru juga diperkenalkan untuk sistem konferensi.

## Format File ICS ##

Jenis MIME yang digunakan oleh data iCalendar adalah “teks/kalender”. Set karakter default untuk iCalendar adalah UTF-8, namun dengan menyediakan parameter dalam MIME, set karakter yang berbeda dapat digunakan. File iCalendar berisi bagian, di antara bagian ini "VCALENDAR", adalah bagian global yang merangkum semua bagian lainnya. Bagian VEVENT menentukan acara, VTODO mencantumkan semua item yang harus dilakukan, VJOURNAL berisi entri jurnal, dan VTIMEZONE menentukan informasi zona waktu. beberapa bagian dari kategori serupa diperbolehkan. Untuk banyak acara, beberapa bagian VEVENT dapat ditampilkan dalam file iCalendar.

### Baris Konten ###

Objek iCalendar disusun menjadi baris teks "baris konten" yang berbeda. Dalam format file ini, urutan CRLF mengakhiri baris sedangkan panjang baris dibatasi hingga 75 oktet tidak termasuk jeda baris. Item data yang panjang dapat dibentangkan ke banyak baris.

### Pemisah Daftar dan Bidang ###

Properti dan parameter menentukan daftar nilai yang dipisahkan oleh karakter COMMA. Kutipan-string digunakan untuk nilai parameter berbasis URI. Daftar parameter dapat dibangun oleh nilai properti. Setiap parameter properti dalam daftar ini harus dipisahkan oleh SEMICOLON.

Dalam daftar nilai, SEMICOLON mengisolasi parameter properti dan COMMA memisahkan nilai properti. Contoh diberikan di bawah ini:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Beberapa Nilai

Beberapa properti dapat memiliki beberapa nilai. Cukup menghasilkan baris konten baru dengan nama properti adalah aturan dasar untuk properti multi-nilai. Namun, untuk satu nilai dengan beberapa variasi bahasa tidak boleh menggunakan properti multinilai.

### Konten Biner

Di dalam objek iCalendar, nilai properti dapat mereferensikan data konten biner yang ditempatkan di entitas MIME eksternal menggunakan URI. Konten biner sebaris dapat digunakan dalam situasi khusus dengan parameter "ENCODING", di mana aplikasi perlu mengekspresikan objek iCalendar sebagai entitas tunggal. Contoh berikut menjelaskan properti "LAMPIRKAN" dengan referensi URI:

LAMPIRKAN: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Set karakter

Meskipun skema charset default untuk iCalendar adalah UTF-8 namun tidak ada parameter properti yang ditentukan untuk menentukan charset dari nilai properti. dalam transfer MIME parameter "charset" HARUS digunakan untuk charset yang ada.

## Referensi

* [Spesifikasi Objek Inti Kalender dan Penjadwalan Internet](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

