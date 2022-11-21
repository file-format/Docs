{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - File Templat Email Microsoft Outlook",
  "description":"Pelajari tentang format file OFT dan API yang dapat membuat dan membuka file OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file OFT?

File dengan ekstensi .oft adalah file template yang dibuat menggunakan Microsoft Outlook. Set tata letak yang telah diformat sebelumnya untuk template pesan kemudian digunakan untuk mengirimkan email dengan informasi umum untuk menghemat waktu. File tersebut dapat dibuat dengan membuat email baru, menambahkan informasi yang diperlukan, lalu menggunakan dropdown Save As Office Template (.oft) dari Microsoft Outlook. Pengguna dapat membuka file OFT dengan mengklik dua kali dan itu akan terbuka di aplikasi terkait pada sistem tertentu.

## Struktur File Sering ##

Format file .OFT menggunakan format file [MSG](/id/email/msg/) pada dasarnya. Satu-satunya perbedaan adalah file OFT memiliki CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) sebagai kelas penyimpanan (WriteClassStg), sedangkan file MSG menggunakan CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

Format CFB_3 adalah dasar dari file MSG. Paradigma didasarkan pada konsep penyimpanan dan aliran, cukup dekat dengan direktori dan file. Oleh karena itu, perbedaan utama pada yang pertama adalah seluruh hierarki, yang dikemas ke dalam file yang berbeda, yang disebut file gabungan. Objek merupakan file pesan dan terdiri dari satu properti atau koleksinya. Kemampuan ini memfasilitasi aplikasi untuk menyimpan data terstruktur yang rumit dalam satu file. Format ini juga menentukan banyak penyimpanan, setiap penyimpanan mewakili objek Pesan sebagai komponen utama. Penyimpanan ini berisi sejumlah aliran yang mewakili properti dari komponen tersebut. Bersarang penyimpanan juga dimungkinkan.

### Properti Sering

Di tingkat atas file .msg, penyimpanan berisi aliran yang menyimpan properti di dalamnya. Properti dapat dikategorikan sebagai berikut:

* Properti panjang tetap
* Properti panjang variabel
* Properti bernilai ganda

Terlepas dari kategorinya, properti adalah tag atau nama. Namun, informasi pemetaan yang sesuai diperlukan untuk properti bernama seperti yang ditentukan oleh penyimpanan pemetaannya.

### Penyimpanan SERING

Penyimpanan merupakan komponen kunci dari objek Pesan. Format file MSG menyatakan penyimpanan berikut:

### Struktur Tingkat Atas

Objek pesan mewakili seluruh tingkat teratas dari format file Msg. Bergantung pada jenis, properti, jumlah penerima, dan objek Lampiran, objek pesan dapat memiliki penyimpanan aliran yang berbeda dalam file .MSG yang sesuai.

#### Hubungan dengan Struktur Lain

Format file MSG/OFT memiliki hubungan berikut dengan struktur lain:

* Basis .msg adalah Compound File Binary File Format.
* Properti yang digunakan oleh Message and Attachment Object Protocol digunakan oleh format ini.

## Referensi

* [[MS-OXMSG]: Format File MSG Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

