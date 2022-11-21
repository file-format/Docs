{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "ekstensi", "file", "format", "sistem", "File Panel Kontrol", "Windows", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - File Panel Kontrol",
  "description":"Pelajari tentang format file CPL dan API yang dapat membuat dan membuka file CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu file CPL? ##

File CPL adalah jenis file "sistem". Ini digunakan oleh sistem operasi Windows. File CPL adalah kependekan dari Control Panel File. File-file ini adalah file biner yang dibuka dengan panel kontrol di sistem operasi Microsoft Windows dan digunakan untuk mewakili dan membuka alat yang tersedia di panel kontrol, seperti Mouse, Layar, Jaringan, dan lain-lain. File CPL biasanya disimpan di folder sistem di perangkat Anda. File-file ini tidak boleh dibuka secara manual.


## Format File CPL ##

File CPL yang berbeda di sistem operasi Windows Anda terhubung untuk mewakili item panel kontrol yang berbeda. Semua item panel kontrol ditautkan ke file CPL dan memiliki akhiran ".cpl" yang dilampirkan ke itemnya.

Beberapa jenis file CPL yang umum dengan formatnya adalah:

* Inetcpl.cpl – Untuk properti Internet di perangkat Anda
* Appwiz.cpl – Untuk Menambah atau Menghapus properti Program di perangkat Anda
* Desk.cpl – Untuk properti Tampilan
* Main.cpl – Untuk properti yang terkait dengan Mouse, Font, Keyboard, dan Printer.
* Netcpl.cpl – Untuk properti terkait Jaringan
* System.cpl – Untuk properti terkait Sistem dan untuk menambahkan wizard Perangkat Keras Baru
* TimeDate.cpl – Untuk properti Tanggal atau Waktu
* Mlcfg32.cpl – Untuk properti Microsoft Exchange atau Windows Messaging
* Intl.cpl – Ini berkaitan dengan properti Pengaturan Regional
* Modem.cpl – Untuk properti terkait Modem
* Themes.cpl – Menyimpan Tema dan properti Desktop.
* Password.cpl – Untuk properti Kata Sandi
* Mmsys.cpl – Untuk properti Multimedia
* Wgpocpl.cpl – Berkaitan dengan Microsoft Mail Post Office

## Sejarah Singkat ##

Jenis file CPL dikembangkan oleh Microsoft Windows dan merupakan bagian integral dari sistem operasi Windows sejak Windows 1.0. Itu masih digunakan di semua versi Windows, dan semua properti item panel kontrol disimpan menggunakan jenis file ini.

## Contoh CPL ##

Contoh file CPL dapat dilihat di bawah ini:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
