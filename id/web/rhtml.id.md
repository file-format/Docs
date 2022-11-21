{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml", "file rhtml", "format file rhtml", "jenis file rhtml", "file", "ketik", "apa itu file rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Halaman Ruby HTML",
  "description":"Pelajari tentang format file RHTML dan API yang dapat membuat dan membuka file RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Apa itu file RHTML?

File dengan ekstensi .rhtml adalah file [HTML](/id/web/html/) sisi server yang berisi kode atau skrip Ruby. Kode dieksekusi di server menggunakan Ruby on Rails yang berjalan di backend. Bagi mereka yang tidak tahu tentang Ruby on Rails, ini adalah kerangka kerja full-stack untuk mengembangkan aplikasi web dengan database backend berdasarkan pola Model-View-Control. Sederhananya, RHTML adalah kombinasi dari HTML dan Ruby di mana kekuatan skrip/pemrograman Ruby tersedia untuk pengembang web menggunakan tag HTML.

## Format Berkas RHTML

File RHTML ditulis dalam format teks biasa seperti file web berbasis teks lainnya. Kode yang akan dieksekusi dilampirkan di dalam `<% %>` sementara untuk keluaran, kode ditulis di dalam pernyataan `<%= %>`.

## Contoh RHTML

Contoh berikut menggunakan kombinasi HTML dan Ruby on Rails yang paling sederhana untuk menampilkan nama setiap produk dari daftar produk.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referensi

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

