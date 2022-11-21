{
  "date" : "2019-10-11",
  "keywords" :[ "file emf", "format file emf", "apa itu file emf", "file", "contoh emf", "ekstensi file emf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Format Metafile yang Disempurnakan",
  "description":"Pelajari tentang format file EMF dan API yang dapat membuat dan membuka file EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file EMF?

**Enhanced metafile format (EMF)** menyimpan gambar grafis perangkat secara independen. Metafiles EMF terdiri dari catatan panjang variabel dalam urutan kronologis yang dapat merender gambar yang disimpan setelah diuraikan pada perangkat keluaran apa pun. Rekaman dengan panjang variabel ini dapat berupa definisi objek terlampir, perintah untuk menggambar, dan properti grafik yang penting untuk merender gambar secara akurat. Saat perangkat membuka metafile EMF menggunakan lingkungan grafisnya sendiri, proporsi, dimensi, warna, dan properti grafis lainnya dari gambar asli tetap sama terlepas dari platform perangkat pembuka.

## Sejarah Singkat ##

Pada tahun 1990, Microsoft merancang format file gambar Windows Metafile ([WMF](/id/image/wmf/)) untuk Microsoft Windows. Windows Metafiles adalah format 16-bit yang mungkin berisi beberapa komponen bitmap.WMF dapat terdiri dari grafik vektor dan dimaksudkan agar tetap portabel di antara berbagai aplikasi. Pada tahun 1993, Win32/GDI mengumumkan Enhanced Metafile (EMF), versi yang lebih baru dengan peningkatan fleksibilitas dan skalabilitas. EMF juga digunakan sebagai perintah bahasa grafis untuk menjalankan driver printer. Microsoft sekarang merekomendasikan format metafile yang disempurnakan (EMF) melalui format Windows (WMF). Ketika Windows XP diperkenalkan, versi Enhanced Metafile Format Plus (EMF+) dirilis. Versi yang lebih baru ini menemukan jalannya dengan membuat serialisasi panggilan API GDI+ demikian pula panggilan rekaman WMF/EMF ke GDI. Ada versi EMF terkompresi gzip yang dikenal sebagai EMZ.

## Format File Meta EMF ##

Berikut ini adalah elemen penting dari format metafile yang disempurnakan:

* EMR_HEADER (versi, ukuran, resolusi gambar saat dibuat)
* Tabel untuk objek GDI
* Palet yang dicadangkan (opsional)
* Catatan Metafile diatur dalam struktur array (pengaturan properti, objek yang ditentukan, perintah menggambar)
* Catatan EMR_EOF (rekaman terakhir di metafile EMF)

## Versi EMF ##
* **Original**: Versi asli menentukan rekaman yang diperlukan untuk menyimpan gambar asli dan menjaga perangkatnya tetap independen. Apalagi mendukung rekaman yang berisi objek grafik dan perintah untuk menggambar.
* **Versi 1**: Versi kedua EMF meningkatkan fleksibilitas dan kemandirian perangkat dengan menambahkan record untuk format piksel dan ketentuan untuk menggunakan perintah OpenGL.
* **Versi 2**: Versi ketiga meningkatkan akurasi dengan menambahkan sistem Metrik untuk mengukur jarak permukaan perangkat, menjadikan rekaman lebih terukur.

## Catatan Metafile yang Disempurnakan ##

Metafile record disusun dalam bentuk array. Catatan-catatan ini memiliki struktur ENHMETARECORD dan panjang variabel. ENHMETARECORD menentukan data yang menentukan fungsi GDI untuk membuat gambar menggunakan format metafile yang ditingkatkan. Struktur **ENHMETAHEADER** selalu menjadi rekaman pertama dalam format ini. Header EMF ini berisi informasi berikut.

Setiap rekaman metafile yang ditingkatkan memiliki dua anggota EMR (menyediakan struktur dasar) di awal. Anggota pertama mengenali fungsi GDI (parameter digunakan dalam record) yang menentukan jenis record dan dikenal sebagai iType. Anggota lain nSize menentukan ukuran setiap record. Parameter yang tersisa (jika ada) dan data tambahan diatur tepat di bawah nSize. Segera setelah tajuk, deskripsi teks opsional mungkin muncul. Nama gambar dan penulis dicatat dalam deskripsi teks itu. Palet yang keberadaannya merupakan opsi menentukan warna yang digunakan dalam pembuatan metafile yang disempurnakan. Catatan lain digunakan untuk menentukan fungsi GDI yang penting dalam pembuatan gambar.

Setidaknya satu catatan EMF harus ada di setiap metafile. Informasi traversing dari satu record ke record lainnya bergantung pada record EMF sehingga record ini harus disusun secara berdekatan. Pada catatan tertentu dalam metafile kecuali EOF_record, panjang catatan tertentu itu menentukan untuk pindah ke catatan berikutnya.

## Pembuatan Metafile yang Disempurnakan ##

Fungsi **CreateEnhMetaFile** digunakan untuk membuat metafile yang disempurnakan. Argumen fungsi ini digunakan untuk dimensi dan penyimpanan gambar pada disk/memori. Selain itu, fungsi ini memerlukan dimensi perangkat di mana gambar muncul pertama kali (perangkat yang direferensikan) dan konteks perangkat referensi (DC). Jadi argumen untuk menangani DC ini harus disediakan saat memanggil fungsi **CreateEnhMetaFile**. Sintaks fungsinya adalah sebagai berikut:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** handle ke perangkat referensi.

**lptoFilename:** Pointer ke nama file.

**lprc:** Penunjuk ke struktur oval menentukan dimensi gambar dalam mm.

**lpDesc:** penunjuk ke string untuk judul gambar dan nama aplikasi yang membuat gambar tersebut.

## Operasi Metafile yang Disempurnakan ##

Berikut ini adalah pekerjaan yang dapat dilakukan dengan menggunakan pegangan ke file meta yang disempurnakan.

* Tampilkan dan edit untuk gambar yang disimpan.
* Menghasilkan salinan metafile yang disempurnakan.
* Ambil salinan header EMF, deskripsi opsional, dan versi biner dari metafile yang disempurnakan
* Merekapitulasi warna di palet.

## Objek Grafik ##

Dalam operasi menggambar dan melukis, objek grafik dapat dibuat dengan catatan pembuatan objek dan dapat disimpan untuk digunakan lebih lanjut. Rekaman `EMR_SELECTOBJECT` dapat mengambil objek grafik ini menggunakan konteks perangkat pemutaran. Pena, palet, kuas, spasi warna, font, dan objek stok adalah beberapa jenis objek yang dapat digunakan kembali.

## Pengurutan Byte ##

Format Little-endian digunakan untuk menyimpan data dalam catatan metafile.

## Pembuatan versi ##

Format file EMF telah direvisi dua kali. Versi yang diubah adalah asli, ekstensi 1, dan ekstensi 2. Versi yang diperluas memiliki ketentuan untuk catatan OpenGL dan deskriptor opsional untuk format piksel internal. Fasilitas pengukuran dalam mililiter ditambahkan untuk dimensi yang ditampilkan.

## Referensi ##

* [File Meta Format yang Disempurnakan | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Format dan Spesifikasi Metafile yang Disempurnakan](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

