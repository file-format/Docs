{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Pelajari tentang format file TNEF dan API yang dapat membuat dan membuka file TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file TNEF?

Transport Neutral Encapsulation Format (TNEF) adalah hak milik Microsoft, untuk merangkum lampiran email berdasarkan Messaging Application Programming Interface (**MAPI**). Microsoft Outlook dan Microsoft Exchange Server, sepenuhnya mendukung TNEF sementara kemudian menerjemahkan TNEF menjadi MAPI dan menampilkan email yang diformat. Lampiran email dengan pengkodean TNEF memiliki tipe MIME dari MS-TNEF dan disimpan sebagai winmail/win.dat. Lampiran di winmail .dat merangkum informasi berikut:


|Pesan|Objek OLE|Fitur Outlook
---|---|---|
|<ul><li> Lampiran pesan asli</li><li> Versi format asli</li><li> font, ukuran teks, dan warna teks</li></ul> |<ul><li> gambar yang disematkan</li><li> dokumen Office yang disematkan</li></ul> |<ul><li> formulir kustom</li><li> tombol pemungutan suara</li><li> permintaan pertemuan</li></ul>


Layanan email lain yang tidak mendukung TNEF, menyajikan teks biasa untuk pesan berformat TNEF. Outlook menyematkan format pesan yang kaya dalam file TNEF (OLE) atau fitur Outlook tertentu (formulir, tombol polling, dan permintaan konferensi). Pemberian sanksi pengkodean TNEF eksplisit dalam klien email Outlook tidak dimungkinkan, namun, Memilih format RTF untuk pengiriman email secara implisit memfasilitasi pengkodean TNEF.

## Format File TNEF

Algoritme data TNEF membentuk struktur rata dari properti pesan hierarkis yang kaya. Struktur yang diratakan ini kemudian digunakan untuk mewakili aliran data serial yang terdiri dari properti tertentu.

Dalam beberapa situasi, di mana properti muncul dalam grup atau memiliki banyak nilai, aliran mungkin menyertakan hitungan dan padding untuk menerapkan penyelarasan data tertentu. Situasi khas di mana penggunaan algoritme ini menguntungkan adalah dalam lingkungan perpesanan yang tidak mendukung. Dalam lingkungan seperti itu, properti pesan kaya dikodekan ke dalam aliran data serial oleh Penulis TNEF. Selanjutnya, properti yang bukan milik TNEF yang mendasarinya dapat dienkapsulasi selama transmisi. Properti yang dienkapsulasi ini kemudian tersedia dengan decoding melalui TNEF untuk memastikan ketersediaan semua properti dari pesan asli ke aplikasi klien.

Di TNEF semua tipe data numerik adalah little-endian dan ukurannya lebih besar dari satu byte. Penanganan nilai numerik ini pada platform non-little-endian perlu dilakukan transformasi yang sesuai untuk mendapatkan nilai yang benar. Nilai string direpresentasikan dalam format Augmented Backus-Naur Form (ABNF) menurut spesifikasi [RFC5234]. Saat string diakhiri dengan karakter null, string juga disertakan; misalnya, `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="Format File TNEF" >}}

## Atribut TNEF dan aturan Pemrosesan ##

Aliran data di TNEF dimulai dengan nomor versi lawas, tanda tangan, nilai kunci primitif, dan atribut yang mewakili halaman kode. Halaman kode ini dibuat saat encoder merekam atribut dan properti ANSI. Setelah itu, stream menjadi rangkaian atribut dimana atribut pesan berjajar terlebih dahulu kemudian diikuti oleh atribut attachment. Karakteristik pesan dan lampiran yang berbeda terkandung dalam atribut khusus seperti attMsgProps, attAttachment, dan attRecipTable. Atribut yang muncul di aliran TNEF, berisi struktur, properti pesan, dan konversi yang diperlukan untuk melibatkannya dengan properti pesan. Setiap atribut terdiri dari ID, ukuran dan data atribut, checksum dan level sesuai dengan aplikasinya.

## Hubungan dengan Protokol dan Algoritma Lain ##

Sistem yang memiliki mekanisme yang buruk untuk menampilkan format pesan yang kaya secara alami membutuhkan algoritma data TNEF untuk transportasi. Menggunakan tipe media ms-TNEF, keluaran dari algoritme terdiri dari file lampiran (winmail.dat) dan bagian badan MIME yang ditentukan dalam [RFC2045]. Badan pesan teks biasa ditransmisikan menggunakan UUENCODE sesuai dengan spesifikasi [MSDN-UAF] dan badan pesan ini atau metode yang setara didekodekan di sisi penerima. Selain itu, TNEF dapat mengirimkan data pesan menggunakan protokol internet yang berbeda seperti SMTP, POP3, IMAP4, dan lainnya, mengintegrasikan MIME sesuai standar RFC2045.

## Pernyataan Penerapan ##

Selain transmisi pesan sederhana, aplikasi asli TNEF akan dibuat untuk menggunakan kelas pesan dan mendukung fitur tambahan yang tidak memiliki dukungan asli dalam protokol transport. Aplikasi ini disempurnakan lebih lanjut untuk transmisi properti pesan kaya dan properti bernama yang digunakan klien perpesanan modern saat ini. Untuk kepatuhan dengan implementasi asli, sintaks atribut asli dipertahankan dan atribut khusus menyimpan properti pesan baru secara terpisah.

## Referensi

* [Format Enkapsulasi Transportasi Netral](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Alamat email dan buku alamat di Exchange Server](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Algoritma Data Transport Neutral Encapsulation Format (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

