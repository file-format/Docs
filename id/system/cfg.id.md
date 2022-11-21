{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "ekstensi", "file", "format", "sistem", "konfigurasi", "pengaturan", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Format Berkas",
  "description":"Pelajari tentang format file CFG dan API yang dapat membuat dan membuka file CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu file CFG? ##

File dengan ekstensi .cfg adalah jenis file "pengaturan". Ini adalah jenis file yang populer digunakan dan digunakan untuk menyimpan informasi mengenai konfigurasi dan pengaturan untuk program komputer. Sebagian besar jenis file CFG disimpan dalam format teks dan tidak boleh dibuka secara manual, melainkan harus dibuka menggunakan editor teks. Namun, ada berbagai jenis file CFG, yang berbeda dalam format penyimpanan informasi. Fitur yang ditawarkan file CFG bervariasi dari satu aplikasi ke aplikasi lainnya. Beberapa aplikasi komputer memungkinkan pengguna untuk memodifikasi, atau mengembangkan sintaks file konfigurasi mereka dengan menggunakan gangguan grafis, sementara yang lain hanya mengizinkan modifikasi menggunakan editor teks. Setelah memodifikasi file-file ini, pengguna dapat menginstruksikan aplikasi untuk membaca file-file ini lagi dan menerapkan modifikasi ke sistem.


## Format File CFG ##

File CFG didukung oleh berbagai sistem operasi seperti sistem operasi mirip Unix dan Unix, MS-DOS, macOS, Microsoft Windows, dan IBM OS/2. Format file-file ini disimpan dan digunakan di masing-masing sistem operasi ini berbeda-beda. Sebagian besar sistem menggunakan dan menyimpan file-file ini dalam format teks biasa yang dapat dibaca manusia dan dapat diedit, sementara yang lain menyimpannya dalam format yang lebih kompleks, bergantung pada penggunaan file dan kebutuhan sistem operasi.

Dalam sistem operasi mirip Unix dan Unix, sebagian besar file CFG menggunakan beberapa gaya format berbeda untuk file CFG, namun, format yang paling umum adalah format teks biasa yang mudah dibaca, dan hampir semua format memungkinkan komentar dibuat dan diedit. Ekstensi file paling umum untuk file CFG dalam sistem operasi ini adalah CNF, CONF, CF, dan INI.

Dalam sistem operasi MS-DOS awalnya hanya ada satu format file konfigurasi, yaitu, teks biasa, namun, MS-DOS 6, memperkenalkan format file konfigurasi INI.

macOS menggunakan file konfigurasi gaya format daftar properti standar.

Di Microsoft Windows, file konfigurasi gaya INI teks biasa adalah sumber penting untuk menyimpan dan mengedit informasi, namun, sistem basis data baru diperkenalkan pada tahun 1993, yang menyebabkan penurunan penggunaan file konfigurasi di Microsoft Windows setelah tahun 1993.


## Contoh CFG ##

Contoh file CFG dapat dilihat di bawah ini:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
