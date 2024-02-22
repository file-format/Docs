{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file OSR dan API yang dapat membuat dan membuka file OSR.",
  "title" : "File OSR - osu! Putar Ulang Format File",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-id",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Apa itu file OSR?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**Jenis MIME Format File OSR:** x-osu-replay

## Format Berkas OSR

File OSR disimpan sebagai file biner dengan bidang data dengan panjang tetap dan variabel.

|Jenis Data| Format|
---|---|
|Byte |Mode permainan replay (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Integer |Versi game saat pemutaran ulang dibuat (mis. 20131216)|
|String |osu! hash MD5 beatmap|
|Tali| Nama pemain|
|Tali| osu! memutar ulang hash MD5 (termasuk properti pemutaran ulang tertentu)|
|Pendek| Jumlah 300an|
|Pendek| Jumlah 100 di standar, 150 di Taiko, 100 di CTB, 100 di mania|
|Pendek| Angka 50an di standar, buah kecil di CTB, 50an di mania|
|Pendek| Jumlah Geki di standar, Maks 300 di mania|
|Pendek| Jumlah Katus di standar, 200 di mania|
|Pendek| Jumlah kesalahan|
|Bilangan Bulat| Total skor yang ditampilkan pada laporan skor|
|Pendek| Kombo terhebat ditampilkan pada laporan skor|
|Bita| Kombo sempurna/penuh (1 = tidak ada yang meleset dan tidak ada penggeser yang patah serta tidak ada penggeser yang selesai lebih awal)|
|Bilangan Bulat| Mod yang digunakan. Lihat di bawah untuk daftar nilai mod.|
|Tali| Grafik batang kehidupan: pasangan yang dipisahkan koma u/v, dengan u adalah waktu dalam milidetik memasuki lagu dan v adalah nilai floating point dari 0 - 1 yang mewakili jumlah kehidupan yang Anda miliki pada waktu tertentu (0 = bar kehidupan adalah kosong, 1= bilah kehidupan penuh)|
|Panjang| Stempel waktu (Windows berdetak)|
|Bilangan Bulat| Panjang data pemutaran ulang terkompresi dalam byte|
|Byte |Array Data pemutaran terkompresi|
|Panjang| ID Skor Online|
|Ganda| Informasi mod tambahan. Hanya ada jika Latihan Target diaktifkan.|

## Referensi

* [OSU! Permainan Irama](https://osu.ppy.sh/home)

* [Format Berkas OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


