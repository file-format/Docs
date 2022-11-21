{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "parsial", "ekstensi", "file", "format", "web", "Sindikasi Sangat Sederhana", "Perangkat Lunak Userland" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Sindikasi Sangat Sederhana",
  "description":"Pelajari tentang format file RSS dan API yang dapat membuat dan membuka file RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Apa itu berkas RSS? ##

File dengan ekstensi .rss disebut sebagai Really Simple Syndication. RSS adalah tipe file yang siap atau mudah dibaca oleh komputer, yaitu file XML. File XML ini diperbarui secara otomatis dengan setiap perubahan data atau pembaruan situs web atau halaman web. Informasi yang diperbarui bersama dengan metadata (nama penulis, nama penerbit, tanggal penerbitan, dll.), Dan konten web lainnya dari situs web diekstrak oleh file RSS pengguna dan disajikan dalam format yang mudah dibaca. Fitur terbaik dari file RSS ini adalah ia bekerja secara real-time, dan pembaruan, berita, terbitan, yang terbaru, ditampilkan di bagian atas file. Dengan menggunakan file RSS, Anda dapat dengan mudah membuat file yang berisi pembaruan terkini dari topik apa pun yang Anda minati, dengan menarik konten terkait dari web dan membacanya menggunakan file RSS.

## Sejarah Singkat ##

Dalam dagingnya, file RSS pertama kali dibuat oleh Netscape, mereka menemukan versi pertama dari file RSS tetapi kemudian membuang idenya, dan tidak melanjutkan dengan versi yang lebih baru. Saat itulah **Perangkat Lunak Userland** yang bekerja pada format file RSS dan terus berinovasi dengan versi yang lebih baru, begitulah cara RSS v2 masuk ke pasar. Namun, penemuan RSS dapat dihubungkan kembali ke Resource Description Framework, oleh Ramanathan V pada tahun 1997. Cara kerja kedua file tersebut sangat mirip dan dapat diasumsikan bahwa konsep RSS dibentuk berdasarkan cara kerja RDF, pembaca file yang digunakan untuk mengumpulkan metadata.

## Spesifikasi Teknis ##

File RSS adalah jenis file XML dan semua file RSS harus mengikuti standar XML 1.0. Ada versi berbeda dari file RSS yang berbeda, seperti 0.91, 0.92, 2.0, antara lain. File setiap versi sesuai dengan spesifikasi dan standar versi tertentu itu.

## Contoh RSS ##

Berikut ini adalah contoh sederhana dari RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Referensi ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
