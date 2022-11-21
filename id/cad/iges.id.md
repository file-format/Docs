{
  "date" : "2020-03-16",
  "keywords" :[ "File IGES", "Format File", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file IGES dan API yang dapat membuat dan membuka file IGES.",
  "title" :"Format File IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Apa itu file IGES?

File dengan ekstensi .iges digunakan untuk bertukar informasi desain antara aplikasi desain berbantuan komputer (CAD). IGES adalah singkatan dari Spesifikasi Pertukaran Grafis Awal. Pertukaran informasi menggunakan IGES meliputi diagram sirkuit, wireframe, permukaan bentuk bebas, atau representasi pemodelan padat. IGES menemukan penerapannya dalam gambar teknik tradisional, analisis model, dan fungsi manufaktur. Formatnya dapat bertukar informasi desain 2D atau 3D antara program CAD. File IGES dapat dibuka dengan beberapa aplikasi CAD seperti Autodesk dan CADSoftTools ABViewer. Ada juga beberapa API yang tersedia untuk membuka dan mengonversi file IGES secara terprogram.

## Format File IGES

File IGES dalam format teks ASCII dan dapat dibuka di editor teks apa pun untuk melihat konten file. Informasi tekstual dalam file IGES direpresentasikan dalam format "Hollerith". File IGES umum dapat berisi ribuan baris untuk mewakili informasi 2D atau 3D yang dapat dipertukarkan sesuai format ini. File IGES dibagi menjadi lima bagian, dilambangkan dengan huruf besar khusus di kolom ke-73. Bagian tersebut adalah bagian `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P), dan `Terminate` (T). Bagian Entri Data dan Data Parameter biasanya disingkat DE dan PD.

### Tajuk Berkas IGES

Bagian Mulai dan Global berisi informasi dasar tentang:
* Nama file dan sumbernya
* Pembatas untuk bagian Data Parameter
* Penulis file, dan informasi umum lainnya.

Bagian Mulai dan Global dari contoh dokumen di Wikipedia adalah sebagai berikut.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Seperti dapat dilihat, bidang awal berisi deskripsi file yang dapat dibaca manusia, dan saya memiliki karakter apa pun di kolom 1-72, dengan baris yang diakhiri dengan header bagian dan nomor baris bagian. Harus ada setidaknya 1 baris bagian Mulai. Bagian global berisi data praprosesor. Itu juga harus ada dalam file dan diakhiri dengan format G000000#.

### Bagian Entri Data (DE) dan Data Parameter (PD).

#### Bagian Entri Data
File IGES terdiri dari beberapa entitas yang berisi informasi tentang data dasar format file IGES. Entitas berisi informasi tentang berbagai elemen format data IGES dan digunakan untuk menggambar. Entitas yang lebih umum digunakan meliputi:
* Busur Melingkar
* Kurva Komposit
* Busur berbentuk kerucut
* Pesawat terbang
* Garis

Ini hanya beberapa dan ada sekitar 150 entitas berbeda di dalam IGES. Setiap entitas diidentifikasi dengan nomor Jenis seperti:
* BUSUR LINGKARAN (Tipe 100)
* GARIS (Tipe 110)

##### Properti Entitas

Setiap entitas yang dideklarasikan memiliki properti berikut.

|Nama Bidang|Deskripsi|
---|---|
|Tipe Entitas |Ini adalah tipe entitas yang dijelaskan. Misalnya, 116 mendeskripsikan entitas Point.|
|PD pointer |Ini memberikan lokasi untuk data entitas ini di bagian Data Parameter. Lokasi ini hanyalah nomor baris di dalam bagian PD yang memiliki baris pertama dari data entitas ini.|
| Struktur | Nol atau penunjuk ke entitas definisi. Tidak berlaku untuk sebagian besar entitas|
|Pola Font Baris| Angka atau penunjuk ke entitas pola font baris. Angka menandakan: * 0 Tidak ada pola yang ditentukan (default) * 1 Solid * 2 Dashed * 3 Phantom * 4 Centerline * 5 Dotted|
|Tingkat| Menentukan level yang akan dikaitkan dengan entitas ini. Mengizinkan entitas muncul di lebih dari satu level|
|Lihat| Menentukan opsi tampilan. Ini adalah: 0 Menunjukkan visibilitas dan karakteristik yang sama di semua tampilan. Penunjuk Default ke entitas Tampilan (Tipe 410) yang dapat dilihat dari Referensi entitas Asosiatif Tampilan Terlihat (Tipe 402, Formulir 3)
|Penunjuk Matriks Transformasi| Referensi entitas matriks transformasi (Tipe 124) atau nol secara default (tanpa transformasi)|
|Asosiasi Tampilan Label| Merujuk Asosiasi Tampilan Label (Tipe 402, Formulir 5) yang menentukan bagaimana label entitas muncul.|
|Nomor Status| Berisi empat bagian dari dua nomor. 1-2: Status kosong. Entah 00 untuk normal atau 01 untuk dikosongkan. 3-4: Peralihan entitas bawahan: adalah 00 untuk independen, 01 untuk dependen fisik, 02 untuk dependen logis, dan 03 untuk keduanya. 5-6: Bendera Penggunaan Entitas: apakah 00 untuk Geometri, 01 untuk anotasi, 02 untuk definisi, 03 untuk Lainnya, 04 untuk Logika, 05 untuk parametrik 2D, dan 06 untuk Geometri konstruksi. Terakhir, 7-8 adalah hierarki, di mana 00 menunjukkan top down global (gunakan karakteristik entitas ini), 01 adalah penangguhan global (jangan gunakan karakteristik entitas ini), dan 02 gunakan properti hierarki (gunakan Entitas Hierarki (Tipe 406, Formulir 10)untuk menentukan karakteristik pengelompokan hierarkis).|
|Nomor Urut| Ditentukan oleh D#, di mana # adalah nomor baris untuk bagian ini (bukan dari bagian atas file). Ini juga digunakan untuk menunjuk ke entitas Entri Data ini.|
|Jenis Entitas| itu ditentukan dua kali per daftar entitas|
|Jumlah Berat Garis| Menentukan ketebalan saat menampilkan entitas. Terkecil adalah 1, 0 adalah default|
|Nomor Warna| Menentukan warna entitas. Nilai bilangan bulat yang diperbolehkan adalah: 0 Tanpa warna (default) 1 Hitam 2 Merah 3 Hijau 4 Biru 5 Kuning 6 Magenta 7 Cyan 8 Putih|
|Nomor Penghitungan Baris Parameter| Menentukan jumlah baris yang digunakan entitas ini di Bagian Data Parameter|
|Nomor Formulir| Menunjukkan bentuk, atau representasi dari entitas ini. Mengubah cara interpretasi data parameter. Standarnya adalah 0|
|Bidang Cadangan| Tidak digunakan|
|Bidang Cadangan| Tidak digunakan|
|Label Entitas| Pengidentifikasi yang ditentukan aplikasi- dibenarkan kanan |
|Nomor Langganan| Kualifikasi numerik untuk label entitas. Keduanya bersama-sama membentuk pengidentifikasi unik untuk entitas|
|Nomor urut Lihat di atas. |Ini akan menjadi D#+1, karena setiap entitas ditentukan pada dua baris.|

#### Bagian Data Parameter
Bagian Entri Data diikuti oleh bagian Data Parameter. Ini mencantumkan data untuk masing-masing entri dan mencantumkan parameter untuk entitas berdasarkan pembatas yang ditentukan di bagian Global (biasanya koma untuk memisahkan parameter dan titik koma untuk mengakhiri daftar).


## Referensi
* [IGES oleh WikiPedia](https://en.wikipedia.org/wiki/IGES)

