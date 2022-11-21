{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - File Kontak Virtual",
  "description":"Pelajari tentang format file VCF dan API yang dapat membuat dan membuka file VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file VCF?

VCF (Virtual Card Format) atau vCard adalah format file digital untuk menyimpan informasi kontak. Format ini banyak digunakan untuk pertukaran data di antara aplikasi pertukaran informasi populer. Sebagian besar sistem operasi seperti Windows dan MacOS hadir dengan aplikasi default untuk membuat dan membuka file-file ini. File VCF tunggal dapat berisi informasi kontak untuk satu atau beberapa kontak. File VCF biasanya berisi informasi seperti nama kontak, alamat, nomor telepon, email, ulang tahun, foto, dan audio selain sejumlah bidang lainnya. Didukung oleh klien dan layanan email, tidak ada kehilangan data selama transfer kontak melalui penggunaan format vCard. Jenis media untuk format file VCF adalah teks/vcard.

## Format File VCF

File VCF bersifat tekstual dan dapat dibaca manusia. Ini dapat dibuka di editor teks seperti Notepad di Microsoft Windows dan TextEdit di MacOS. Namun, jika ada gambar di file, itu tidak akan ditampilkan di editor teks.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) menyediakan dukungan untuk membuka file VCF serta mengonversi ke sejumlah format lain seperti format [MSG](/id/email/msg/) yang populer. Format file VCF ditingkatkan dengan waktu dari versi 2.1 ke 4.0 menambahkan informasi rinci ke format file. Format ini juga digunakan untuk mengekspor kontak telepon dan kemudian mengimpor di perangkat lain.

{{< figure src="../VCF.png" alt="Format File VCF" >}}

### Contoh VCF 2.1

Berikut adalah contoh versi 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Contoh VCF 3.0

Berikut adalah contoh versi 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Contoh VCF 4.0

Berikut adalah contoh versi 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Referensi

* [VCF - Oleh Wikipedia](https://en.wikipedia.org/wiki/VCard)

