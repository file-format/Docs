{
  "date" : "2019-10-11",
  "keywords" :[ "file osm", "apa itu file osm", "file", "contoh osm", "ekstensi file osm", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Format Berkas OpenStreetMap",
  "description":"Pelajari tentang format file OSM dan API yang dapat membuat dan membuka file OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file OSM?

OpenStreetMap (OSM) adalah kumpulan besar penyimpanan informasi geografis sukarela dalam berbagai jenis file, menggunakan skema pengkodean yang berbeda untuk mengubah data ini menjadi bit dan byte. OSM adalah upaya kolaboratif menuju pembuatan peta dunia yang dapat diedit secara gratis. Keluaran utama dari upaya kolaboratif ini adalah data geografis daripada peta itu sendiri. Kendala penggunaan atau ketersediaan informasi geografis di sebagian besar dunia memicu kebutuhan untuk membuat OSM. Data yang tersedia dari OSM siap untuk menggantikan Google Maps untuk aplikasi klasik (Facebook, Craigslist dll.) dan data default untuk aplikasi penerima GPS.^^ ^^Meskipun kualitas data beragam di seluruh dunia namun data OpenStreetMap dapat dengan mudah dibandingkan dengan paten sumber data.

## Sejarah Singkat ##

Terinspirasi oleh kesuksesan Wikipedia, pada tahun 2004, Steve Coast seorang pengusaha Inggris, membuat proyek pemetaan dunia berbasis komunitas ini di Inggris. Dia awalnya fokus pada pemetaan Britania Raya. OpenStreetMap Foundation pertama kali didirikan pada April 2006 untuk mendukung evolusi, perluasan, dan sirkulasi geospasial gratis bagi siapa saja. Pada bulan Desember 2006, Yahoo membantu OpenStreetMap dengan fotografi udaranya untuk produksi peta. Data jalan lengkap untuk Belanda dan data jalan utama untuk India dan China dikontribusikan ke OSM pada bulan April 2007 oleh Automotive Navigation Data (AND). Pada bulan Desember 2007, Universitas Oxford adalah organisasi terkemuka yang mengintegrasikan data OpenStreetMap ke dalam situs utama mereka. Sejak saat itu, lebih dari 2 juta pengguna terdaftar menyumbangkan data dalam proyek ini menggunakan perangkat GPS, foto udara, dan survei manual. Data kontribusi komunitas ini tersedia di bawah Lisensi Open Database. Sebuah organisasi nirlaba yang terdaftar di Inggris OpenStreetMap Foundation mengelola situs OSM.

## Format File OSM ##

Ada banyak cara dan format file untuk menyimpan data geografis tetapi format file **OSM** dibatasi untuk OpenStreetMap. OSM dirancang khusus dengan format standar yang dimaksudkan untuk dipindahkan dengan mudah melintasi internet. Format pesanan terstruktur, dikodekan dalam XML merupakan file .osm. Di OpenStreetMap ada empat elemen pivot untuk menyimpan struktur data topologi:

{{< figure src="../OSM.png" alt="Format File OSM" >}}


|Node|Cara|Hubungan|Tag
---|---|---|---|
|<ul><li> Mewakili posisi geografis yang disimpan sebagai pasangan lintang dan bujur.</li><li> Digunakan untuk merepresentasikan fitur peta tanpa ukuran, seperti puncak gunung.</li></ul> |<ul><li> Daftar node yang diurutkan, menandakan polyline, atau poligon</li><li> Mewakili fitur linier seperti jalan dan sungai, dan zona, seperti area parkir, hutan, dan taman.</li></ul> |<ul><li> Daftar simpul dan jalan yang diurutkan mewakili hubungan mereka seperti penghalang dan Anda berbelok di jalan, jalan raya menjangkau berbagai jalan dan area yang ada dengan lubang.</li></ul> |<ul><li> Menyimpan metadata tentang objek peta.* Selalu melekat pada simpul, jalan, atau relasi apa pun</li></ul>


Tag digunakan untuk mengkarakterisasi fitur fisik di lapangan (bangunan dan jalan dll.) di OpenStreetMap. Setiap tag menghubungkan karakteristik geografis dari fitur yang diwakili oleh node atau relasi spesifik tersebut. Dalam sistem pemberian tag gratis ini, untuk menggambarkan fitur, jumlah atribut yang tidak terbatas dapat dimasukkan ke dalam peta. Kombinasi kunci dan nilai khusus yang didukung oleh pengguna terdaftar bertindak sebagai standar informal untuk tag yang sering digunakan. Namun, tag baru dapat dibuat kapan pun aspek baru perlu menganalisis atribut fitur yang belum dipetakan sebelumnya. Sebagian besar fitur hanya menggunakan sejumlah kecil tag untuk deskripsi.

Tiga jenis file digunakan oleh OSM untuk menyimpan data utamanya.

OSM menangani semua file ini dengan informasi tentang detail pemformatannya. Tetapi objek internal yang sama diproduksi oleh file-file ini. Untuk file data, flag yang terlihat pada objek OSM selalu benar yang tidak berlaku untuk file riwayat dan perubahan.

Dalam penggunaan umum, ada keragaman dalam format file OSM. Format file menentukan pengkodean konten pada disk atau kabel dalam bit dan byte. OSM mampu membaca dan menulis maksimal format ini.

**XML**

Format OSM asli berbasis XML. Data yang dikembalikan API basis data OSM utama dalam format XML.

**PBF**

Penyandian Protocol Buffer berdiri pada format biner dan salah satu format yang paling ringkas.

**O5M/O5C**

Format berbasis biner lebih sederhana tetapi relatif lebih sedikit digunakan. OSM dapat membaca tetapi tidak dapat menulis format ini.

**OPL**

Format sederhana yang diusulkan untuk digunakan dengan alat baris perintah UNIX standar. Dekat dengan file CSV, memungkinkan satu entitas OSM dalam satu baris.

**DEBUG**

Format berbasis teks yang dimaksudkan untuk dibuat untuk debugging. OSM dapat menulis format ini tetapi tidak dapat membaca.

**LUBANG HITAM**

Format dummy yang membuang semua data. OSM dapat menulis format ini tetapi tidak dapat membaca.

## Penyimpanan Data OSM ##

Database **PostgreSQL** utama OSM menyimpan salinan utama data OSM dengan ekstensi PostGIS. Untuk setiap primitif data, database utama memelihara tabel yang barisnya menyimpan objek individual. Semua suntingan memperbarui basis data ini dan semua format lainnya dibentuk menggunakan basis data ini. Banyak kumpulan database yang dapat diunduh dibuat untuk mentransfer data dari satu tempat ke tempat lain. Dua format, satu menggunakan XML dan lainnya menggunakan Protocol Buffer Binary Format (PBF) menentukan kumpulan ini. Data lengkap disimpan dalam file bernama planet.osm

## Kompresi dalam File OSM ##

Format berbasis teks (XML, OPL, dan Debug) menggunakan kompresi gzip atau bzip2 secara opsional.

## Referensi ##

* [Panduan Format file OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Pelajari OSM](https://learnosm.org/en/osm-data/getting-data/)

