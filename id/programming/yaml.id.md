{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "apa itu file yaml", "cara membuka file yaml", "ekstensi", "file", "file yaml", "format file yaml", "ekstensi .yaml" , "yaml vs json" ,"contoh file YAML", "contoh file docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file YAML dan API yang dapat membuat dan membuka file YAML.",
  "title" :"Format Berkas YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Apa itu file YAML? ##

**File YAML** terdiri dari bahasa YAML (YAML Ain't Markup Language) yang merupakan bahasa serialisasi data berbasis Unicode; digunakan untuk file konfigurasi, perpesanan internet, persistensi objek, dll. YAML menggunakan ekstensi .yaml untuk filenya. Sintaksnya tidak bergantung pada bahasa pemrograman tertentu. Pada dasarnya, YAML didesain untuk interaksi manusia dan bekerja dengan baik dengan bahasa pemrograman modern. Dukungan untuk menserialisasikan struktur data asli arbitrer meningkatkan keterbacaan file YAML, tetapi ini membuat proses parsing dan pembuatan file sedikit rumit.

## Sejarah Singkat ##

YAML pertama kali diusulkan pada tahun 2001 dan dikembangkan oleh Clark Evans, Ingy döt Net, dan Oren Ben-Kiki. YAML pertama kali dikatakan berarti "Bahasa Markup Lain" untuk menunjukkan tujuannya sebagai bahasa markup. Itu kemudian digunakan kembali sebagai "Bahasa Markup Aint YAML" untuk menunjukkan tujuannya sebagai berorientasi data.


## Format File YAML ##

File YAML terdiri dari tipe data berikut

- **Skalar**: Skalar adalah nilai seperti String, Integer, Boolean, dll.
- **Urutan**: Urutan adalah daftar dengan setiap item dimulai dengan tanda hubung (-). Daftar juga bisa bersarang.
- **Pemetaan**: Pemetaan memberikan kemampuan untuk membuat daftar kunci dengan nilai.

### Sintaks ###

- **Spasi kosong**: Lekukan spasi digunakan untuk menunjukkan susunan dan struktur keseluruhan.

``` yaml
nama: John Smith
kontak:
rumah: 1012355532
kantor: 5002586256
alamat:
jalan: |
123 Gang Tornado
Suite 16
kota: Centerville Timur
negara bagian: KS
```

- **Komentar**: Komentar ditulis diawali dengan simbol "#".

``` yaml
# Ini adalah Komentar YAML
```

- **Daftar**: Tanda hubung (-) digunakan untuk menunjukkan anggota daftar dengan setiap anggota pada baris terpisah. Anggota daftar juga dapat dilampirkan dalam tanda kurung siku ([...]) dengan anggota dipisahkan dengan koma (,).

``` yaml
  - A
  - B
  - C
```

``` yaml
[A, B, C]
```

- **Larik Asosiatif**: Larik asosiatif diapit oleh tanda kurung kurawal ({...}). Kunci dan nilai dipisahkan oleh titik dua (:) dan setiap pasangan dipisahkan oleh koma (,).

``` yaml
  {name: John Smith, age: 20}
```

- **String**: String dapat ditulis dengan atau tanpa tanda kutip ganda ("") atau tanda kutip tunggal (').

``` yaml
Rangkaian Sampel
"Sampel Tali"
'Rangkaian Sampel'
```

- **Konten Blok Skalar**: Konten skalar dapat ditulis dalam notasi blok dengan menggunakan berikut ini:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

``` yaml
data: |
YAML
(YAML Bukan Bahasa Markup)
adalah bahasa serialisasi data
```

``` yaml
data: ?
YAML (YAML Bukan Bahasa Markup)
adalah bahasa serialisasi data
```

- **Beberapa Dokumen**: Beberapa dokumen dipisahkan oleh tiga tanda hubung (---) dalam satu aliran. Tanda hubung menunjukkan awal dokumen. Tanda hubung juga digunakan untuk memisahkan arahan dari konten dokumen. Akhir dokumen ditandai dengan tiga titik (...).

``` yaml
  ---
Dokumen 1
  ---
Dokumen 2
...
```

- **Jenis**: Untuk menentukan jenis nilai, tanda seru ganda (!!) digunakan.

``` yaml
a:!!mengambang 123
b: !!str 123
```

- **Tag**: Untuk menetapkan tag ke catatan, tanda ampersand (&) digunakan dan untuk mereferensikan node tersebut, tanda bintang (*) digunakan.

``` yaml
nama: John Smith
tagihan ke: &id01
jalan: |
123 Gang Tornado
Suite 16
kota: Centerville Timur
negara bagian: KS

kirim ke: *id01
```

- **Directives**: Dokumen YAML dapat didahului oleh directives dalam sebuah stream. Arahan dimulai dengan tanda persen (%) diikuti dengan nama dan kemudian parameter dipisahkan oleh spasi.

``` yaml
%YAML 1.2
  ---
Konten dokumen
```
## Contoh file YAML
Di sini Anda dapat melihat **contoh file docker yaml** di bawah:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Pada dasarnya, JSON dan YAML dikembangkan untuk menyediakan format pertukaran data yang dapat dibaca manusia. YAML direalisasikan sebagai superset dari format JSON. Artinya kita bisa mengurai JSON menggunakan parser YAML. Meskipun implementasi praktis dari teori ini sedikit rumit. Oleh karena itu, beberapa perbedaan mendasar antara YAML dan JSON diberikan di bawah ini:

|YAML| JSON|
---|---|
|Proses penguraian data berseri yang rumit dan memakan waktu |Parse data berseri JSON dengan cepat dan mudah dengan desainnya yang lebih sederhana|
|Kurang dukungan komunitas| Dukungan dan popularitas komunitas yang lebih besar|
|Mendukung komentar| Tidak mendukung komentar |
|Kemampuan untuk menggunakan referensi objek data lain| Tidak mungkin membuat cerita bersambung struktur kompleks dengan referensi objek|
|Hierarki dilambangkan dengan menggunakan karakter spasi ganda. Karakter tab tidak diperbolehkan|Objek dan Larik dilambangkan dengan tanda kurung kurawal.|
|Kutipan string bersifat opsional tetapi mendukung tanda kutip tunggal dan ganda.|String harus dalam tanda kutip ganda.|
|Node root dapat berupa tipe data apa pun yang valid|Node root harus berupa array atau objek.|


## Referensi ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

