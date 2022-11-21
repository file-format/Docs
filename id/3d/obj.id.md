{
  "date" : "2019-10-11",
  "keywords" :[ "file obj", "format file obj", "apa itu file obj", "file", "contoh obj", "ekstensi file obj", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File OBJ",
  "description":"Pelajari tentang format file OBJ dan API yang dapat membuka dan membuat file OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu File OBJ?

File **OBJ** digunakan oleh aplikasi Advanced Visualizer Wavefront untuk mendefinisikan dan menyimpan objek geometris. Transmisi data geometris maju dan mundur dimungkinkan melalui file OBJ. Baik geometri poligonal seperti titik, garis, simpul tekstur, permukaan, dan geometri bentuk bebas (kurva dan permukaan) didukung oleh format OBJ. Format ini tidak mendukung animasi atau informasi terkait cahaya dan posisi pemandangan.

File OBJ biasanya merupakan produk akhir dari proses pemodelan 3D yang dihasilkan oleh CAD (Computer Aided Design). Urutan default untuk menyimpan simpul berlawanan arah jarum jam menghindari deklarasi eksplisit wajah normal. Meskipun file OBJ mendeklarasikan informasi skala di baris komentar, belum ada unit yang dideklarasikan untuk koordinat OBJ.

## Sejarah Format OBJ 3D

Wavefront Technologies membuat format file OBJ untuk aplikasi Advanced Visualizer untuk menyimpan objek geometris dan data 3D. Versi 2.11 digantikan oleh versi 3 yang baru didokumentasikan. Format file terbuka dan telah diterapkan oleh vendor lain untuk aplikasi grafik 3D mereka. Wavefront Technologies menyimpan format file ini open source dan netral.

## Format File OBJ

Dalam objek 3D, pengkodean geometri permukaan adalah pekerjaan yang menantang yang diselesaikan dengan sangat baik oleh format file OBJ. Format ini cukup serbaguna karena menawarkan sejumlah pilihan untuk menyandikan geometri permukaan. Berikut adalah tiga format yang diperbolehkan dengan kelebihan dan kekurangannya masing-masing:

### Tesselasi dengan Wajah Poligonal

Format file OBJ memfasilitasi pengguna untuk mengubah permukaan model 3D menggunakan bentuk geometris sederhana atau kompleks. Untuk pengkodean geometri permukaan model, file menyimpan simpul dan normal untuk setiap poligon. Meskipun tessellation meningkatkan kekasaran model, namun penting untuk menemukan keseimbangan yang tepat antara ukuran file dan kualitas cetaknya.

### Kurva Bentuk Bebas

Format file OBJ memungkinkan kurva permukaan bentuk bebas yang ditentukan pengguna untuk menentukan geometri permukaan suatu model. Karena kurva bentuk bebas lebih kompleks daripada permukaan poligonal, dengan sedikit parameter matematis, garis lengkung dapat didefinisikan dengan baik oleh kurva bentuk bebas. Oleh karena itu, dengan data yang lebih sedikit dibandingkan dengan teselasi poligonal, kurva bentuk bebas digunakan untuk menghasilkan pengkodean berkualitas tinggi dari model 3D apa pun tanpa memperluas ukuran file.

### Permukaan bentuk bebas

Format file OBJ juga menentukan ubin geometri permukaan dengan tambalan permukaan bentuk bebas. Tambalan permukaan bentuk bebas (NURBS) jenis ini sangat cocok untuk permukaan tanpa dimensi radial yang kaku seperti badan truk, sayap helikopter, atau lambung kapal. Penggunaan permukaan bentuk bebas sangat menguntungkan karena lebih presisi untuk menjaga ukuran file lebih kecil dengan presisi lebih tinggi. Permukaan ini adalah bagian penting dari industri kedirgantaraan dan otomotif di mana presisi rendah tidak dapat dimaafkan.

Kata kunci berikut disusun berdasarkan tipe data untuk mendefinisikan geometri permukaan.


|Elemen|Pernyataan tubuh kurva/permukaan bentuk bebas|Atribut kurva/permukaan bentuk bebas
---|---|---|
|p|Titik|parm|Nilai parameter|derajat|Derajat
|l|Line|trim|Loop pemangkasan luar|bmat|Matriks dasar
|f|Wajah|lubang|Lingkaran pemangkasan bagian dalam|langkah|Ukuran langkah
|curv|Curve|scrv|Special curve|cstype|Curve or surface type
|curv2|kurva 2D|sp|Titik khusus|**Konektivitas dan Pengelompokan permukaan**
|surf|Surface|end|End statement|con|connect
|**Tampilkan/render atribut**|g|Nama grup
|bevel|Interpolasi bevel|shadow_obj|Shadow casting|s|Smoothing group
|lod|Tingkat detail|trace_obj|Ray tracing|mg|Menggabungkan grup
|d_interp|Larutkan interpolasi|ctech|Teknik perkiraan kurva|o|Nama objek
|c_interp|Interpolasi warna|stech|Teknik perkiraan permukaan|
|usemtl|Nama bahan|mtllib|Perpustakaan bahan|
|**Simpul geometris**|
|v|Vertex geometris|vn|Vertex normal|
|vt|Verteks tekstur|vp|Verteks ruang parameter|

### Warna dan Tekstur

File OBJ memungkinkan informasi warna dan tekstur disimpan dalam format file terkait yang disebut Material Template Library (MTL). Render model geometris multiwarna menggunakan kedua file ini secara bersamaan. File MTL berbasis ASCII dan memfasilitasi rendering komputer dengan menggambarkan sifat pantulan cahaya dari suatu permukaan menggunakan model pantulan Phong. Standar tersebut telah diadopsi oleh sejumlah besar vendor perangkat lunak yang memanfaatkannya untuk pertukaran materi. Format MTL agak ketinggalan jaman karena tidak memiliki dukungan dalam teknologi terbaru seperti peta specular dan paralaks.

## Referensi

* [Wavefront .obj file](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

