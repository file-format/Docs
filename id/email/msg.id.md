{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Format Email Microsoft Outlook",
  "description":"Pelajari tentang format file MSG dan API yang dapat membuat dan membuka file MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file MSG?

MSG adalah format file yang digunakan oleh [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) dan Exchange untuk menyimpan pesan email , kontak, janji temu, atau tugas lainnya. Pesan tersebut dapat berisi satu atau lebih bidang email, dengan pengirim, penerima, subjek, tanggal, dan badan pesan, atau informasi kontak, keterangan janji temu, dan satu atau beberapa spesifikasi tugas. Properti yang membentuk objek Pesan, termasuk juga merupakan bagian dari file MSG. File MSG memiliki header, badan pesan utama, dan hyperlink sebagai teks ASCII biasa. File MSG juga cocok dengan program yang membutuhkan Antarmuka Pemrograman Aplikasi Perpesanan (MAPI) Microsoft.

## Struktur File MSG

Format CFB_3 adalah dasar dari file MSG. Paradigma didasarkan pada konsep penyimpanan dan aliran, cukup dekat dengan direktori dan file. Oleh karena itu, perbedaan utama pada yang pertama adalah seluruh hierarki, yang dikemas ke dalam file yang berbeda, yang disebut file gabungan. Objek merupakan file pesan dan terdiri dari satu properti atau koleksinya. Kemampuan ini memfasilitasi aplikasi untuk menyimpan data terstruktur yang rumit dalam satu file. Format ini juga menentukan banyak penyimpanan, setiap penyimpanan mewakili objek Pesan sebagai komponen utama. Penyimpanan ini berisi sejumlah aliran yang mewakili properti dari komponen tersebut. Bersarang penyimpanan juga dimungkinkan.

## Properti Mapi

Di tingkat atas file .msg, penyimpanan berisi aliran yang menyimpan properti di dalamnya. Properti dapat dikategorikan sebagai berikut:

* Properti panjang tetap
* Properti panjang variabel
* Properti bernilai ganda

Terlepas dari kategorinya, properti adalah tag atau nama. Namun, informasi pemetaan yang sesuai diperlukan untuk properti bernama seperti yang ditentukan oleh penyimpanan pemetaannya.

## Penyimpanan

Penyimpanan merupakan komponen kunci dari objek Pesan. Format file MSG menyatakan penyimpanan berikut:

## Struktur Tingkat Atas

Objek pesan mewakili seluruh tingkat teratas dari format file MSG. Bergantung pada jenis, properti, jumlah penerima, dan objek Lampiran, objek pesan dapat memiliki penyimpanan aliran yang berbeda dalam file .MSG yang sesuai.

### Hubungan dengan Struktur Lain

Format file Msg memiliki hubungan berikut dengan struktur lain:

* Basis .msg adalah Compound File Binary File Format.
* Properti yang digunakan oleh Message and Attachment Object Protocol digunakan oleh format ini.

## Skenario untuk menghindari Format MSG

Objek pesan dapat dibagi antara klien atau penyimpanan pesan yang menggunakan sistem file .msg. Ada beberapa keadaan di mana menyimpan objek Message dalam format file .msg tidak sesuai. Sebagai contoh:

* Dalam hal menegakkan arsip mandiri yang besar, lebih baik menggunakan format berfitur lengkap di mana tampilan dapat ditampilkan dengan lebih tepat.
* Jika penerima tidak diketahui, mungkin formatnya tidak didukung oleh penerima dan pribadi atau tidak relevan mungkin dikirimkan.

## Contoh File MSG

Untuk mengetahui tampilan file MSG, Anda dapat mendownload [file sampel MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) dan membukanya di komputer untuk melihat isinya.

## Referensi

* [[MS-OXMSG]: Format File MSG Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

