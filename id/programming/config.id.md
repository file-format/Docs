{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - File Konfigurasi",
  "description":"Pelajari tentang format file CONFIG dengan contoh CONFIG dan API yang dapat membuat dan membuka file CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Apa itu file CONFIG?
File CONFIG dikenal sebagai file konfigurasi; digunakan untuk mengkonfigurasi parameter dan pengaturan utama untuk beberapa perangkat lunak komputer. Beberapa perangkat lunak hanya membaca **file konfigurasi** saat startup. Lainnya memeriksa file konfigurasi untuk perubahan secara berkala.

## Format File KONFIG
**Format File CONFIG** digunakan untuk proses server, aplikasi perangkat lunak, dan pengaturan sistem operasi. Seorang programmer dapat menulis kode untuk menginstruksikan perangkat lunak untuk membaca file konfigurasi lagi dan lagi setelah periode waktu tertentu dan menerapkan perubahan pada proses saat ini. Tidak ada standar definitif atau konvensi yang kuat untuk sysntax file CONFIG. Misalnya, file Microsoft Web.config termasuk dalam format file CONFIG, yang terdiri dari kumpulan tag berbasis [XML](https://docs.fileformat.com/web/xml/); dapat diedit dengan Microsoft Visual Studio atau editor teks lainnya.

## Contoh file konfigurasi:
Karena, file konfigurasi tidak dibuat dengan mengikuti aturan, standar, atau konvensi apa pun, file ini mungkin ditulis dengan menggunakan format yang berbeda. File .config mungkin didasarkan pada XML, [JSON](https://docs.fileformat.com/web/json/) atau format lainnya. Berikut adalah contoh file konfigurasi untuk sistem operasi dan perangkat lunak terkenal:

### File konfigurasi di Linux
Setiap program Linux adalah file yang dapat dieksekusi yang menyimpan daftar **opcodes** yang dijalankan CPU untuk menyelesaikan operasi biasa. Pengoperasian hampir setiap program dapat disesuaikan dengan kebutuhan Anda dengan mengubah file konfigurasinya. Beberapa file konfigurasi di sistem Linux ada di direktori /etc. File konfigurasi dapat diklasifikasikan ke dalam kategori berikut:
|Kategori|Contoh| Komentar|
---|---|---|
|Akses file|/etc/host.conf|Memberitahu server domain jaringan cara mencari nama host.|
|Booting dan masuk/keluar|/etc/rc.d/rc.local|Tidak resmi. Dapat dipanggil dari rc, rc.sysinit, atau /etc/inittab.|
|Sistem file|/etc/mtools.conf|Konfigurasi untuk semua operasi (mkdir, salin, format, dll.) pada sistem file tipe DOS.|
|Administrasi sistem|/etc/shells|Menyimpan daftar kemungkinan "cangkang" yang tersedia untuk sistem.|
|Networking|/etc/gated.conf|Konfigurasi untuk gated. Hanya digunakan oleh daemon yang terjaga keamanannya.|
|Perintah sistem|/etc/logrotate.conf|Konfigurasi untuk Dynamic Linker.|
|Daemons|/etc/httpd.conf|File konfigurasi untuk Apache, server Web. File ini biasanya tidak ada di /etc.|
|Program pengguna| /etc/lynx.cfg| Pengaturan proxy|
### Contoh file AWS CONFIG
Pengaturan konfigurasi dan kredensial yang sering digunakan dapat disimpan dalam file CONFIG yang dikelola oleh AWS CLI. File CONFIG harus berupa file teks biasa yang menggunakan format berikut:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Contoh file CONFIG SSH
File konfigurasi sisi klien OpenSSH diberi nama CONFIG, dan disimpan di direktori .ssh. File SSH CONFIG terdiri dari struktur berikut:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Contoh file CONFIG Python
File CONFIG Python dapat terlihat seperti ini:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Referensi

* [Memahami file konfigurasi Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Pengaturan file konfigurasi dan kredensial](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [File konfigurasi dengan Python](https://martin-thoma.com/configuration-files-in-python/)

