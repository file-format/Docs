{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File AXD - Format File Pengendali Web ASP.NET",
  "description" :"Pelajari tentang apa itu file AXD dan API yang dapat membuat dan membuka file AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Apa itu file AXD?

File AXD adalah file pengaturan web yang digunakan untuk menangani dan mengambil permintaan sumber daya tertanam di ASP.NET. Ini terdiri dari instruksi untuk mengambil sumber daya yang disematkan seperti gambar, file JavaScript ([.JS](/id/web/js/)), dan file [.CSS](/id/web/css/). File AXD digunakan untuk memasukkan sumber daya ke halaman sisi klien. Hal ini memungkinkan halaman klien untuk mengakses sumber daya ini di server dengan cara standar.

## Format File AXD

File AXD disimpan sebagai file biner di sisi server. Ini mengacu pada file Web Handler di ASP.NET yang merupakan komponen yang menghasilkan respons terhadap permintaan spesifik ke server web. File AXD melakukan pemrosesan khusus sebelum menghasilkan respons berdasarkan permintaan halaman sisi klien. Ini biasanya disimpan sebagai file **WebResource.axd**.

### Apa itu berkas WebResource.axd?

Sebagian besar proyek ASP.NET menyimpan file AXD sebagai file WebResource.axd yang memungkinkan halaman sisi klien mengunduh sumber daya yang tertanam dalam rakitan. Aplikasi Anda mungkin menghadapi kinerja yang lambat jika Anda menjalankannya dalam mode debug karena pengendali WebResources.axd tidak di-cache.

## Referensi

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

