{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "file", "ekstensi", "format", "audio", "smaf", "ekstensi mmf", "file mmf", "file musik seluler", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file MMF dan API yang dapat membuat dan membuka file MMF.",
  "title" :"MMF - Format File Musik Seluler",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Apa itu file MMF?

MMF adalah ekstensi file yang terkait dengan file SMAF. MMF adalah singkatan dari Mobile Music File sedangkan SMAF adalah singkatan dari Format Aplikasi Seluler musik sintetis. File MMF di dalam smartphone berisi nada dering sistem, suara, dan juga dapat berisi tampilan grafik dan teks. MMF selanjutnya berisi tiga jenis parameter instrumen termasuk FM, PCM, dan Stream PCM. Format file ini kompatibel dengan platform sistem Windows. File MMF dikategorikan sebagai file data. Biasanya, Microsoft Mail mendukung file MMF. File yang memiliki akhiran MMF dapat disalin ke perangkat seluler atau platform sistem apa pun.

Selain itu, file-file ini berukuran jauh lebih kecil dibandingkan dengan file format MIDI standar. File [WAV](/id/audio/wav/) dan [MID](/id/audio/mid/) dapat dikonversi ke format MMF yang kemudian dapat dibagikan dan didistribusikan sebagai konten audio. File-file ini dapat diterima melalui email langsung ke ponsel dan PC.


## Sejarah Singkat Format File MMF

Yamaha mengembangkan alat SMAF sebagai file suara sehingga smartphone dapat menyimpan lebih banyak nada dering unik. Yamaha memperkenalkan SMAF dengan produksi chip suara MA-1, MA-2, MA-3, MA-5, dan MA-7 LSI mereka. Semua format ini menjadi sangat familiar di kalangan ponsel di Pasar Asia Timur pada awal tahun 2000.

Di tingkat internasional, format MMF disahkan oleh Samsung. Dengan bantuan format MMF, Samsung mampu merancang berbagai nada dering polifonik untuk digunakan di smartphone Samsung.

Yamaha ingin membuat format ini lebih populer dan seterusnya pada file SMAF resmi Yamaha, mereka menerbitkan lebih banyak alat yang kompatibel dengan format ini. Dengan ini pengguna sekarang dapat dengan mudah memutar file MMF di komputer mereka.


## Spesifikasi Format File MMF ##

File MMF dikategorikan ke dalam bagian data. Struktur awalan sekitar 8-byte digunakan untuk menggambarkan setiap segmen.
Label 4-byte termasuk CNTI, OPDA, MSTR, MTR, dan ATR. Ukuran data ditambah 8 byte adalah ukuran potongan; seluruh ukuran file dihitung dengan menjumlahkan semua ukuran potongan. Jika file tidak rusak, ukuran file yang dijumlahkan harus sama dengan ukuran header utama.

### Tajuk ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Berikut adalah contoh file MMF:

![](../mmf.png)

## Referensi

* [MMF - Oleh Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

