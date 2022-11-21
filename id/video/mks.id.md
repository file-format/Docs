{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MKS",
  "keywords" :[ "mks", "matroska video", "format mkv", "file", "format", "video"],
  "description":"Pelajari tentang format file MKS untuk subtitle yang hanya dibuat oleh Matroska dan API yang dapat membuat dan membuka file MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Apa itu file MKS?

File MKS umumnya dikenal sebagai file Matroska yang hanya berisi subtitle. Meskipun Matroska adalah wadah file umum, Matroska menghindari penyimpanan informasi dalam format tertentu. Karena subtitle digunakan di beberapa wadah audio atau video, Matroska menaruh perhatian untuk menyimpan beberapa format subtitle yang umum. Ini membantu Matroska untuk konsisten dengan tingkat pertumbuhan. Anda harus mengikuti poin-poin seperti yang diberikan di bawah ini untuk menyimpan subtitle di Matroska:

- ".mks". ekstensi akan digunakan oleh file Matroska (hanya berisi subtitle).
- **CodecPrivate** digunakan untuk menyimpan semua informasi terkait codec yang bersifat global ke seluruh aliran.
- Hapus stempel waktu Mulai dan hentikan yang digunakan dalam format penyimpanan asli stempel waktu. Sebagai gantinya, gunakan stempel waktu dan Durasi Blok.
- Anda dapat menggunakan apa saja dengan lapisan transparan, termasuk video.

## Format Subtitle Umum

Berikut beberapa catatan singkat tentang format subtitle yang lebih umum disimpan di Matroska:

### Subtitle Gambar
Format subtitle VobSub adalah format subtitle gambar pertama yang diimpor ke Matroska. Format ini dihasilkan dengan mengekspor subtitle dari DVD. Trek harus dipisahkan saat disimpan di Matroska jika VobSub terdiri dari beberapa aliran.

### Teks SRT
SRT adalah yang paling sederhana dan mendasar dari semua format subtitle. Ini terdiri dari empat bagian seperti yang diberikan di bawah ini:
 



1. Angka yang menunjukkan urutan subtitle.
2. Waktu muncul dan menghilang subtitle di layar.
3. Subtitle itu sendiri.
4. Baris kosong untuk menandakan dimulainya subjudul berikutnya.
 



### Teks SSA/ASS
Sub Station Alpha (SSA) adalah format file yang digunakan oleh editor subtitle populer SubStation Alpha. Subtitle SSA banyak digunakan oleh fansubber. Ia memiliki kemampuan untuk menampilkan fitur-fitur modern, misalnya karaoke, positioning, styling, dll.
 



### Teks WebVTT
Konsorsium World Wide Web (W3C) mengembangkan WebVTT yang disingkat sebagai "Format Trek Teks Video Web". Format ini digunakan untuk menandai sumber daya trek teks eksternal sehubungan dengan elemen HTML.

### Subtitle grafis presentasi HDMV
Format subtitle grafik presentasi HDMV (HDMV PGS) adalah serangkaian bitmap dan kami tidak dapat mengatakannya sebagai teks sama sekali. Dengan kata lain, Anda dapat mengatakan bahwa itu hanyalah urutan waktu dari gambar grafik. Untuk mengekstrak informasi, mengubah PGS menjadi SRT adalah proses yang diperlukan.

### subtitel teks HDMV
Teks HDMV dikenal sebagai format subtitle tekstual yang digunakan pada Blu-ray. Matroska hanya mengizinkan kumpulan karakter UTF-8 Ketika menyimpan subtitle TextST.

### Subtitle Penyiaran Video Digital (DVB).
Format subtitle DVB diperkenalkan untuk mengatur transmisi dan tampilan subtitle beberapa bahasa pada sinyal TV. Format subtitling tipikal juga akan memungkinkan setiap pemirsa untuk menonton transmisi subtitel DVB, apa pun produsen sistem transmisinya.


## Referensi ##

- [Subtitel Matroska](https://www.matroska.org/technical/subtitles.html)

