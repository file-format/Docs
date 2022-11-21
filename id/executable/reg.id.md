{
  "date" : "2021-08-02",
  "keywords" :[ "file reg", "format file reg", "apa itu file reg", "file", "contoh reg", "ekstensi file reg", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file REG dan API yang dapat membuat dan membuka file REG.",
  "title" :"REG - File Registri Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Apa itu file REG?
File REG hanyalah file teks dengan ekstensi .reg. File-file ini biasanya dibuat dengan mengekspor kunci khas dari Registry. File-file ini juga dapat digunakan sebagai cadangan registri (Khusus langkah ini penting sebelum melakukan perubahan!). Anda dapat melihat bahwa beberapa membuatnya tersedia sebagai file yang dapat diunduh di situs yang sama yang menunjukkan kepada Anda cara melakukan peretasan Registri. File REG berguna untuk membuat perubahan manual pada Registry dan mengekspor perubahan tersebut. Cukup bersihkan file sedikit lalu bagikan dengan orang lain.

## format file REG
Format file REG dirancang untuk mengekspor dan mengimpor bagian dari registri Windows menggunakan sintaks berbasis INI. Registri Windows adalah basis data relasional atau hierarkis yang menyimpan pengaturan tingkat rendah untuk sistem operasi Microsoft Windows dan aplikasi lain yang menggunakan registri Windows. kalau tidak, kami dapat mengatakan, registri atau Windows Registry terdiri dari informasi, opsi, pengaturan, dan nilai lain untuk program dan perangkat keras yang diinstal pada semua versi sistem operasi Microsoft Windows.
### Sintaks file REG
Berikut adalah beberapa elemen kunci sebagai bagian dari sintaks file REG:
- **RegistryEditorVersion**: Misalnya "Windows Registry Editor Version 5.00" untuk Windows 2000, Windows XP, dan Windows Server 2003.
- **Baris kosong**: Mengidentifikasi awal jalur registri baru.
- **RegistryPathx**: Jalur subkunci yang menyimpan nilai pertama yang Anda impor.
- **DataItemNamex**: Nama item data yang ingin Anda impor.
- **DataTypex**: Tipe data untuk nilai registri.

Kunci disimpan dalam file .reg menggunakan sintaks berikut:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Anda dapat mengedit Nilai Default kunci dengan menggunakan "@" alih-alih "Nama Nilai":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Contoh
Berikut adalah contoh file REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Referensi

* [Windows Registry- oleh Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Cara menambahkan, mengubah, atau menghapus subkunci dan nilai registri menggunakan file .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registry-subkunci-dan-nilai-dengan-menggunakan-file-reg-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


