{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file OSU dan API yang dapat membuat dan membuka file OSU.",
  "title" : "Berkas OSU - Osu! Format File Skrip",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-id",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Apa itu file OSU?

File OSU adalah skrip game yang ditulis untuk osu! permainan ritme. Ini berisi informasi tentang beatmap yang digunakan dalam game seperti tingkat kesulitan, lagu yang akan dimainkan, dan timing objek pukulan yang harus disinkronkan oleh pemain dengan musik. Ini memungkinkan pemain game ritme untuk mengembangkan tantangan khusus dan berbagi dengan komunitas game.

**Jenis MIME Format File OSR:** x-osu-beatmap

## Format File OSU

File OSU disimpan sebagai file teks biasa ke disk dan strukturnya didefinisikan dengan sangat jelas di [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) oleh osu!.

### Bagian dalam File OSU

File OSU pada umumnya memiliki bagian berikut.

|Bagian |Deskripsi |Jenis konten|
---|---|---|
|[Umum]| Informasi umum tentang beatmap| kunci: pasangan nilai|
|[Penyunting]| Pengaturan tersimpan untuk editor beatmap| kunci: pasangan nilai|
|[Metadata] |Informasi yang digunakan untuk mengidentifikasi beatmap| kunci:pasangan nilai|
|[Kesulitan] |Pengaturan kesulitan| kunci:pasangan nilai|
|[Acara]| Acara grafis beatmap dan storyboard| Daftar yang dipisahkan koma|
|[Titik Waktu]| Titik waktu dan kontrol| Daftar yang dipisahkan koma|
|[Warna]| Kombinasi dan warna kulit| kunci : pasangan nilai|
|[Objek Hit]| Pukul benda| Daftar yang dipisahkan koma|

## Referensi

* [OSU! Permainan Irama](https://osu.ppy.sh/home)

* [Format berkas OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


