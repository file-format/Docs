{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "file wpl", "ekstensi", "format", "apa itu file wpl", "musik", "format file wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file WPL dan API yang dapat membuat, mengonversi, dan membuka file WPL.",
  "title" :"WPL - File Daftar Putar Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Apa itu file WPL?

Sebuah file dengan ekstensi .wpl berisi playlist lagu-lagu yang akan dijalankan di Microsoft Windows Media Player. File-file ini biasanya dibuat oleh pengguna untuk koleksi video dan audio mereka. Konten yang ditulis dalam file WPL, hanyalah jalur direktori atau lokasi untuk file multimedia yang dipilih oleh pembuat file .wpl, sehingga aplikasi pemutar media dapat segera menemukan dan memutar konten multimedia dari lokasi direktorinya.

## Format File WPL

WPL (Windows Media Player Playlist) adalah format file berpemilik yang digunakan di Microsoft Windows Media Player versi 9 atau lebih tinggi. Ini adalah format file komputer yang menyimpan daftar putar multimedia. Secara default, playlist disimpan dengan ekstensi .wpl(Windows Media Player Playlist). Anda dapat menggunakan ekstensi [.m3u](/id/audio/m3u), Jika Anda ingin memutar disk data di perangkat yang tidak mendukung ekstensi ini. Elemen file WPL direpresentasikan dalam format XML.

Elemen tingkat atas "smil" menentukan bahwa elemen file mengikuti struktur Synchronized Multimedia Integration Language (SMIL). File dibuat dan disimpan dengan ekstensi .wpl dan tipe MIME-nya adalah application/vnd.ms-wpl.

### Contoh WPL

Berikut adalah contoh file wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Referensi ##

* [MPEG-1 Audio Layer II - Oleh Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

