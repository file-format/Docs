{
"tanggal": "27-09-2023",
  "keywords": [
"cfg",
"file cfg",
"file konfigurasi cfg celestia",
"apa itu file cfg",
"cara membuka file cfg",
"mengajukan",
"ekstensi file cfg",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File CFG - File Konfigurasi Celestia",
  "description":"Pelajari tentang format File Konfigurasi CFG Celestia dan API yang dapat membuat dan membuka file CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "pengaturan"
}
},
"mod terakhir": "27-09-2023"
}

## Apa itu file CFG?

File konfigurasi Celestia adalah file teks biasa yang digunakan oleh Celestia, program simulasi alam semesta 3D. File-file ini penting untuk menyesuaikan bagaimana Celestia berperilaku, benda langit apa yang ditampilkan, dan bagaimana program muncul. Namun, pengeditan file-file ini memerlukan perhatian yang cermat karena perubahan yang tidak tepat dapat mengganggu proses pemuatan Celestia, sehingga mencegahnya berjalan dengan benar.

## Celestia

Celestia adalah perangkat lunak simulasi astronomi 3D sumber terbuka dan gratis yang memungkinkan pengguna menjelajahi dan memvisualisasikan alam semesta dengan cara yang sangat realistis dan interaktif. Ini dikembangkan oleh Chris Laurel dan pertama kali dirilis pada awal tahun 2000-an. Celestia tersedia untuk sistem operasi Windows, macOS, dan Linux.

Fitur dan aspek utama Celestia meliputi:

- **Visualisasi 3D Realistis:** Celestia memberikan representasi tata surya kita secara detail dan akurat, serta bintang, galaksi, dan objek langit lainnya. Ini menggunakan model dan tekstur 3D berkualitas tinggi untuk menciptakan pengalaman visual yang imersif.

- **Basis Data Langit yang Luas:** Perangkat lunak ini dilengkapi dengan basis data bawaan yang luas dari benda-benda langit yang diketahui, termasuk bintang, planet, bulan, asteroid, komet, dan pesawat ruang angkasa. Pengguna dapat dengan mudah menemukan dan menjelajahi objek-objek tersebut.

- **Akurasi Ilmiah:** Meskipun Celestia adalah alat visualisasi, alat ini bertujuan untuk merepresentasikan objek dan fenomena langit seakurat mungkin, berdasarkan data ilmiah yang tersedia.

## Format File yang Digunakan oleh Celestia

Celestia menggunakan berbagai format file untuk berbagai aspek simulasi astronomi 3D-nya. Berikut adalah beberapa format file utama yang digunakan oleh Celestia:

1. **File Konfigurasi (.cel)**
- *Deskripsi*: File teks biasa yang memungkinkan pengguna menyesuaikan perilaku, tampilan, dan konten Celestia.
- *Tujuan*: Menyesuaikan pengaturan, menentukan lokasi, dan menentukan objek langit.

2. **Model dan Jerat 3D**
- *Format*: [.3ds](/id/3d/3ds/), [.obj](/id/3d/obj/), [.dae](/id/3d/dae/), .ac
- *Deskripsi*: Mendukung format file model 3D yang digunakan untuk merender benda langit dan pesawat ruang angkasa.
- *Tujuan*: Menampilkan objek 3D di dalam Celestia.

3. **File Tekstur**
- *Format*: [.jpg](/id/image/jpeg/), [.png](/id/image/png/), [.dds](/id/image/dds/)
- *Deskripsi*: File-file ini memberikan tekstur permukaan benda langit.
- *Tujuan*: Memetakan tekstur ke model 3D untuk tampilan realistis.

4. **Katalog Bintang dan File Data**
- *Format*: Format khusus, [.csv](/id/spreadsheet/csv/), [.tsv](/id/spreadsheet/tsv/)
- *Deskripsi*: File data yang digunakan untuk mewakili bintang dan benda langit lainnya, memastikan simulasi yang akurat.
- *Tujuan*: Representasi akurat benda langit.

5. **Peta Kubus Tekstur**
- *Deskripsi*: Peta kubus digunakan untuk mensimulasikan penampakan benda langit jauh seperti galaksi.
- *Tujuan*: Merender objek jauh dengan tekstur realistis.

6. **File Skrip**
- *Deskripsi*: File ini berisi skrip khusus yang ditulis dalam bahasa skrip Celestia.
- *Tujuan*: Memungkinkan pengguna membuat peristiwa dan animasi dinamis dalam alam semesta Celestia.

## File konfigurasi Celestia

Berikut adalah ikhtisar dasar tentang apa yang dapat Anda lakukan dengan file konfigurasi Celestia:

1. **Menetapkan Lokasi Anda**: Anda dapat menentukan lokasi Anda di Bumi menggunakan parameter lintang, bujur, dan ketinggian. Hal ini memungkinkan Celestia menampilkan langit malam secara akurat dari posisi Anda.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Menyesuaikan Opsi Tampilan Anda:** Anda dapat menyesuaikan berbagai opsi tampilan seperti bidang pandang, pengaturan waktu, dan preferensi rendering.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Memuat Benda Langit:** Anda dapat menambahkan benda langit seperti bintang, planet, asteroid, pesawat ruang angkasa, dan lainnya ke simulasi Anda. Setiap objek didefinisikan dalam file konfigurasi dengan propertinya.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Mendefinisikan Pesawat Luar Angkasa:** Anda dapat membuat pesawat ruang angkasa fiksi Anda sendiri atau menggunakan pesawat ruang angkasa asli dengan menentukan parameternya seperti posisi, orientasi, dan model 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Membuat Skrip:** Anda dapat menulis skrip dalam bahasa skrip khusus Celestia untuk membuat peristiwa dan animasi dinamis.

## Bagaimana cara membuka file CFG?

Program yang membuka atau mereferensikan file CFG

- Celestia (Gratis) untuk (Windows, Mac, Linux)

## File CFG lainnya

Berikut jenis file lain yang menggunakan ekstensi file **.cfg**.

**Pengaturan**
- [CFG - File Konfigurasi Celestia](/id/settings/cfg-celestia/)
- [CFG - File Koneksi Server Citrix](/id/settings/cfg-citrix/)
- [CFG - File Konfigurasi MAME](/id/settings/cfg-mame/)
- [CFG - File Konfigurasi LightWave](/id/settings/cfg-lightwave/)

**Permainan**
- [CFG - File Bahasa Markup Wesnoth](/id/game/cfg-wesnoth/)
- [CFG - File Konfigurasi MUGEN](/id/game/cfg-mugen/)
- [CFG - File Konfigurasi Mesin Sumber](/id/game/cfg-sourceengine/)

**Sistem & Lainnya**
- [CFG - Berkas CFG](/id/system/cfg/)
- [CFG - File Konfigurasi Model Cal3D](/id/misc/cfg-cal3d/)

## Referensi
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

