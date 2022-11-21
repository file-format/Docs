{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File P7S - Pesan Email yang Ditandatangani Secara Digital",
  "description":"Pelajari tentang format file P7S dan API yang dapat membuat dan membuka file P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Apa itu file P7S?

File P7S adalah tanda tangan digital yang diterima dengan email yang ditandatangani secara digital. Kehadiran file ini sebagai lampiran email memverifikasi bahwa email dikirim dari sumber asli. Ini memastikan bahwa pengirim memiliki sertifikat Penandatanganan Email yang terinstal di komputer mereka. Ketika email yang ditandatangani dikirim dari komputer pengguna, file P7S dilampirkan dengan nama pengirim. Klien email yang mendukung email bertanda tangan dapat melihat informasi pengirim.

## Format File P7S - Informasi Lebih Lanjut

File P7S S/MIME (Secure/Multipurpose Internet Mail Extensions) berisi informasi dalam format teks biasa yang dapat dibaca manusia. Klien email seperti Microsoft Outlook, Apple Mail, dan dukungan Mozilla Thunderbird untuk membaca informasi yang ditandatangani secara digital dari email S/MIME. Menandatangani email memverifikasi identitas pengirim dan memberi tahu penerima bahwa pesan itu asli. Saat email diunduh dari klien email (baik sebagai [EML](/id/email/eml/) atau [MSG](/id/email/msg/)), file P7S ini ditemukan terlampir dengan email tersebut.

File P7S berisi informasi berikut:

* Sumber asal email
* Tanggal dan waktu saat dikirim,
* Apakah telah dimodifikasi selama transmisi

Informasi ini disematkan menggunakan teknologi Public-Key Cryptography Standard #7 (PKCS7) untuk melampirkan tanda tangan terenkripsi secara digital ke email.

## Referensi ##

* [Microsoft Sign Tool](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

