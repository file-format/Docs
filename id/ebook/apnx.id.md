{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "extension", "file", "format", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file dan API Amazon APNX yang dapat membuat dan membuka file APNX.",
  "title" :"APNX - Indeks Nomor Halaman Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Apa itu file APNX? ##

File Indeks Nomor Halaman Amazon yang menggunakan ekstensi .apnx adalah jenis file eBuku; digunakan oleh Amazon Kindle. File-file ini sebenarnya dikenal sebagai file pagination yang digunakan oleh perangkat Kindle. Jadi file APNX biasanya dibuat untuk menandai halaman eBook Kindle. Fitur paginasi telah dimulai pada perangkat Amazon Kindle sejak firmware 3.1-nya. Itu melihat ke file APNX untuk indeks halaman dan kemudian memetakannya dengan nomor halaman di buku cetak asli. File-file ini disimpan ke perangkat Kindle bersama dengan file Amazon eBooks. Anda tidak dapat membuka atau mengedit file APNX.

## Spesifikasi Format File APNX ##

### Tata Letak

|byte| konten| komentar|
---|---|---|
|4 |00010001 | Pengidentifikasi format. Nilai 65537 little-endian.|
|4 |mulai berikutnya | Offset setelah lokasi akhir dari header pertama. Mulai urutan baru dari header info|
|4 |panjang| Panjang tajuk pertama|
|N |tajuk pertama | String yang berisi tajuk konten. Dimulai urutan berikutnya|
|2 |tidak dikenal | Selalu 1|
|2 |panjang | Panjang tajuk kedua|
|2 |jumlah halaman | Jumlah total byte setelah header kedua yang mewakili halaman. Total ini termasuk byte yang diabaikan oleh pageMap.|
|2 |tidak dikenal | Selalu 32|
|N |tajuk kedua | String berisi header pemetaan halaman|
|4*N |pelapis | Angka pertama yang diberikan pada header pemetaan halaman menunjukkan jumlah 0 byte.|
|4*N |daftar halaman ||

### Tajuk Konten

Header materi terdiri dari string yang disertakan dalam {} yang berisi kunci, pasangan nilai:

|konten| komentar|
---|---|
|panduankonten| Panduan.|
| asin | Pengidentifikasi Amazon untuk versi Kindle dari buku tersebut.|
|cdeType | cdeType MOBI. Harus selalu EBOK untuk ebook.|
|fileRevisionId | Revisi file ini.|

#### Contoh
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Header Pemetaan Halaman
Header pemetaan halaman terdiri dari string yang disertakan dalam {} yang berisi kunci, pasangan nilai.

|konten | komentar|
---|---|
| asin | ISBN 10 untuk buku kertas yang sesuai dengan halaman |
|peta halaman| Tiga tupel nilai. Sepertinya: "(N,N,N)\
1) Jumlah byte setelah header yang memulai urutan penomoran halaman\
2) tidak diketahui\
3) tidak diketahui\|
#### Contoh
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Daftar Halaman

Daftar halaman adalah urutan offset dalam HTML mentah. Setiap
nilai adalah awal dari halaman baru. Setiap entri adalah big endian 4 byte
int.



## Referensi

* [Format file Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - oleh MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

