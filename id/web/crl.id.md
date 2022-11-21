{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CRL - Daftar Pencabutan Sertifikat",
  "description":"Pelajari tentang format file CRL dan API yang dapat membuat dan membuka file CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Apa itu file CRL?

File CRL (Daftar Pencabutan Sertifikat) adalah daftar hitam sertifikat digital X.509 yang dicabut oleh otoritas sertifikat (CA) sebelum tanggal pencabutan yang ditetapkan. Ini berisi informasi tentang masalah dan tanggal pencabutan yang memungkinkan administrator keamanan memblokir sertifikat digital yang terpengaruh. CRL tidak menyertakan sertifikat kedaluwarsa karena tujuan utamanya adalah untuk memberi tahu tentang sertifikat yang tidak tepercaya dan tidak valid.

Aplikasi yang dapat **membuka file CRL** termasuk OpenSSL, Microsoft IIS Server, dan Citrix NetScaler.

## Format File CRL - Informasi Lebih Lanjut

File CRL berisi informasi dalam standar X.509 yang juga menentukan semantiknya untuk berbagi informasi kunci publik. Informasi lain yang terkandung di dalam file CRL mungkin termasuk batas waktu sertifikat dicabut, alasan pencabutan, nomor seri sertifikat dicabut dan stempel waktu.


### Alasan Utama Sertifikat Ditambahkan ke CRL

Mungkin ada beberapa alasan untuk mencabut sertifikat situs web Anda dan ditambahkan ke CRL. Beberapa dari mereka mungkin;

1. Kunci privat sertifikat Anda telah disusupi
1. Sertifikat Anda tidak valid atau salah diterbitkan oleh CA
1. Detail organisasi yang terkait dengan sertifikat diubah dan CA mengeluarkan sertifikat baru
1. Alasan lain yang tidak dapat dihindari untuk pencabutan sertifikat

## Referensi

* [Institut Standar dan Teknologi Nasional (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Daftar Pencabutan Sertifikasi](https://en.wikipedia.org/wiki/Certificate_revocation_list)

