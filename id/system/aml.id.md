{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AML - File Bahasa Mesin ACPI",
  "description":"Pelajari tentang format file ACPI AML dan API yang dapat membuat dan membuka file AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Apa itu file AML?

File AML adalah file sistem yang dibuat dengan bahasa Advanced Configuration and Power Interface (ACPI) yang digunakan untuk mengonfigurasi properti perangkat keras. Ini berisi kode byte independen mesin yang digunakan untuk mengonfigurasi perangkat keras bahkan untuk operasi sederhana seperti mematikan komputer. File AML mungkin berisi instruksi tergantung pada tujuan penginstalannya di mesin. Implementasi standar ACPI memungkinkan Anda meningkatkan fungsionalitas manajemen daya dan antarmuka yang tangguh untuk mengonfigurasi perangkat motherboard seperti motherboard P55.

## Format File AML ACPI

File AML disimpan sebagai file biner ke disk dengan konten yang ditulis dalam kode byte. Spesifikasi format file standar ACPI tersedia di [uefi](https://uefi.org/). Bahasa ini telah dirancang untuk menawarkan stabilitas dan kompatibilitas mundur, membutuhkan lebih sedikit penulisan ulang atau pembuatan ulang tumpukan aplikasi.

## Spesifikasi Format File AML

File AML terdiri dari tabel DSDT dan SSDT. Kode byte AML dibaca dan diuraikan dari awal setiap tabel ini. Ini memberikan informasi tentang definisi perangkat dan objek di ruang nama ACPI. Dengan menggunakan informasi ini, juru bahasa AML dapat membuat daftar semua perangkat yang tersedia di sistem, serta properti dan fungsinya yang didukung.

### Contoh Kode ASL untuk DSDT

Contoh kode ASL untuk DSDT adalah sebagai berikut.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Referensi

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

