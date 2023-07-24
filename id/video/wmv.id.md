{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas WMV",
  "description":"Pelajari tentang format file WMV dan API yang dapat membuat dan membuka file WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Apa itu file WMV?

Advanced Systems Format (ASF) adalah wadah multimedia digital yang dirancang terutama untuk menyimpan dan mentransmisikan aliran media. Microsoft Windows Media Video (WMV) adalah format video terkompresi dan Microsoft Windows Media Audio (WMA) adalah format audio terkompresi bersama dengan metadata tambahan dalam wadah ASF yang dikembangkan oleh Microsoft. Setelah file WMV atau WMA dikodekan dengan Windows Media Video dan Windows Media Audio codec kemudian direpresentasikan dengan ekstensi .asf. WMV mengompres file besar untuk kecepatan transmisi yang lebih baik melalui jaringan dengan tetap menjaga kualitas video. WMV dirancang khusus untuk berjalan di semua perangkat Windows. Setelah standardisasi oleh Society of Motion Picture and Television Engineers (SMPTE), WMV sekarang dianggap sebagai format standar terbuka.

## Sejarah ##

Dengan bantuan codec milik Microsoft, format video terkompresi baru dikembangkan pada tahun 1999 yang dikenal sebagai WMV7 yang didasarkan pada MPEG-4 Bagian 2. Perbaikan ditambahkan dalam dua versi selanjutnya yaitu WMV8 dan 9. Microsoft mengirimkan versi ke-9^^ dari WMV ke SMPTE untuk standardisasi pada tahun 2003 yang akhirnya distandarisasi pada tahun 2006 sebagai SMPTE 421M juga dikenal sebagai VC-1. Ide di balik WMV adalah untuk mengembangkan format media yang dapat didukung oleh semua perangkat keras dan perangkat lunak yang didukung Microsoft. Selain itu, tujuan utama lainnya adalah mengirimkan aliran video melalui internet dalam skenario yang optimal. Setelah standarisasi dari SMPTE, WMV juga menjadi format video untuk cakram Blu-ray.

## Spesifikasi Format File

### Kontainer

Secara umum, WMV dikemas ke dalam wadah ASF tetapi selain itu, wadah Matroska atau AVI juga dapat mendukungnya dengan ekstensi masing-masing .mkv dan .avi.

### Video Windows Media 9

Meskipun ada berbagai codec audio dan video yang tersedia di seri Windows Media Video 9 untuk pembuatan dan pemutaran media digital, codec WMV-9 adalah codec video terbaru dan terbaik karena dapat mencapai kompresi optimal dari kecepatan bit yang sangat rendah yaitu 160 x 120 pada 10 Kbps hingga 1920 x 1080 pada 4-8 Mbps untuk berbagai video HD.

### Struktur Codec

WMV-9 memiliki format warna internal 8 bit 4:2:0. Seperti semua standar kompresi video populer lainnya MPEG-1 dan H.261, WMV-9 menggunakan kompensasi gerak berbasis blok dan skema transformasi spasial. Secara umum, kita dapat mengatakan bahwa standar ini melakukan kompensasi gerakan blok demi blok dari kerangka yang direkonstruksi sebelumnya dengan bantuan kuantitas 2-D yang disebut vektor gerak (MV) untuk memberi sinyal perpindahan spasial. Blok arus dibentuk dengan bantuan memprediksi nilai dari ukuran yang sama dengan bingkai yang direkonstruksi sebelumnya yang dipindahkan dari posisi saat ini oleh vektor gerak. Akhirnya, kesalahan residual dihitung sebagai perbedaan antara blok yang diprediksi dengan kompensasi gerakan dan blok yang sebenarnya. Kesalahan residual ini ditransformasikan menggunakan transformasi pemadatan energi linier kemudian dikuantisasi dan diberi kode entropi.

Koefisien transformasi terkuantisasi didekodekan dengan entropi, didekuantisasi, dan ditransformasikan terbalik untuk menghasilkan perkiraan kesalahan residual pada sisi dekoder, yang kemudian ditambahkan ke prediksi kompensasi gerakan untuk menghasilkan rekonstruksi. Deskripsi codec tingkat tinggi ditunjukkan pada gambar berikut.

Bagian selanjutnya akan membahas peningkatan baru dalam WMV-9 yang membedakannya dari solusi pengkodean video lainnya seperti standar MPEG. WMV-9 memiliki bingkai intra (I), prediksi (P), dan prediksi dua arah (B). Frame intra adalah mereka yang dikodekan secara independen dan tidak memiliki ketergantungan pada frame lain. Bingkai yang diprediksi adalah bingkai yang bergantung pada satu bingkai di masa lalu. Decoding dari frame yang diprediksi dapat terjadi hanya setelah semua frame referensi sebelum frame saat ini mulai dari frame (I) terbaru telah didekodekan. Bingkai B adalah bingkai yang memiliki dua rujukan—satu di masa lalu yang bersifat sementara dan satu lagi di masa depan yang bersifat sementara. Frame B ditransmisikan setelah referensi mereka, yang berarti bahwa frame B dikirim keluar untuk memastikan bahwa referensi mereka tersedia pada saat decoding. Bingkai B di WMV-9 tidak digunakan sebagai referensi untuk bingkai berikutnya. Ini menempatkan frame B di luar loop decoding, memungkinkan pintasan diambil selama decoding frame B tanpa penyimpangan atau artefak visual jangka panjang. Definisi bingkai I, P, dan B di atas berlaku untuk urutan progresif dan interlaced.

Performa codec video dibandingkan dengan plot rate-distortion (RD) mereka. Ini adalah kurva 2-D yang menunjukkan distorsi yang dihasilkan oleh kompresi pada bitrate tertentu.

WMV-9 telah mengatasi masalah ini dengan pengenalan berbagai teknik yang tercantum di bawah ini:

1. Transformasi ukuran blok adaptif

2. Set transformasi presisi terbatas

3. Kompensasi gerak

4. Kuantisasi dan dekuantisasi

5. Pengodean entropi tingkat lanjut

6. Penyaringan loop

7. Pengkodean bingkai B tingkat lanjut

8. Jalin kode

9. Perataan tumpang tindih

10. Alat dengan tarif rendah

11. Kompensasi memudar

## Referensi ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


