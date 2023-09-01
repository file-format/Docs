{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "ekstensi", "file", "format file", "Jenis File BAK", "Ekstensi File BAK", "Tipe File Basis Data", "Format File Basis Data", "File Basis Data" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file BAK dan API yang dapat membuat dan membuka file BAK.",
  "title" :"Format File BAK - File Cadangan Basis Data",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## Apa itu file BAK?

File dengan ekstensi .bak biasanya merupakan file cadangan yang digunakan oleh berbagai perangkat lunak untuk menyimpan cadangan data. Dari perspektif basis data, file BAK digunakan oleh Microsoft SQL Server untuk menyimpan konten basis data. Semua data dan file yang terkait dengan database disimpan dalam format file ini untuk diambil jika database rusak atau tidak valid karena alasan apa pun. File cadangan dapat disimpan dan diindeks di server lain untuk tujuan keamanan. Beberapa aplikasi dapat membuat file BAK seperti SQL Server Management Studio, Transact-SQL, dan Windows PowerShell.

## Format File BAK

Detail internal file BAK tidak diketahui tetapi diasumsikan secara luas bahwa itu didasarkan pada Microsoft Tape Format (MTF). Spesifikasi MTF tersedia dan dapat dirujuk untuk memahami struktur file. Dokumen tersebut memberikan detail tentang penyimpanan MTF untuk siapa saja yang memiliki pengetahuan umum tentang operasi manajemen penyimpanan, tape drive, dan sistem file.

### Kumpulan Data

Kumpulan data adalah kumpulan objek yang ditulis ke media penyimpanan (tape, disk optik, dll.) Selama pencadangan atau pemulihan data. Kumpulan data terdiri dari beberapa media jika volume data besar.

### Elemen Dasar MTF

File MTF terdiri dari beberapa elemen fundamental yang membentuk blok penyusunnya. Elemen-elemen ini adalah:

#### Blok Deskriptor

Blok deskriptor (DBLK) digunakan untuk kontrol format dan merupakan fondasi utama dari file MTF. Satu file MTF menentukan beberapa DBLK untuk setiap peran unik. Setiap DBLK adalah blok panjang variabel data yang dibagi menjadi empat bagian berikut:

* `Common Block Header` - Struktur panjang tetap yang umum untuk semua DBLK. Ini adalah satu-satunya Header Blok yang diperlukan.
* `Informasi Jenis DBLK` - Blok Panjang Tetap khusus untuk jenis DBLK yang ditentukan
* `Operating System Data` - Data khusus yang didefinisikan berdasarkan jenis DBLK dan sistem Operasi
* `Informasi DBLK` - Informasi khusus panjang variabel DBLK yang tidak dapat disimpan dengan informasi DBLK Panjang Tetap.

 {{< figure src="../bak.png" alt="Format File Cadangan Microsoft SQL" >}}

#### Aliran data

Aliran data dalam file MTF digunakan untuk enkapsulasi dan penyelarasan data. Ini terdiri dari Stream Header, diikuti oleh Stream Data. Header aliran hanya dapat merangkum satu jenis Data Aliran.

{{< figure src="../bak_datastream.png" alt="Format File Cadangan Microsoft SQL" >}}

#### FileMarks

Filemark digunakan untuk pemisahan logis dan akses cepat dalam media. Tanda file ditiru oleh driver perangkat atau dengan menggunakan blok Soft Filemark Descriptor jika perangkat yang digunakan tidak menyediakan tanda file.

## Referensi ##

* [[MS-BCP]: Format Salinan Massal](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

