{
  "date" : "2019-12-03",
  "keywords" :[ "GLB", "file", "format", "jenis file", "ekstensi", "apa itu file GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Pelajari tentang format file GLB dan API yang dapat membuka dan membuat file GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Apa itu file GLB?

GLB adalah representasi format file biner dari model 3D yang disimpan dalam Format Transmisi GL ([glTF](/id/3d/gltf/)). Informasi tentang model 3D seperti hierarki node, kamera, material, animasi, dan jerat dalam format biner. Format biner ini menyimpan aset glTF (JSON, .bin, dan gambar) dalam gumpalan biner. Itu juga menghindari masalah peningkatan ukuran file yang terjadi dalam kasus glTF. Format file GLB menghasilkan ukuran file yang ringkas, pemuatan cepat, representasi adegan 3D lengkap, dan ekstensibilitas untuk pengembangan lebih lanjut. Formatnya menggunakan model/gltf-binary sebagai tipe MIME.

## Format File GLB - Informasi Lebih Lanjut

Metode pengiriman konten yang digunakan oleh glTF menghasilkan pemrosesan ekstra untuk mendekode data biner yang disandikan base-64 dan juga meningkatkan ukuran file sebesar 33%. Metode pengiriman ini, yang berkontribusi pada pembentukan format file GLB, meliputi:

* glTF JSON menunjuk ke data biner eksternal (geometri, bingkai kunci, kulit), dan gambar.
* glTF JSON menyematkan data biner berenkode base64, dan gambar sebaris menggunakan URI data.

GLB sebagai format wadah diperkenalkan sebagai format file biner untuk representasi aset glTF dalam gumpalan biner untuk menghindari masalah yang disebabkan oleh glTF. Format file GLB [spesifikasi](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) harus dirujuk untuk implementasi pembaca/penulis yang sama untuk pengembangan aplikasi .

## Struktur File GLB

Format file GLB didasarkan pada little endian dan strukturnya menunjukkan bahwa file tersebut berisi:

* Pembukaan 12-byte, berjudul header.
* Satu atau lebih potongan yang berisi konten JSON dan data biner.

#### Judul GLB

Header format file GLB terdiri dari tiga entri 4-byte:

* sihir uint32 - sihir sama dengan 0x46546C67. Ini adalah glTF string ASCII, dan dapat digunakan untuk mengidentifikasi data sebagai glTF Biner
* versi uint32 - menunjukkan versi format kontainer Binary glTF
* panjang uin32 - panjang total glTF Biner, termasuk Header dan semua potongan dalam byte

#### Potongan

Setiap potongan dalam file GLB memiliki struktur berikut:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - panjang chunkData dalam byte
* `chunkType` - menunjukkan jenis potongan
* `chunkData` - muatan biner dari chunk

di mana tipe chunk adalah:

|# |Jenis Potongan|ASCII|Deskripsi|Kejadian
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Konten JSON terstruktur|1
|2.|0x004E4942|BIN|Buffer biner|0 atau 1

Awal dan akhir setiap potongan harus disejajarkan dengan batas 4-byte dan padding harus digunakan untuk tujuan ini.

##### Konten JSON Terstruktur

Ini harus menjadi bongkahan pertama dari aset glTF Biner dan memungkinkan implementasi mengambil sumber daya secara progresif dari bongkahan berikutnya. Ini juga memberikan kemampuan untuk membaca hanya subset sumber daya yang dipilih dari aset glTF Biner seperti LOD mesh yang paling kasar. Untuk memenuhi persyaratan penyelarasan, potongan ini harus diisi dengan karakter Space tambahan (0x20).

##### Penyangga Biner #####

Potongan ini berisi muatan biner untuk geometri, bingkai kunci animasi, kulit, dan gambar. Itu harus menjadi bagian kedua dari aset Binary glTF dan harus diisi dengan angka nol (0x00) untuk memenuhi persyaratan penyelarasan.

## Referensi ##

* [Spesifikasi Format File GLB - Khronos](/id/3D/GLTF/)

