{
  "date" : "2019-10-11",
  "keywords" :[ "file aba", "format file aba", "apa itu file aba", "file", "contoh aba", "ekstensi file aba", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Format File CemText",
  "description":"Pelajari tentang format file ABA dan API yang dapat membuat dan membuka file ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Apa itu file ABA?

File dengan ekstensi .aba adalah format file Australian Bankers Association (ABA) atau [Cemtext](https://www.cemtexaba.com/) yang digunakan oleh bank untuk transaksi batch. Ini digunakan oleh sebagian besar Bank untuk pencatatan keuangan. Juga dikenal sebagai file Entri Langsung, format file ABA telah diadopsi oleh sebagian besar bank Australia sebagai format default untuk transaksi batch. Itu masih belum diakui sebagai format Standar meskipun faktanya telah digunakan oleh Bank of Queensland, NAB dan Westpac. File ABA dapat dibuka dengan editor teks apa pun seperti Notepad ++.


## Format File ABA

File ABA menggunakan format ASCII untuk menyimpan data untuk diteruskan atau dimuat ke sistem perbankan. Formatnya dibuat sederhana untuk memudahkan integrasi ke dalam sistem keuangan perusahaan sendiri untuk memproses kumpulan transaksi. Misalnya, dalam sistem penggajian, sekumpulan transaksi dapat diunggah untuk diproses dalam satu klik. Spesifikasi format file ABA tersedia sebagai transkrip lengkap di situs web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) dan dapat dirujuk untuk referensi developer .

File ABA terdiri dari beberapa baris di mana setiap baris dikenal sebagai `record`. Ada tiga catatan utama dalam file ABA:

* Catatan Deskriptif
* Catatan Detil
* File Catatan Total

### Catatan Deskriptif

Sebuah `Rekaman Deskriptif` berisi informasi seperti Nomor Urutan Reel, Nama Lembaga Keuangan Pengguna, File penyedia Nama Penggunaan, dan informasi lainnya.

### Catatan Detail

Jenis `Detail Record` mencakup informasi seperti Nomor Bank/Negara Bagian/Cabang, Nomor Rekening yang akan dikreditkan/didebit, Indikator, Kode Transaksi, Jumlah, dan informasi lainnya.

### Berkas Total Catatan

Tipe "File Total Record" meliputi Record Type 7, BSB Format Filler, File (User) Net Total Amount, File (User) Credit Total Amount, File (User) Debit Total Amount, dan informasi lainnya.

### Kode Transaksi

Daftar kode transaksi yang valid adalah sebagai berikut. Sering kali, kode "53 - Bayar" digunakan dalam file ABA. Kode transaksi ini mencakup debit, kredit, dan pemotongan pajak.

|Kode|Deskripsi Transaksi|
---|---|
|13|Item debit yang dimulai secara eksternal|
|50|Item kredit yang diprakarsai secara eksternal dengan pengecualian yang membawa Kode Transaksi|
|51|Kepentingan Keamanan Pemerintah Australia|
|52|Tunjangan Keluarga|
|53|Bayar|
|54|Pensiun|
|55|Pembagian|
|56|Dividen|
|57|Bunga Surat Utang/Catatan|

## Contoh File ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referensi

* [Cemtext ABA](https://www.cemtexaba.com/)

