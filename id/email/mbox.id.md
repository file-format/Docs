{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - File Kotak Surat Email",
  "description":"Pelajari tentang format file MBOX dan API yang dapat membuat dan membuka file MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file MBOX?

Format file MBox adalah istilah umum yang mewakili wadah untuk kumpulan pesan surat elektronik. Pesan disimpan di dalam wadah bersama dengan lampirannya. Pesan dari seluruh folder disimpan dalam satu file database dan pesan baru ditambahkan ke akhir file. Banyak aplikasi dan API memberikan dukungan untuk format file MBox seperti Apple Mail dan Mozilla Thunderbird.

## Format File MBOX ##

Format file MBox tetap tidak standar untuk waktu yang cukup lama hingga tahun 2005 ketika aplikasi/mbox distandarisasi sebagai [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Pesan, dalam format RFC 2822 , digabungkan di dalam format file MBox satu demi satu. Setiap pesan dimulai dengan garis pemisah yang mengidentifikasi pengirim pesan, dan juga mengidentifikasi tanggal dan waktu di mana pesan diterima oleh penerima akhir (baik sistem last-hop di jalur transfer, atau sistem yang berfungsi sebagai jalur penerima). toko surat). Setiap pesan biasanya diakhiri dengan baris kosong. Akhir dari database biasanya dikenali dengan tidak adanya data tambahan, atau dengan adanya penanda akhir file yang eksplisit.

## Membaca Pesan dari File MBox ##

Pembaca memindai file mbox untuk mencari From_ lines. Baris Dari_ apa pun menandai awal pesan. Pembaca tidak boleh mencoba memanfaatkan fakta bahwa setiap baris From_ (melewati awal file) adalah baris kosong. Setelah pembaca menemukan pesan, ia mengekstrak pengirim amplop (kemungkinan rusak) dan tanggal pengiriman dari baris From_. Ini kemudian membaca hingga baris From_ atau akhir file berikutnya, mana saja yang lebih dulu. Ini menghapus baris kosong terakhir dan menghapus kutipan >Dari_ baris dan >>Dari_ baris dan seterusnya. Hasilnya adalah pesan RFC 822.

## Pertimbangan Pengodean ##

Konten file MBox dapat bercampur secara permanen ketika email yang diterima berisi file Mbox sebagai lampiran dan disimpan di file Mbox lain. Untuk menghindari hal ini, sistem perpesanan harus menyandikan database mbox dengan pengkodean transfer non-transparan (seperti BASE64 atau Quoted-Printable) setiap kali objek tersebut ditransfer melalui protokol perpesanan. Pelaksana juga harus bersiap untuk menyandikan data mbox secara lokal jika data yang tidak sesuai diterima.

## Referensi ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

