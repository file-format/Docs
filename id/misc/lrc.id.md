{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File LRC - Apa itu file LRC?",
  "description":"Pelajari tentang file LRC Lyric dan API yang dapat membuat dan membuka file LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Apa itu file LRC?

File LRC adalah file lirik berbasis teks yang berisi lirik lagu audio. Saat lagu audio diputar dengan pemutar musik atau perangkat lunak pemutar audio di komputer, file LRC dibaca secara paralel dan ditampilkan sesuai waktu. File LRC berisi titik isyarat untuk menampilkan lirik saat lagu diputar. Secara umum, file LRC memiliki nama yang sama dengan file audio yang sesuai seperti audio.mp3 dan audio.lrc. File LRC mirip dengan file subtitle seperti [SRT](/id/video/srt/).

## Format File LRC - Informasi Lebih Lanjut

File format lirik LRC disimpan sebagai file teks biasa dan dapat dibuka dan diedit dalam file teks. Isi file LRC berisi informasi warna untuk tampilan teks lirik.

## Format LRC

Ada beberapa format file LRC yang telah dikembangkan dari waktu ke waktu. Ini

### Format LRC Sederhana

Tag Waktu Baris dalam format `[mm:ss.xx]` dengan mm adalah menit, ss adalah detik, dan xx adalah seperseratus detik.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Format Sederhana Diperpanjang

Itu termasuk Kemampuan untuk mengubah dan menentukan jenis kelamin lirik dengan menggunakan M: Pria, F: Wanita, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Format LRC yang disempurnakan

Format LRC yang disempurnakan adalah versi tambahan dari format LRC Sederhana. Itu menambahkan Tag Waktu Kata dalam format`<mm:ss.xx>` di akhir kata sebelumnya.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referensi

* [Format File Lirik LRC - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

