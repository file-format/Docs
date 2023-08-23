{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "file", "ekstensi", "format", "apa itu format file m4a", "musik", "format file m4a", "M4A vs MP3", "spesifikasi format file m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file M4A dan API yang dapat membuat, mengonversi, dan membuka file M4A.",
  "title" :"M4A - Berkas Audio MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Apa itu file M4A?

**Format file M4A** adalah file audio yang dibuat dengan menggunakan AAC (Advanced Audio Coding) yang dikenal sebagai kompresi lossy. Kata M4A disingkat MPEG 4 Audio. File audio ini biasanya memiliki ekstensi file .m4a. Ini terutama berlaku untuk konten yang tidak dilindungi. Ini dapat menyimpan berbagai jenis konten audio, seperti buku audio, lagu, dan podcast. M4A biasanya direalisasikan sebagai format yang lebih canggih daripada MP3, yang biasanya tidak dirancang untuk audio saja. Ini hanyalah lapisan audio dalam file video MPEG 1 atau 2.

Format M4A dienkripsi oleh FairPlay Digital Rights Management seperti yang dijual melalui iTunes Store menggunakan ekstensi .m4p. Apple iPhone menggunakan audio MPEG-4 untuk nada deringnya, tetapi file audio tersebut menggunakan ekstensi .m4r.


## M4A vs MP3

M4A dan [MP3](/audio/mp3/) adalah format file audio saja.

**M4A**: Lebih baik dari MP3 dalam hal kualitas dan ukuran saat dikodekan pada kecepatan bit yang sama. Ekstensi file .m4a sangat umum karena telah digunakan oleh Apple untuk digunakan di iTunes Music Store. M4A adalah file audio yang dikompres menggunakan teknologi MPEG-4; algoritma untuk kompresi lossy. Ini pada dasarnya terkait dengan "Lapisan Audio MPEG-4", file dengan ekstensi .m4a adalah lapisan audio film MPEG-4. Ini dimaksudkan untuk menyalip MP3 dan menjadi standar baru dalam kompresi audio. Ini sangat mirip dengan MP3 dalam banyak hal tetapi diperkenalkan untuk memiliki kualitas yang lebih baik dalam ukuran file yang sama atau bahkan lebih kecil. Format M4A pertama kali diperkenalkan oleh Apple. Jenis format juga direalisasikan sebagai Apple lossless Encoder (ALE).

Oleh karena itu, saat ini M4A tidak bisa mendapatkan kesuksesan arus utama MP3 karena format audionya belum dapat diputar secara umum. Entah bagaimana itu terbatas hanya untuk MacOS, iPod, dan produk Apple lainnya.

**Mp3**: Format audio digital paling terkenal. Itu juga salah satu format kompresi pertama di tempat kejadian dan menjadi sangat populer di kalangan pecinta musik. Kesuksesan utamanya sangat cepat sehingga jenis file dapat dimainkan secara universal dan dengan hampir semua hal, perangkat keras atau perangkat lunak. Secara umum, M4A akan menghasilkan kualitas suara yang lebih baik, tetapi banyak yang berpendapat bahwa, benar atau tidak, perbedaan suara tidak dapat dibedakan, dan akan membuang-buang waktu untuk mencoba mengonversi file MP3 menjadi file M4A. Akhirnya, konversi hanya akan membuat Anda kehilangan kualitas suara aslinya.

## Spesifikasi format file M4A

File M4A terdiri dari potongan berurutan. Setiap potongan memiliki 8 byte header dan dibagi menjadi:
- Ukuran potongan 4-byte (big-endian, byte tinggi dulu)
- Jenis potongan 4-byte - salah satu tanda tangan yang telah ditentukan sebelumnya: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Chunk pertama akan bertipe "ftype" dan memiliki sub-tipe di offset 8. M4A ditentukan oleh sub-tipe yang harus "M4A_", untuk sub-tipe M4B harus "M4B_" dan untuk sub-tipe M4P harus menjadi "M4P_".

Iterasi potongan, sampai potongan jenis yang tidak diketahui terdeteksi, Ini akan membuat file M4A (MPEG-4 Audio).

## Referensi ##

* [MPEG-4 Bagian 14 - Oleh Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Contoh Pemulihan](https://www.file-recovery.com/m4a-signature-format.htm)

