{
  "date" : "2019-12-13",
  "keywords" :[ "file ppt", "format file ppt", "apa itu file ppt", "file", "contoh ppt", "ekstensi file ppt", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PPT dan API yang dapat membuat dan membuka file PPT.",
  "title" :"PPT - Format Berkas PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file PPT?

File dengan ekstensi PPT mewakili file PowerPoint yang terdiri dari kumpulan slide untuk ditampilkan sebagai SlideShow. Ini menentukan Format File Biner yang digunakan oleh Microsoft PowerPoint 97-2003. File PPT dapat berisi beberapa jenis informasi berbeda seperti teks, poin berpoin, gambar, multimedia, dan objek OLE tersemat lainnya. Microsoft datang dengan format file yang lebih baru untuk PowerPoint, yang dikenal sebagai [PPTX](/id/presentation/pptx/), dari tahun 2007 dan seterusnya yang didasarkan pada Office OpenXML dan berbeda dari format file biner ini. Beberapa program aplikasi lain seperti OpenOffice Impress dan Apple Keynote juga bisa membuat file PPT.

## Sejarah Singkat ##

Microsoft memperkenalkan format file PPT dengan rilis PowerPoint pada tahun 1987. Format biner stabil dibagikan sebagai default di PowerPoint 97-2003 untuk Windows. Format file biner didukung untuk membaca dan menulis oleh PowerPoint versi terbaru juga termasuk PowerPoint 2016.

## Spesifikasi Format File ##

Sejak diperkenalkan, format file PPT telah mengalami beberapa kali revisi untuk penambahan fitur dan penyempurnaan baru. Spesifikasi versi terbaru yang tersedia adalah revisi 6.0 yang diterbitkan pada Agustus 2018 yang tidak boleh dicampur dengan nomor produk sebenarnya dari format file PPT karena Microsoft tidak lagi menyediakan modifikasi untuk format ini.

### Ikhtisar Format File ###

Beberapa komponen kunci dari format file PPT adalah sebagai berikut:

#### Slide ####

Data pengguna seperti bentuk, teks, animasi, dan media ditambahkan ke presentasi di dalam Slide. Presentasi dapat berisi satu atau beberapa slide yang ditampilkan sebagai tayangan slide saat presentasi dijalankan. Presentasi berisi slide master dan slide master judul yang berfungsi sebagai template untuk properti visual umum slide presentasi. Ada juga slide master catatan dan slide master selebaran yang melayani tujuan serupa dan menyediakan properti visual umum untuk semua slide catatan dan semua selebaran tercetak.

#### Bentuk ####

Bentuk adalah objek yang memungkinkan pengguna menambahkan berbagai konten ke slide dalam bentuk bentuk placeholder, gambar, dan grafik. Bentuk pada slide master menentukan data umum untuk grup bentuk.

#### Bentuk Placeholder ####

Ini adalah placeholder khusus yang berfungsi sebagai wadah untuk berbagai objek. Bentuk tempat penampung yang berbeda dapat digunakan untuk memberikan petunjuk untuk menyisipkan jenis bentuk tertentu seperti tabel atau bagan. Di dalam slide, bentuk placeholder mengadopsi properti visual dari slide master utama, slide master judul, atau slide master catatan.

#### Objek Eksternal ####

Objek eksternal seperti audio yang disematkan dan ditautkan, video yang ditautkan, objek OLE yang disematkan dan ditautkan, dan hyperlink bisa disematkan di slide. Objek ini dapat digunakan untuk mengaktifkan objek tertaut untuk mengakses sumber daya eksternal selama peragaan slide.

### Struktur Format File ###

Format file biner PowerPoint terdiri dari aliran berikut untuk mewakili keseluruhan struktur dan data dokumen.

* Aliran Pengguna Saat Ini
* Aliran Dokumen PowerPoint
* Aliran Gambar
* Informasi Ringkasan dan Informasi Ringkasan Dokumen (Opsional)

Spesifikasi lengkap untuk format file DOC dapat ditemukan sebagaimana disediakan oleh [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) dan harus dikonsultasikan mengacu pada bagian yang disebutkan dalam rincian berikut.

#### Aliran Pengguna Saat Ini ####

Itu menyimpan catatan pengguna terakhir yang membuka dokumen dan namanya harus "Pengguna Saat Ini".

#### Aliran Dokumen PowerPoint ####

Menyimpan catatan semua informasi tentang presentasi PowerPoint dan menjelaskan tata letak dan isinya. Ini adalah aliran wajib yang namanya HARUS "Dokumen PowerPoint". Isi aliran ini ditentukan oleh urutan catatan tingkat atas. Pembatasan pengurutan sebagian pada urutan rekaman ditentukan dalam rekaman PersistDirectoryAtom dan UserEditAtom.

Sebagai catatan wadah, catatan DocumentContainer, MainMasterContainer (bagian 2.5.3), HandoutContainer (bagian 2.5.8), SlideContainer (bagian 2.5.1), dan NotesContainer (bagian 2.5.6) masing-masing adalah akar dari pohon catatan wadah dan rekaman atom. Di dalam catatan wadah apa pun, catatan lain bisa ada yang tidak secara eksplisit terdaftar sebagai catatan anak. Catatan yang tidak diketahui diidentifikasi ketika bidang recType dari struktur RecordHeader (bagian 2.3.1) berisi nilai yang tidak ditentukan oleh pencacahan RecordType (bagian 2.13.24). Catatan yang tidak diketahui ini, jika ditemukan, HARUS diabaikan, dan MUNGKIN<1> dipertahankan. Catatan yang tidak diketahui dapat diabaikan dengan mencari maju recLen byte dari akhir struktur RecordHeader.

Setiap kali aliran ini ditulis, rekaman tingkat atas baru, hasil edit pengguna, dapat ditambahkan ke aliran yang ada, atau seluruh konten aliran dapat diganti dengan urutan rekaman tingkat atas yang diperbarui. Jika seluruh aliran tidak diganti, catatan tingkat teratas yang sudah ada sebelumnya yang terdiri dari hasil edit pengguna sebelumnya, dapat dibuat usang oleh catatan tingkat atas yang ditambahkan berikutnya yang terdiri dari hasil edit pengguna saat ini.

#### Aliran Gambar ####

Ini adalah aliran opsional yang Berisi data tentang gambar yang terdapat dalam presentasi PowerPoint. Namanya HARUS "Gambar". Konten aliran ini ditentukan oleh catatan OfficeArtBStoreDelay sebagaimana ditentukan dalam [MS-ODRAW] bagian 2.2.21.

#### Aliran Informasi Rangkuman ####

Itu membuat statistik tentang dokumen mengikuti standar Microsoft Office. Nama Aliran Informasi Ringkasan harus "\005SummaryInformation", di mana \005 adalah karakter dengan nilai 0x0005, bukan literal string "\005". Aliran ini HARUS dihilangkan untuk dokumen terenkripsi. Isi aliran ini ditentukan dalam [MS-OSHARED] bagian 2.3.3.2.1.

#### Aliran Informasi Ringkasan Dokumen ####

Aliran opsional yang namanya HARUS "\005DocumentSummaryInformation", di mana \005 adalah karakter dengan nilai 0x0005, bukan string literal "\005". Aliran ini MUNGKIN<2> dihilangkan untuk dokumen terenkripsi. Isi aliran ini ditentukan dalam bagian [MS-OSHARED] 2.3.3.2.2.

#### Aliran Informasi Ringkasan Terenkripsi ####

Aliran opsional yang namanya HARUS "EncryptedSummary". Aliran ini hanya ada dalam dokumen terenkripsi. Isi aliran ini ditentukan dalam bagian [MS-OFFCRYPTO] 2.3.5.4.

#### Penyimpanan Tanda Tangan Digital ####

Penyimpanan opsional yang namanya HARUS "_xmlsignatures". Itu MUNGKIN dihilangkan dan MUNGKIN diabaikan. Konten penyimpanan ini ditentukan dalam [MS-OFFCRYPTO] bagian 2.5.2.

#### Penyimpanan Data XML Khusus ####

Penyimpanan opsional yang namanya HARUS "MsoDataStore". Isi penyimpanan ditentukan dalam [MS-OSHARED] bagian 2.3.6.

#### Aliran Tanda Tangan ####

Aliran opsional yang namanya HARUS "_signatures". Itu HARUS dihilangkan dan MUNGKIN diabaikan. Isi aliran ini ditentukan dalam [MS-OFFCRYPTO] bagian 2.5.1.

## Referensi ##

* [Spesifikasi Format File PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Tipe Data Umum Office dan Struktur Objek](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Struktur Kriptografi Dokumen Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Format File PowerPoint](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

