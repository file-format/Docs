{
  "date" : "2021-06-09",
  "keywords" :[ "isyarat", "file", "ekstensi", "format", "apa itu file isyarat", "musik", "format file isyarat", "spesifikasi format file isyarat", "lembar isyarat", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file CUE dan API yang dapat membuat, mengonversi, dan membuka file CUE.",
  "title" :"CUE - File Lembar Isyarat",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Apa itu file CUE?

File dengan ekstensi .cue, juga dikenal sebagai file lembar isyarat, adalah file metadata yang berisi informasi tentang tata letak trek pada CD atau DVD. Ini didukung oleh pemutar media dan aplikasi pembuat cakram optik. Data audio utama yang disimpan di CD direferensikan oleh file isyarat, bersama dengan spesifikasi panjang trek, judul disk, dan artis. Jadi jika satu file audio berisi banyak trek, file isyarat dapat digunakan untuk membagi audio menjadi beberapa file atau mereferensikan berbagai trek.

## Format File CUE

File CUE atau cue sheet disimpan dalam format teks biasa yang dapat dibaca manusia. Informasi dalam file isyarat adalah perintah dengan satu atau lebih parameter. Perintah-perintah ini berlaku untuk seluruh file atau ke trek individu, tergantung pada perintah tertentu dan konteksnya. Panduan pengguna CDRWIN menjelaskan spesifikasi untuk sintaks dan semantik lembar isyarat.

## Perintah Penting Lembar CUE

|Perintah|Deskripsi|
---|---|
|FILE| Merujuk ke file yang berisi data dan formatnya seperti [MP3](/id/audio/mp3/), [WAV](/id/audio/wav/), atau gambar disk biner biasa)|
|TRACK| Menentukan informasi konteks trek seperti nomor dan jenis atau modenya.|
|INDEKS| Mewakili posisi sebagai indeks dalam FILE. Formatnya adalah mm:ss:ff (menit-detik-frame).|
|PREGAP dan POSTGAP|Ini menunjukkan pregap atau post-gap dari suatu trek, yang tidak disimpan dalam file data apa pun. Panjangnya ditentukan dalam format menit-detik-bingkai yang sama seperti untuk INDEX.|

### Contoh Lembar CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referensi

* [file .cda - Oleh Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

