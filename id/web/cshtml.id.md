{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml", "file cshtml", "format file cshtml", "tipe file cshtml", "file", "ketik", "apa itu file cshtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - Halaman Web Razor ASP.NET",
  "description":"Pelajari tentang format file CSHTML dan API yang dapat membuat dan membuka file CSHTML.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## Apa itu file CSHTML?

File dengan ekstensi .cshtml adalah file HTML [C#](/id/programming/cs/) yang digunakan di sisi server oleh mesin Razor Markup untuk merender file halaman web ke browser pengguna. Pengkodean sisi server ini mirip dengan halaman ASP.NET standar yang memungkinkan pembuatan konten web dinamis dengan cepat saat halaman web ditulis ke browser. Server mengeksekusi kode sisi server di dalam halaman sebelum mengirimkan halaman yang dihasilkan ke browser. Tugas kompleks seperti mengakses database dan merender tampilan kompleks. File CSHTML dapat dibuat dan diprogram menggunakan Microsoft Visual Studio.

## Format File CSHTML

File CSHTML adalah file teks yang mengikuti sintaks yang digariskan oleh mesin markup Razor. Razor mendukung C# dan VB.NET, dan mudah dipelajari dan digunakan daripada ASP dan ASP.NET klasik. w3schools memiliki panduan sederhana namun efektif untuk [sintaks C# dan VB.NET](https://www.w3schools.com/asp/razor_syntax.asp) pengkodean Razor.

### Contoh CSHTML

Berikut adalah contoh Kode C# yang digunakan dalam file CSHTML untuk Razor.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Kode VB.NET yang setara untuk Razor adalah sebagai berikut.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## Referensi

* [Referensi Sintaks Razor - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

