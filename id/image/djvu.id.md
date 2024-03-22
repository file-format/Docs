{
  "date" : "2019-10-11",
  "keywords" :[ "file djvu", "format file djvu", "apa itu file djvu", "file", "contoh djvu", "ekstensi file djvu", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File DJVU",
  "description":"Pelajari tentang format file DJVU dan API yang dapat membuat dan membuka file DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DJVU?

DjVu, diucapkan sebagai "déjà vu", adalah format file grafik yang ditujukan untuk dokumen dan buku yang dipindai terutama yang berisi kombinasi teks, gambar, gambar, dan foto. Ini dikembangkan oleh AT&T Labs. Ini menggunakan beberapa teknik seperti pemisahan lapisan gambar dari teks dan gambar latar belakang, pemuatan progresif, pengkodean aritmatika dan kompresi lossy untuk gambar bitonal. Karena file DJVU dapat berisi gambar, foto, teks, dan gambar berwarna yang dikompresi namun berkualitas tinggi dan dapat disimpan dalam ruang yang lebih kecil, oleh karena itu, ini digunakan di web sebagai eBuku, manual, surat kabar, dokumen kuno, dll.

DjVu dapat dinilai sebagai alternatif yang lebih unggul dari [PDF](/id/pdf/). Ekstensi file yang terkait dengan DjVu adalah .DJVU atau .DJV. DjVu dapat mencapai rasio kompresi sekitar 5 – 10 lebih baik daripada metode yang ada seperti [JPEG](/id/image/jpeg/) & [GIF](/id/image/gif/) untuk dokumen berwarna dan 3 – 8 kali lebih baik daripada [TIFF](/image/tiff/) dalam dokumen hitam putih. Dokumen yang dipindai pada 300 DPI dengan warna penuh hingga 25 MB dapat dikompres hingga 30 hingga 100 KB. Demikian pula dokumen hitam putih dapat dikompresi hingga 5 hingga 30 KB. Halaman HTML rata-rata bisa mencapai 50 KB, oleh karena itu, dokumen-dokumen ini dapat diunggah di internet tanpa masalah.

## Sejarah Singkat ##

Teknologi DjVu dikembangkan di laboratorium AT&T oleh [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, dan Paul G dari tahun 1996 hingga 2001. Format file DjVu telah melewati berbagai revisi, yang terbaru dari tahun 2005.


|Versi|Tanggal rilis|Catatan
---|---|---|
|1–19|1996–1999|Ini adalah versi pengembangan.
|20|April 1999|Single page diubah menjadi format Multipage.
|23|Juli 2002|bagian CID
|24|Februari 2003|LTAnno bongkahan
|21|September 1999|Format penyimpanan tidak langsung diganti. Lapisan pencarian teks telah ditambahkan.
|22|April 2001|Orientasi halaman, warna JB2
|25|Mei 2003|NAVM potongan. Dukungan untuk bookmark DjVu telah ditambahkan.
|26|April 2005|Anotasi teks/baris

## Format File DjVu ##

Dokumen DjVu adalah file IFF85. Strukturnya menyediakan hierarki wadah yang menyimpan informasi dalam file DjVu. Wadah ini juga disebut "Potongan". Tipe bongkahan dan ID bongkahan menjelaskan bagaimana bongkahan digunakan. Ada header 4byte diikuti oleh struktur IFF. Empat byte pertama file DjVu adalah 0x41 0x54 0x26 0x54. Bagian ini membahas berbagai jenis dokumen DjVu dan bagian-bagiannya yang sesuai.


|Chunk ID|Penggunaan
---|---|
|BENTUK|Potongan komposit memiliki empat byte data pertama dari potongan FORM yang merupakan pengidentifikasi sekunder.
|FORM:DJVM|Dokumen DjVu multi halaman. Potongan komposit yang berisi potongan DIRM.
|FORM:DJVU|Dokumen DjVu satu halaman. Potongan komposit yang berisi potongan yang membentuk halaman dalam dokumen djvu.
|FORM:DJVI|File DjVu “bersama” yang disertakan melalui potongan INCL. Anotasi bersama dan kamus bentuk.
|FORM:THUM|Composite chunks yang berisi TH44 chunks yang merupakan thumbnail tersemat.
|DIRM|Informasi nama halaman untuk dokumen multi-halaman.
|NAVM|Informasi bookmark
|ANTa, ANTz|Anotasi termasuk pengaturan tampilan awal dan overlay hyperlink, kotak teks, dll.
|TXTa, TXTz|Teks Unicode dan informasi tata letak.
|Djbz|Tabel bentuk bersama.
|Sjbz|BZZ mengompresi data bitonal JB2 yang digunakan untuk menyimpan mask.
|FG44|Data IW44 digunakan untuk menyimpan latar depan
|BG44|Data IW44 digunakan untuk menyimpan latar belakang
|TH44|Data IW44 digunakan untuk menyimpan gambar thumbnail tersemat
|WMRM|JB2 diperlukan data untuk menghapus watermark
|FGbz|Warna data JB2. Memberikan warna untuk masing-masing (blit atau bentuk?) di potongan Sjbz yang sesuai.
|INFO|Informasi tentang halaman DjVu
|INCL|ID dari potongan FORM:DJVI yang disertakan.
|BGjp|latar belakang yang disandikan JPEG
|FGjp|JPEG disandikan latar depan
|Smmr|masker yang disandikan G4

### Kompresi DJVU

Gambar tunggal dibagi menjadi banyak gambar berbeda, dan kemudian setiap gambar dikompresi secara terpisah. Untuk pembuatan file DjVu, gambar pertama-tama dipisahkan menjadi tiga gambar, latar belakang, latar depan, dan gambar topeng. Biasanya gambar latar belakang dan latar depan adalah gambar berwarna dengan resolusi lebih rendah; tetapi gambar topeng adalah gambar beresolusi lebih tinggi dan biasanya teks disimpan di sana. Setelah pemisahan gambar latar depan dan latar belakang dikompresi melalui algoritma kompresi berbasis wavelet IW44, sedangkan gambar topeng dikompresi menggunakan metode lain yang disebut JB2.

Metode pengkodean JB2 menghilangkan banyak redundansi dalam gambar teks dengan mengidentifikasi bentuk yang identik pada halaman, seperti beberapa kemunculan karakter dalam font tertentu. JB2 pertama-tama mengkodekan bitmap dari setiap bentuk unik dengan memanfaatkan redundansi antara bentuk serupa. Ini kemudian memberi kode lokasi di mana setiap bentuk muncul di halaman. Baik JB2 dan IW44 mengandalkan tipe baru pembuat kode aritmatika biner adaptif yang disebut ZP-coder yang memeras redundansi yang tersisa dalam beberapa persen dari batas Shannon. ZP-coder bersifat adaptif, dan lebih cepat daripada coders aritmatika biner perkiraan lainnya.

## Referensi ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Format File DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

