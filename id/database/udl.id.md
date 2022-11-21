{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "ekstensi", "file udl", "format file udl", "Tipe File Basis Data", "Format File Basis Data", "apa itu file udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file UDL dan API yang dapat membuat dan membuka file UDL.",
  "title" :"UDL - File Tautan Data Universal Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Apa itu file UDL?
File dengan ekstensi .udl disebut file Microsoft Universal Data Link; menentukan atribut koneksi; digunakan oleh aplikasi Windows untuk membuat koneksi dengan database. File UDL berisi string koneksi untuk sumber data OLE DB; dengan nama pengguna dan kata sandi dan properti string koneksi penting. Untuk menghindari menentukan properti secara langsung dalam string koneksi, kotak dialog Properti Tautan Data dapat digunakan untuk menyimpan informasi koneksi dalam file .udl sebagai alternatif.

## Format File UDL
Pada dasarnya, file UDL (Universal Data Link) adalah file teks sederhana yang terdiri dari string koneksi database dengan atribut atau properti tertentu. Setelah file UDL dibuat, dapat diuji dengan menggunakan SQL Server Management Studio untuk memverifikasi konektivitas.

### Properti string koneksi
Properti berikut dapat diatur dalam UDL untuk memastikan konektivitas yang tepat:

- **Nama Server**: lokasi server tempat database yang ingin Anda akses berada.
- **Opsi Otentikasi**
- **Otentikasi Windows**: Otentikasi ke SQL Server menggunakan kredensial akun Windows pengguna yang saat ini masuk.
- **Otentikasi SQL Server**: Otentikasi menggunakan ID login dan kata sandi.
- **Active Directory - Terintegrasi**: Autentikasi terintegrasi dengan identitas Azure Active Directory; juga dapat digunakan untuk otentikasi Windows ke SQL Server.
- **Active Directory - Password**: User ID dan autentikasi kata sandi dengan identitas Azure Active Directory.
- **Active Directory - Universal dengan dukungan MFA**: Autentikasi interaktif dengan identitas Azure Active Directory.
- **Active Directory - Service Principal**: Autentikasi dengan prinsipal layanan Azure Active Directory.
- **Server SPN**: Jika Anda menggunakan koneksi tepercaya, Anda dapat menentukan nama prinsip layanan (SPN) untuk server.
- **Nama pengguna**: Ketik ID Pengguna yang akan digunakan untuk autentikasi saat Anda masuk ke sumber data.
- **Kata Sandi**: Ketik kata sandi yang akan digunakan untuk autentikasi saat Anda masuk ke sumber data.
- **Kata sandi kosong**: Jika dicentang, memungkinkan penyedia yang ditentukan untuk menggunakan kata sandi kosong di string koneksi.
- **Izinkan menyimpan kata sandi**: Memungkinkan kata sandi disimpan dengan string koneksi.
- **Gunakan enkripsi yang kuat untuk data**: data yang melewati koneksi akan dienkripsi.
- **Trust server certificate**: Sertifikat server akan divalidasi.
- **Database**: Nama database yang ingin Anda akses.
- **Lampirkan file database sebagai nama database**: Menentukan nama file utama untuk database yang dapat dilampirkan.

## Referensi ##

* [Komponen Akses Data Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Konfigurasi Universal Data Link (UDL)](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

