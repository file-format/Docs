{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MKV",
  "keywords" :[ "mkv", "matroska video", "mkv format", "cara memutar file mkv", "video", "file", "format" ],
  "description":"Pelajari tentang format file MKV dan API yang dapat membuat dan membuka file MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Apa itu File MKV? ##

MKV (Matroska Video) adalah wadah multimedia yang mirip dengan format [MOV](/id/video/mov/) dan [AVI](/id/video/avi/), tetapi mendukung lebih dari satu trek audio dan subtitle dalam file yang sama. File MKV adalah format wadah multimedia Matroska yang digunakan untuk video. MKV didasarkan pada Extensible Binary Meta Language dan mendukung beberapa format kompresi video dan audio. Perbedaan utama antara MKV dan format video lainnya adalah bahwa MKV adalah wadah dan bukan codec. File MKV disimpan dengan ekstensi file .mkv. MKV dapat menggabungkan audio, video, dan subtitle dalam satu file meskipun elemen tersebut menggunakan berbagai jenis penyandian. Misalnya, Anda dapat memiliki file MKV yang berisi video H.264 dan MP3 atau AAC untuk audio. MKV juga mendukung deskripsi, peringkat, seni sampul, dan bahkan poin bab. Ada beberapa fitur utama yang dimiliki MKV untuk masa depan. Fitur-fitur ini meliputi:

- Dukungan untuk pencarian Cepat.
- Kemampuan untuk memilih aliran audio dan video yang berbeda.
- Dukungan untuk subtitle (hard-coded dan soft-coded).
- Dukungan untuk metadata, bab, dan menu.
- Kemampuan untuk streaming online.
- Kemampuan untuk memulihkan file yang salah yang memberikan kemampuan untuk memutar file yang rusak.

## Sejarah Singkat ##

File MKV berasal dari tahun 2002 di Rusia. Pengembang utama adalah Lasse Kärkkäinen yang bekerja dengan pendiri Matroska, Steve Lhomme, dan tim pemrogram. MKV dikembangkan sebagai proyek standar terbuka, yang artinya bersifat open source dan gratis untuk digunakan. Seiring berjalannya waktu, format tersebut diperbaiki dan menjadi dasar format multimedia WebM pada tahun 2010.

## Desain Matroska ##

Matroska menambahkan batasan berikut pada spesifikasi EBML.

- **docType** **EBML Header** harus 'matroska'.
- **EBMLMaxIDLength** **EBML Header** harus 4.
- **EBMLMaxSizeLength** **EBML Header** harus antara 1 dan 8 (inklusif).

Semua elemen tingkat atas dikodekan dalam 4 oktet.

- Kode bahasa: Matroska (versi 1 hingga 3) menggunakan kode bahasa yang dapat berupa bibliografi 3 huruf ISO-639-2 (seperti "fre" untuk bahasa Prancis), atau kode negara tambahan dapat digunakan seperti "fre-ca " untuk bahasa Prancis Kanada. Mulai Matroska versi 4, ISO 639-2 atau BCP 47 MUNGKIN digunakan untuk kode bahasa, meskipun BCP 47 disarankan.
- Jenis Fisik: Ini memiliki arti berbeda untuk file audio dan video. Misalnya, ChapterPhysicalEquiv = 60 berarti (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) untuk audio dan (DVD / VHS / LASERDISC) untuk video.
- Struktur Blok - Header Blok: Header blok berisi informasi mengenai nomor trek, stempel waktu, jenis hantaman, dll.
- Hantaman: Ini adalah mekanisme untuk menghemat ruang saat menyimpan data yang biasanya digunakan untuk blok kecil data (bingkai). Ada 3 jenis hantaman:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Structure: Terinspirasi oleh **Block structure** dengan perbedaan utama adalah penambahan flag **Keyframe** dan **Discardable**. Selain itu, semuanya sama.

## Struktur Matroska ##

Dokumen Matroska harus terdiri dari setidaknya satu **Dokumen EBML** menggunakan **Tipe Dokumen Matroska**. Setiap **Dokumen EBML** harus dimulai dengan **Header EBML** diikuti oleh **Elemen Dasar EBML** yang didefinisikan sebagai Segmen. Matroska mendefinisikan beberapa Elemen Tingkat Atas yang mungkin muncul dalam **Segmen**.

EBML menggunakan sistem Elemen untuk menyusun Dokumen EBML, Berikut adalah daftar elemen Tingkat Atas dalam file Matroska:

- **Dokumen EBML**: Pembungkus untuk seluruh file.
- **Header EBML**: Berisi informasi header untuk file seperti DocType.
- **Segmen**: Elemen teratas yang berisi semua elemen level teratas lainnya.
- **SeekHead**: Berisi posisi Segmen dari Elemen Tingkat Atas lainnya.
- **Info**: Berisi informasi umum tentang Segmen.
- **Tracks**: Top-Level Element informasi dengan banyak track dijelaskan.
- **Bab**: Digunakan untuk menentukan menu dasar dan data partisi.
- **Cluster**: Elemen Tingkat Atas yang berisi struktur Blok.
- **Isyarat**: Elemen Tingkat Atas yang berisi semua entri lokal ke Segmen yang mencari akses dengan cepat.
- **Lampiran**: Ini berisi file lampiran.
- **Tag**: Elemen ini berisi metadata yang menjelaskan Trek, Edisi, Bab, Lampiran, atau Segmen secara keseluruhan.

Tabel berikut memperlihatkan struktur dokumen Matroska dengan sebagian besar elemen ditampilkan dalam hierarki:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Tajuk EBML | | | |
| Segmen | SeekHead| Mencari | SeekID |
| | | | CariPosisi |
| | Informasi | SegmenUID | |
| | | SegmenFilename | |
| | | Sebelumnya | |
| | | SebelumnyaNamaFile | |
| | | NextUID | |
| | | Namafile berikutnya | |
| | | Keluarga Segmen | |
| | | BabTerjemahkan | |
| | | Skala cap waktu | |
| | | Durasi | |
| | | TanggalUTC | |
| | | Judul | |
| | | MuxingApp | |
| | | Aplikasi Menulis | |
| | Trek | Lacak Entri | Nomor Trek |
| | | | TrackUID |
| | | | Jenis Trek |
| | | | Nama |
| | | | Bahasa |
| | | | CodecID |
| | | | Codec Pribadi |
| | | | CodecName |
| | | | Video | BenderaInterlaced |
| | | | | Pesanan Lapangan |
| | | | | Mode Stereo |
| | | | | Mode Alfa |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | Lebar Tampilan |
| | | | | TampilanTinggi |
| | | | | TipeRasio Aspek |
| | | | | Warna |
| | | | Suara | Frekuensi Sampling |
| | | | | Saluran |
| | | | | BitDepth |
| | Bab | EdisiMasuk | EdisiUID |
| | | | EdisiFlagHidden |
| | | | EditionFlagDefault |
| | | | EdisiBenderaDipesan |
| | | | BabAtom | Bab UID |
| | | | | BabStringUID |
| | | | | Bab Waktu Mulai |
| | | | | BabWaktuBerakhir |
| | | | | BabFlagHidden |
| | | | | Tampilan Bab | ChapString |
| | | | | | ChapLanguage |
| | Gugus | Stempel waktu |
| | | SilentTracks |
| | | Posisi |
| | | SebelumnyaUkuran |
| | | SimpleBlock |
| | | BlockGroup |
| | | Blok Terenkripsi |
| | Isyarat | CuePoint | Waktu Isyarat |
| | | | CueTrackPositions |
| | Lampiran | File Terlampir | Keterangan Berkas |
| | | | Nama Berkas |
| | | | FileMimeType |
| | | | FileUID |
| | | | Referensi Berkas |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Tag | Tandai | Target | NilaiJenisTarget |
| | | | | Jenis Sasaran |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | Nama Tag |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBiner |
| | | | | SimpleTag |


### Menggunakan Codec ###

Jika Anda tidak menginginkan pemutar media baru dan lebih suka menggunakan pemutar yang ada, Anda perlu menginstal beberapa codec (singkatan untuk kompresi/dekompresi). Meskipun mengunduh codec adalah opsi yang valid, Anda harus berhati-hati tentang sumbernya dan ini mungkin mengandung malware.

## Referensi ##

- [Matroska oleh Wikipedia](https://en.wikipedia.org/wiki/Matroska)

