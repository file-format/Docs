{
  "date" : "2020-03-16",
  "keywords" :[ "File DXF", "Format File", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DXF dan API yang dapat membuat dan membuka file DXF.",
  "title" :"Format Berkas DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DXF?

DXF, Drawing Interchange Format, atau Drawing Exchange Format, adalah representasi data yang ditandai dari file gambar AutoCAD. Setiap elemen dalam file memiliki awalan bilangan bulat yang disebut kode grup. Kode grup ini sebenarnya mewakili elemen yang mengikuti dan menunjukkan arti elemen data untuk tipe objek tertentu. DXF memungkinkan untuk merepresentasikan hampir semua informasi yang ditentukan pengguna dalam file gambar.

Format file DXF dikembangkan oleh Autodesk sebagai format file data CAD untuk interoperabilitas data antara AutoCAD dan aplikasi lain. Dengan demikian, data dapat diimpor dari format lain ke DXF ke AutoCAD sesuai spesifikasi interoperabilitas format file DXF.

## Sejarah Singkat ##


Sejarah format file DXF dimulai pada tahun 1982 ketika diperkenalkan sebagai bagian dari AutoCAD 1.0. Versi awal AutoCAD hanya mendukung format file ASCII dari DXF. Dengan rilis 10 AutoCAD (dan lebih tinggi) pada tahun 1988, dukungan untuk format file ASCII dan DXF biner diperkenalkan di AutoCAD. Pada tahap awal, Autodesk tidak membagikan spesifikasi format file apa pun dan oleh karena itu, impor file DXF yang benar menjadi tidak mudah. Namun, Autodesk sekarang menerbitkan spesifikasi DXF dan tersedia untuk umum.

## Spesifikasi Format File ##

Format file DXF menggunakan kode grup dan pasangan nilai untuk menyusun konten menjadi beberapa bagian. Setiap bagian terdiri dari record dimana setiap record terdiri dari kode grup dan item data. Setiap kode dan nilai grup berada pada barisnya masing-masing dalam file DXF. Setiap bagian dimulai dengan kode grup 0 diikuti dengan string, SECTION. Ini diikuti oleh kode grup 2 dan string yang menunjukkan nama bagian (misalnya, BAGIAN1). Setiap bagian terdiri dari kode grup dan nilai yang menentukan elemennya. Bagian diakhiri dengan 0 diikuti oleh string ENDSEC.

Format file DXF menganggap objek berbeda dari entitas. Objek tidak memiliki representasi grafis di sini tetapi entitas memilikinya. Dengan demikian, entri dalam DXF disebut sebagai objek grafis sedangkan objek objek disebut sebagai objek non-grafis. Bagian BLOCK dan ENTITIES dari file DXF berisi Entitas dan penggunaan kode grup di kedua bagian ini identik. Akhir dari suatu entitas ditunjukkan oleh grup 0 berikutnya, yang memulai entitas berikutnya atau menunjukkan akhir dari bagian tersebut.

### Struktur Berkas ###

Bagian dalam file DXF disusun dengan urutan sebagai berikut:

|Bagian|Deskripsi dasar
---|---|
|Header|Bagian ini berisi informasi umum tentang gambar. Ini seperti fungsi Pengaturan di telepon Anda, yang berisi berbagai variabel yang terkait dengan gambar dan nilai yang terkait. Misalnya, bagian Header akan menentukan versi AutoCAD mana yang digunakan file DXF (variabel $ACADVER) atau satuan yang digunakan untuk mengukur sudut dalam file (variabel $AUNITS)
|Kelas|Bagian CLASSES menyimpan informasi untuk kelas yang ditentukan aplikasi yang instansnya muncul di bagian BLOK, ENTITAS, dan OBJEK database.
|Tabel|Bagian ini berisi definisi untuk beberapa tabel yang berbeda, yang masing-masing berisi sejumlah entri simbol yang berbeda. Misalnya [jenis baris](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) menentukan pola garis putus-putus, titik, teks, dan simbol dalam file DXF dan bagaimana skalanya. Berikut adalah daftar lengkap tabel yang ditemukan di bagian ini:<ul><li> Tabel ID Aplikasi (APPID).</li><li> Tabel Blok Catatan (BLOCK_RECORD).</li><li> Tabel Gaya Dimensi (DIMSTYPE).</li><li> Tabel lapisan (LAYER).</li><li> Tabel Linetype (LTYPE).</li><li> Tabel gaya teks (STYLE).</li><li> Tabel Sistem Koordinat Pengguna (UCS).</li><li> Lihat (LIHAT) tabel</li><li> Tabel konfigurasi viewport (VPORT).</li></ul>
|Blok|Bagian ini berisi objek grafis dan entitas gambar yang membentuk setiap referensi blok dalam gambar.
|Entitas|Bagian ini berisi data objek aktual dan entitas grafis dari gambar. Ini dapat mencakup data mentah – misalnya, entitas lingkaran ditentukan oleh ketebalannya, titik tengahnya, radiusnya, dan arah ekstrusi.
|Objek|Di sini, Anda akan menemukan bagian non-grafis dari gambar. Misalnya, kamus AutoCAD disimpan di sini.

## Referensi ##

* [Spesifikasi File DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [DXF AutoCAD oleh Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

