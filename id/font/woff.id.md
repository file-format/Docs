{
  "date" : "2020-08-20",
  "keywords" :[ "file woff", "format file woff", "apa itu file woff", "file", "contoh woff", "ekstensi file woff", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Format File Web Terbuka",
  "description":"File WOFF adalah format font terbuka yang dibuat dalam Format Font Terbuka Web.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Apa itu file WOFF?

File dengan ekstensi .woff adalah file font web berdasarkan Web Open Font Format (WOFF). Ini memiliki wadah terkompresi khusus format berdasarkan jenis font TrueType (.TTF) atau OpenType (.OTT). WOFF diperkenalkan dengan tujuan untuk membedakan font web dari file font yang digunakan dalam aplikasi desktop. Selain itu, format tersebut ditargetkan untuk mengurangi latensi transfer font dari server ke komputer klien melalui jaringan. Tersedia beberapa alat yang dapat mengonversi file WOFF ke TTF dan format file font lainnya.

## **Format File WOFF**

Format font WOFF memampatkan tabel data font dari struktur sfnt berbasis tabel yang digunakan dalam berbagai jenis font seperti TrueType, OpenType, dan Open Font Format. Ini seperti wadah untuk jenis font ini dan juga memiliki ruang untuk menyertakan metadata font dan data penggunaan pribadi untuk dimasukkan ke dalam wadah. Konverter menggunakan file sfnt menjadi file berformat WOFF dan agen pengguna memulihkan file yang disandikan untuk digunakan dengan dokumen web. Perlu dicatat bahwa data font yang dipulihkan sama persis dengan format font input dari semua aspek.

Utilitas file WOFF sering berisi fitur tambahan seperti subset mesin terbang, validasi atau penambahan fitur font tetapi tidak diperlukan. Baik pembuat maupun agen pengguna harus memastikan bahwa validitas data font yang mendasarinya dipertahankan.

### Struktur File WOFF

Struktur file WOFF mirip dengan font sfnt. Itu didasarkan pada direktori tabel yang berisi panjang dan offset untuk setiap tabel data font. Semua tabel diikuti setelah informasi awal ini. File tersebut berisi database font yang sama dengan font aslinya. Urutan tabel juga sama tetapi masing-masing dapat dikompresi. Direktori tabel WOFF menggantikan direktori tabel asli.

File WOFF terdiri dari berikut ini:

* WOFFHeader - File header dengan tipe dan versi font dasar, bersama dengan offset ke metadata dan blok data pribadi.
* TableDirectory - Direktori tabel font, yang menunjukkan ukuran asli, ukuran terkompresi, dan lokasi setiap tabel dalam file WOFF.
* FontTables - Tabel data font dari input font sfnt, dikompresi untuk mengurangi kebutuhan bandwidth.
* ExtendedMetadata - Sebuah blok opsional metadata diperpanjang, diwakili dalam format XML dan dikompresi untuk penyimpanan dalam file WOFF.
* Data Pribadi- Blok data pribadi opsional untuk digunakan oleh perancang font, pengecoran, atau vendor.

### Tajuk WOFF
Header WOFF terdiri dari tanda pengenal yang menunjukkan jenis data yang disertakan dalam file. Header WOFF beserta field-fieldnya adalah sebagai berikut.

|Jenis|Nama Bidang|Deskripsi|
---|---|---|
|UInt32|tanda tangan |0x774F4646 'wOFF' |
|UInt32| rasa |"Versi sfnt" dari font input.|
|UInt32| panjang |Ukuran total file WOFF.|
|UInt16| numTables |Jumlah entri dalam direktori tabel font.|
|UInt16| dipesan |Dicadangkan; setel ke nol.|
|UInt32| totalSfntSize |Ukuran total yang diperlukan untuk data font yang tidak terkompresi, termasuk header sfnt, direktori, dan tabel font (termasuk padding).|
|UInt16| majorVersion |Versi utama dari file WOFF.|
|UInt16| minorVersion |Versi kecil dari berkas WOFF.|
|UInt32| metaOffset |Offset ke blok metadata, dari awal file WOFF.|
|UInt32| metaLength |Panjang blok metadata terkompresi.|
|UInt32| metaOrigLength |Ukuran blok metadata tidak terkompresi.|
|UInt32| privOffset |Offset ke blok data pribadi, dari awal file WOFF.|
|UInt32| privLength |Panjang blok data pribadi.|


## **Referensi**
* [Format File WOFF w3](https://www.w3.org/TR/WOFF/)

