{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "file", "ekstensi", "format", "apa itu format file m4b", "musik", "format file m4b", "M4b vs MP3", "spesifikasi format file m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file M4B dan API yang dapat membuat, mengonversi, dan membuka file M4B.",
  "title" :"M4B - Format File Buku Audio MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Apa itu file M4B?

File dengan ekstensi .m4b adalah buku audio yang umumnya digunakan oleh buku Apple dan iTunes. Audio yang digunakan dalam format ini disimpan dalam MPEG-4 dan dikompresi menggunakan pengkodean AAC. File M4B sangat mirip dengan M4A tetapi memiliki dukungan fitur terkait buku audio, seperti bookmark dan jeda bab. File M4B tersedia dalam versi DRM diaktifkan dan DRM gratis. Buku audio yang dienkripsi DRM biasanya adalah buku audio berbayar dari iTunes Store. Padahal, DRM gratis dapat ditemukan dengan mudah melalui internet.

## Format File M4B

File buku audio yang berisi metadata, gambar, bookmark, dan hyperlink dapat disimpan dengan ekstensi .m4a tetapi umumnya ekstensi .m4b digunakan saat menyimpan, hanya untuk menentukan bahwa file tersebut memiliki format file buku audio. Fairplay DRM (Manajemen Hak Digital) digunakan oleh aplikasi untuk melindungi file M4B mereka. Jadi file yang diunduh dari iTunes hanya dapat diputar di perangkat atau komputer resmi.


## M4B vs M4A

M4B dan [MP3](/audio/mp3/) adalah format file audio saja.

**M4B**: Menang jika dibandingkan dengan MP3 dalam hal kualitas jika menyandikan keduanya pada kecepatan bit yang sama. M4B adalah file buku audio yang dikompres menggunakan pengkodean AAC. Ini pada dasarnya terkait dengan "Lapisan Audio MPEG-4", file dengan ekstensi .m4b adalah lapisan audio dari film MPEG-4 tetapi dengan fitur terkait buku audio tambahan. Tujuannya adalah menyalip MP3 dan menjadi standar baru dalam kompresi audio. Ini sangat mirip dengan MP3 dalam banyak hal tetapi dikembangkan untuk memiliki kualitas yang lebih baik dalam ukuran file yang sama atau bahkan lebih kecil. Format M4B pertama kali diperkenalkan oleh Apple. Jenis format juga direalisasikan sebagai Apple lossless Encoder (ALE).

Oleh karena itu, saat ini M4B tidak bisa mendapatkan kesuksesan arus utama MP3 karena format audionya belum dapat dimainkan secara umum.

**Mp3**: Format audio digital yang sudah tidak asing lagi bagi semua orang. Format kompresi pertama di tempat kejadian dan menjadi sangat terkenal di kalangan pendengar musik. Keberhasilan utamanya sangat cepat sehingga jenis file dapat dimainkan secara universal dan kompatibel dengan hampir semua hal, perangkat keras atau perangkat lunak. Secara umum, M4A akan menghasilkan kualitas suara yang lebih baik, tetapi banyak yang berpendapat bahwa, apakah itu benar atau tidak, perbedaan suara tidak sebanding, dan akan membuang-buang waktu untuk mencoba mengonversi file MP3 menjadi file M4A. Terakhir, konversi hanya akan membuat Anda kehilangan kualitas suara aslinya.

## Spesifikasi format file M4B

Mirip dengan [M4A](/id/audio/m4a/), file M4B juga terdiri dari potongan yang berurutan. Setiap potongan memiliki 8 byte header dan dibagi menjadi:
- Ukuran potongan 4-byte (big-endian, byte tinggi dulu)
- Jenis potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "lewati", "jP2", "lebar", "muat", "imap", "matt", "chap", "kmat", "klip", "crgn", "sinkronisasi", "tmcd", "PICT ", "scpt", "ssrc".

Mirip dengan M4A, potongan pertama di M4B akan bertipe "ftype" dan memiliki sub-tipe di offset 8. M4B ditentukan oleh sub-tipe yang harus "M4B_".

Iterasi potongan, sampai potongan jenis yang tidak diketahui terdeteksi, Ini akan membuat file M4B (MPEG-4 Audio).

## Referensi

* [MPEG-4 Bagian 14 - Oleh Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Contoh Pemulihan](https://www.file-recovery.com/m4a-signature-format.htm)

