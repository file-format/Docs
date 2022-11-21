{
  "date" : "2019-10-11",
  "keywords" :[ "file mpkg", "format file mpkg", "apa itu file mpkg", "file", "contoh mpkg", "ekstensi file mpkg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File MPKG - File Paket Meta",
  "description":"Pelajari tentang format file MPKG dan API yang dapat membuat dan membuka file MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Apa itu file MPKG?

File dengan ekstensi .mpkg adalah file penginstal arsip, kebanyakan ditemukan di Sistem Operasi MacOS. Ini berisi semua file instalasi aplikasi yang diperlukan tanpa perlu menyimpan file terkait secara terpisah. File MPKG tunggal dapat berisi file paket [PKG](/id/compression/pkg/) sebagai salah satu file instalasi selain file lainnya. File MPKG tidak dapat dibuka dengan perangkat lunak umum apa pun dan dijalankan secara otomatis di MacOS menggunakan Penginstal Apple.

## Format File MPKG

File MPKG berisi berbagai jenis file yang diperlukan untuk instalasi beberapa paket di dalamnya. Hal ini terlihat dari gambar di bawah ini yang merupakan struktur pohon dari contoh file MPKG. Struktur pohon ini diekspor menggunakan perintah `tree` di terminal MacOS.

{{< figure src="../mpkg.png" alt="Format File MPKG" >}}

Deskripsi berbagai elemen dalam gambar adalah sebagai berikut.

`Direktori Paket` - menyimpan daftar file pkg, yaitu daftar sub-Paket
`Direktori Sumber Daya` - menyimpan sumber daya yang digunakan oleh pkg, seperti sumber daya dan gambar yang dilokalkan , dokumen Rtf, dokumen pdf, dll.
`Distribution.dist file` - Dokumen xml yang berisi informasi seperti sub-paket yang akan diinstal dan skrip runtime

Contoh file XML untuk file MPKG dapat terlihat sebagai berikut tergantung pada sub-paket terkait.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/id/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - adalah sub-paket yang akan diinstal. Ini adalah direktori struktur Bundel dalam format pkg. Ini berisi subdirektori Contents.

## Referensi

* [Paket OSX Flat](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Manajer Paket C++ MPKG](https://github.com/puellavulnerata/mpkg)

