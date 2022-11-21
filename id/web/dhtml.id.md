{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml", "file dhtml", "format file dhtml", "jenis file dhtml", "file", "ketik", "apa itu file dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Format Berkas HTML Dinamis",
  "description":"Pelajari tentang format file DHTML dan API yang dapat membuat dan membuka file DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DHTML?

File dengan ekstensi .dhtml adalah file [HTML](/id/web/html/) dinamis yang digunakan untuk membuat konten halaman web yang dinamis. Elemen web yang dibuat dalam DHTML digerakkan oleh peristiwa dan tidak perlu memuat ulang halaman. Dalam sebagian besar kasus, file DHTML digunakan untuk membuat konten dinamis halaman web seperti menu drop-down, layer mengambang, tombol rollover, dan konten dinamis lainnya. Anda menemukan elemen html dinamis hampir setiap hari dalam hidup Anda saat Anda mengarahkan mouse ke item menu dan membuka opsi sub-menu lebih lanjut. DHTML memanfaatkan teknologi web seperti [HTML](/id/web/html/), [Javascript](/id/web/js/), HTML DOM, HTML Events, dan [CSS](/id/web/css/) untuk mencapai dinamika perilaku elemen.

## Format File DHTML

File DHTML adalah file teks biasa yang berisi kode DHTML untuk mengimplementasikan perilaku dinamis elemen web.


### DHTML DOM

Model objek dokumen DHTML (DOM) didasarkan pada DOM HTML yang merupakan struktur pohon dengan elemen, atribut, dan teks seperti yang ditunjukkan pada gambar berikut.

{{< figure src="../dhtml.png" alt="HTML-DOM" >}}

Node `Document` dapat digunakan untuk memanggil beberapa fungsi untuk mengimplementasikan fungsi yang berbeda. Contoh berikut hanya menggunakan metode document.write() dari JavaScript di DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Kode ini menulis teks "Hello World" untuk ditampilkan di browser.

### Acara DHTML

|S.No.|Acara|Kejadian|
---|---|---|
|1|onabort|Itu terjadi ketika pengguna membatalkan pemuatan halaman atau file media.|
|2|onblur|Itu terjadi ketika pengguna meninggalkan objek HTML.|
|3|onchange|Itu terjadi ketika pengguna mengubah atau memperbarui nilai suatu objek.|
|4|onclick|Ini terjadi atau terpicu saat ada pengguna yang mengklik elemen HTML.|
|5|ondblclick|Itu terjadi ketika pengguna mengklik elemen HTML dua kali bersamaan.|
|6|onfocus|Itu terjadi ketika pengguna berfokus pada elemen HTML. Event handler ini bekerja berlawanan dengan onblur.|
|7|onkeydown|Ini dipicu saat pengguna menekan tombol pada perangkat keyboard. Event handler ini berfungsi untuk semua kunci.|
|8|onkeypress|Ini dipicu saat pengguna menekan tombol pada keyboard. Penangan kejadian ini tidak dipicu untuk semua kunci.|
|9|onkeyup|Itu terjadi ketika pengguna melepaskan kunci dari keyboard setelah menekan objek atau elemen.|
|10|onload|Itu terjadi ketika sebuah objek dimuat sepenuhnya.|
|11|onmousedown|Itu terjadi ketika pengguna menekan tombol mouse di atas elemen HTML.|
|12|onmousemove|Itu terjadi ketika pengguna memindahkan kursor pada objek HTML.|
|13|onmouseover|Itu terjadi ketika pengguna menggerakkan kursor di atas objek HTML.|
|14|onmouseout|Ini terjadi atau dipicu saat penunjuk tetikus dipindahkan dari elemen HTML.|
|15|onmouseup|Itu terjadi atau dipicu saat tombol mouse dilepaskan di atas elemen HTML.|
|16|onreset|Ini digunakan oleh pengguna untuk mereset formulir.|
|17|onselect|Itu terjadi setelah memilih konten atau teks pada halaman web.|
|18|onsubmit|Ini dipicu ketika pengguna mengklik tombol setelah pengiriman formulir.|
|19|onunload|Ini dipicu saat pengguna menutup halaman web.|

## Referensi

* [HTML Dinamis - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

