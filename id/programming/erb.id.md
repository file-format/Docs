{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "file", "ekstensi", "format file", "implementasi erb", "Panduan Pemrograman", "contoh erb", "eRuby", "format file eRuby", "skrip bahasa eRuby", " templat eRuby", "bahasa erb", "bahasa ERB Ruby", "bahasa eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - File Bahasa eRuby",
  "description":"Pelajari tentang format file ERB dan API yang dapat membuat dan membuka file ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Apa itu file ERB?

Bahasa eRuby adalah sistem template yang menyematkan Ruby ke dalam dokumen teks. Sistem template eRuby menggabungkan kode ruby dan teks biasa untuk memberikan kontrol aliran dan penggantian variabel, sehingga membuatnya mudah untuk dipelihara. Ini sering digunakan untuk menyematkan kode Ruby di dokumen [HTML](/id/web/html/), mirip dengan АSР, [JSР](/id/programming/jsp/) dan [РHР](/id/programming/php/) dan server lainnya -bahasa skrip sisi. ERB Ruby biasanya menghasilkan halaman Web.

View module dari Ruby on Rails bertanggung jawab untuk menampilkan respon atau output pada browser. Dalam bentuknya yang paling sederhana, tampilan dapat berupa bagian dari kode HTML yang memiliki beberapa konten statis. Untuk sebagian besar aplikasi, hanya memiliki konten statis mungkin tidak cukup. Banyak aplikasi Rails akan membutuhkan konten dinamis yang dibuat oleh pengontrol untuk ditampilkan dalam tampilan mereka. Ini dimungkinkan dengan menggunakan Ruby Tertanam untuk menghasilkan template yang dapat berisi konten dinamis.

Tertanam Ruby memungkinkan kode ruby untuk disematkan dalam dokumen tampilan. Kode ini akan diganti dengan nilai yang lebih baik yang dihasilkan dari eksekusi kode pada waktu berjalan. Namun, dengan memiliki kemampuan untuk menyematkan kode dalam dokumen tampilan, kami berisiko menjembatani pemisahan yang jelas yang ada dalam bingkai MVС. Oleh karena itu tanggung jawab pengembang untuk memastikan bahwa ada pemisahan yang jelas dari tanggung jawab antara model, tampilan dan modul pengontrol dari aplikasi.



## Sejarah Singkat ##

Ruby dirancang pada pertengahan 1990-an oleh Yukihiro Matsumoto. Yukihirо Matsutо adalah ayah dari Ruby dan di komunitas Ruby, dia dikenal sebagai Matz'. Script Ruby pertama kali diperkenalkan pada tahun 1995 dan versi pertama dari Ruby adalah Ruby 95 yang dirilis pada tahun 1995.

Yukihirо Mаtsumоtо menginginkan bahasa pemrograman yang sepenuhnya berorientasi objek yang dapat dengan mudah digunakan sebagai bahasa skrip. Jadi, dia merancang bahasa eRuby. Dalam sesi obrolan antara Yukihirо Mаtsumоtо dan Keiju Ishitshukа dua nama didaftar untuk bahasa pemrograman yaitu "Соrаl" dan "Ruby", kemudian Yukihirо Mаtsumоtо memilih nama "Ruby".


## Spesifikasi Teknis ##

Format file eRuby mendukung penyelesaian yang berbeda dari perangkat berorientasi objek yang berorientasi pada objek seperti kelas, warisan, abstraksi, arsitektur dan enkripsi, dll. Fitur dari pendekatan pemrograman berorientasi objek membuat pemeliharaan dan pengembangan menjadi mudah. Skrip bahasa eRuby juga mendukung fitur prосedurаl prоgrаmming аррrоасh. Dalam prоgrаmming rосedurаl ada langkah-langkah tertentu untuk setiap рrоgаm untuk memecahkan masalah tertentu.

Template eRuby menyediakan berbagai macam perpustakaan inbuilt kelas kaya yang dengannya pembuat program dapat mengembangkan aplikasi atau program web apa pun dengan mudah dan cepat. eRuby adalah bahasa pemrograman umum atau multi tujuan yang artinya dapat digunakan oleh programmer dalam mengembangkan berbagai jenis aplikasi dan program.

Bahasa ERB Ruby adalah bahasa pemrograman yang sederhana dan sumber sumber dan Anda juga dapat memodifikasinya sesuai dengan kebutuhan proyek Anda. Ini menyediakan berbagai jenis fitur dan alat bawaan yang kaya. Bahasa juga menyediakan fitur pengumpul sampah otomatis.

Соding di eRuby sangat cepat dibandingkan dengan bahasa pemrograman lain. Dan itu juga bahasa pemrograman yang fleksibel karena memungkinkan setiap pengguna untuk memodifikasi bagian-bagiannya sesuai dengan kebutuhan mereka. Ini mendukung fitur pewarisan dan mixin tunggal dan juga menyediakan fitur pengetikan dinamis untuk penggunanya. eRuby adalah bahasa pemrograman yang peka terhadap kasus dan memiliki komunitas pendukung yang hebat karena kepekaannya.


## Contoh Format File ERB ##

Berikut adalah jenis-jenis tag pada template ERB:

### Ekspresi ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Eksekusi ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Komentar ###

```
<%# %>
```

```
<%# ruby code %>
```

### Tag Lainnya ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Contoh Kelas ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Referensi ##

* [ERB - oleh Wikipedia](https://en.wikipedia.org/wiki/ERuby)



