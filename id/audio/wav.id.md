{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "file", "ekstensi", "format", "format file pertukaran audio", "musik" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file WAV dan API yang dapat membuat dan membuka file WAV.",
  "title" :"WAV - Format File Audio Bentuk Gelombang",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Apa itu file WAV?

WAV, dikenal dengan WAVE (Waveform Audio File Format), adalah bagian dari spesifikasi Resource Interchange File Format (RIFF) Microsoft untuk menyimpan file audio digital. Formatnya tidak menerapkan kompresi apa pun ke aliran bit dan menyimpan rekaman audio dengan kecepatan pengambilan sampel dan kecepatan bit yang berbeda. Ini telah dan merupakan salah satu format standar untuk CD audio. File wave berukuran lebih besar dibandingkan dengan format file audio baru seperti [MP3](/id/audio/mp3/) yang menggunakan kompresi lossy untuk mengurangi ukuran file sekaligus mempertahankan kualitas audio yang sama. Namun, file WAV dapat dikompresi menggunakan codec Audio Compression Manager (ACM). Ada beberapa API dan aplikasi yang tersedia yang dapat mengonversi file WAV ke format file audio populer lainnya.

**Tahukah kamu?**
Anda dapat menjadi kontributor di FileFormat.com agar komunitas format file tetap up to date dengan temuan Anda. Jika Anda harus membagikan sesuatu tentang format file WAV atau Audio, Anda dapat memposting temuan Anda di bagian [Berita Format File Audio](https://news.fileformat.com/t/audio) agar orang-orang tetap mendapatkan informasi terbaru.

## Format File WAV ##

Format file WAVE, sebagai subset dari spesifikasi RIFF Microsoft, dimulai dengan header file diikuti dengan urutan potongan data. File WAVE memiliki satu potongan "WAVE" yang terdiri dari dua sub-potongan:

* potongan "fmt" - menentukan format data
* potongan "data" - berisi data sampel aktual

### Kepala Berkas WAV ###

Header file WAV (RIFF) panjangnya 44 byte dan memiliki format berikut:


|Posisi|Nilai Sampel|Deskripsi
---|---|---|
|1 - 4|"RIFF"|Menandai file sebagai file riff. Panjang karakter masing-masing 1 byte.
|5 - 8|Ukuran file (bilangan bulat)|Ukuran keseluruhan file - 8 byte, dalam byte (bilangan bulat 32-bit). Biasanya, Anda akan mengisi ini setelah pembuatan.
|9 -12|"GELOMBANG"|Tajuk Jenis Berkas. Untuk tujuan kita, itu selalu sama dengan "GELOMBANG".
|13-16|"fmt "|Format penanda potongan. Termasuk trailing null
|17-20|16|Panjang format data seperti yang tercantum di atas
|21-22|1|Jenis format (1 adalah PCM) - bilangan bulat 2 byte
|23-24|2|Jumlah Saluran - bilangan bulat 2 byte
|25-28|44100|Laju Sampel - bilangan bulat 32 byte. Nilai umum adalah 44100 (CD), 48000 (DAT). Sample Rate = Jumlah Sampel per detik, atau Hertz.
|29-32|176400|(Kecepatan Sampel * BitsPerSample * Saluran) / 8.
|33-34|4|(BitsPerSample * Saluran) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Bit per sampel
|37-40|"data"|"data" potongan header. Menandai awal bagian data.
|41-44|Ukuran file (data)|Ukuran bagian data.
|Nilai sampel diberikan di atas untuk sumber stereo 16-bit.

## Referensi ##

* [WAV - Oleh Wikipedia](https://en.wikipedia.org/wiki/WAV)

