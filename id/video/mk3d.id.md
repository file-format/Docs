{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MK3D",
  "keywords" :[ "mk3d", "matroska video", "format mkv", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Pelajari tentang format file MK3D untuk video 3D stereoskopik yang dibuat oleh Matroska dan API yang dapat membuat dan membuka file MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Apa itu file MK3D? ##

File MK3D milik keluarga format video Matroska. File-file ini sebenarnya adalah video **stereoscopic 3d** yang dibuat menggunakan format Matroska 3D. Wadah file MKV menggunakan nilai bidang StereoMode untuk menentukan jenis barang video 3D stereoskopis. Nilai StereoMode juga tersedia untuk menampilkan video 3D stereo lama dengan memisahkan warna cyan dan merah (AnaGlyph)

## Detail Teknis ##
Video 3D dapat dikompresi dengan dua cara berikut:

- Jalur terpisah untuk setiap mata.
- Gabungkan setiap pelacakan mata menjadi satu trek.

Wadah file MKV mendukung keduanya.

Untuk video single-track yang lebih mudah dengan materi 3D di dalamnya, Anda harus menyetel bidang **StereoMode** yang memutuskan apakah pesawat akan dirakit di trek gabungan mono atau kiri kanan. Anda dapat menggunakan salah satu dari nilai bidang StereoMode berikut:

|Nilai | Deskripsi |
|---|---|
|0| mono|
|1| berdampingan (mata kiri pertama) |
|2| atas-bawah (mata kanan pertama)|
|3| atas-bawah (mata kiri pertama)|
|4| checkboard (kanan dulu)|
|5| papan centang (kiri adalah yang pertama)|
|6| baris disisipkan (kanan pertama)|
|7| baris disisipkan (kiri pertama)|
|8| kolom diselingi (kanan pertama)|
|9| kolom diselingi (kiri pertama)|
|10| anaglyph (sian/merah)|
|11| berdampingan (mata kanan adalah yang pertama)|
|12| anaglyph (hijau/magenta)|
|13| kedua mata dicampur dalam satu Blok (mata kiri adalah yang pertama) (mode sekuensial lapangan)|
|14| kedua mata dicampur dalam satu Blok (mata kanan adalah yang pertama) (mode sekuensial lapangan)|

Untuk beberapa trek, wadah MKV perlu menentukan fungsionalitas setiap trek secara terpisah. **TrackOperation** dengan **TrackCombinePlanes** digunakan untuk melakukan pekerjaan itu.


## Referensi ##

- [Catatan Spesifikasi Matroska](https://www.matroska.org/technical/notes.html)
- [Dukungan Kontainer File MKV untuk Video 3D Stereo dan File MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

