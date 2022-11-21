{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "ekstensi", "file", "format", "sistem", "Bahasa Markup Cold Fusion", "bahasa", "halaman web CFM", "mesin CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Markup Cold Fusion",
  "description":"Pelajari tentang format file CFM dan API yang dapat membuat dan membuka file CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Apa itu file CFM? ##

Halaman web dan file yang digunakan dalam **Cold Fusion Markup Language** berisi ekstensi CFM dan diberi nama halaman web CFM. Bahasa skrip pengembangan web ini berjalan di Google App Engine, .NET framework, dan JVM. Ini dapat berisi bahasa pemrograman atau kode bahasa. Ketika salah satu halamannya diakses oleh pengguna, server web ColdFusion mengeksekusinya. CFScript (yang mirip dengan JavaScript) atau tag dapat digunakan untuk menulis CFML. CFML dapat digunakan untuk membuat bahasa lain selain [HTML](/id/web/html/) seperti [CSS](/id/web/css/), [JavaScript](/id/web/js/), [XML](/id/web/ xml/), dan lainnya.

Penggunaan bahasa dan tag yang didukungnya sebagian besar dalam pengembangan aplikasi web dinamis. File dapat langsung dijalankan di browser online jika terjadi kesalahan selama penggunaan offline platform pengembangan aplikasi.
 

CFML bekerja dengan cara ekstensi file server tertentu (.cfc, .cfm) diberikan untuk diproses ke mesin CFML. Jika mesin berbasis Java, itu dicapai dengan menggunakan servlet Java. Mesin CFML hanya memproses fungsi dan tag dan mengembalikan fungsi dan teks di luar tag CFML ke server web tanpa perubahan apa pun.


## Sejarah Singkat ##

Pada tahun 1995, pertama kali dibuat oleh sebuah perusahaan bernama Allaire. Pada tahun 2005 Adobe memperolehnya dan menyediakan layanan untuk mengembangkan ColdFusion sampai sekarang. Selama bertahun-tahun, itu dikembangkan dan ditingkatkan oleh banyak orang dan perusahaan. Pada 2012, sebuah yayasan bernama OpenCFML diluncurkan. Kemudian, pada tahun 2015 mantan Railo memberikan jasanya untuk meningkatkan kinerja CFM dan mengurangi sumber daya untuk fungsionalitas yang lebih baik. Pembaruan terbaru diluncurkan pada tahun 2020 yang diumumkan akan dilanjutkan hingga 2028.

## Format File CFM ##

Kode file CFM dan halaman web sebagian besar terdiri dari tag seperti HTML tetapi dengan sedikit perbedaan. File-file ini bertanggung jawab untuk melakukan berbagai operasi yang dapat dijalankan oleh skrip ColdFusion.
* File-file ini dapat diakses dan dijalankan langsung di Windows dan macOS menggunakan browser sistem operasi apa pun.
* Adobe ColdFusion menyediakan platform untuk pengembangan halaman web dan aplikasi dinamis di PC.
* Setiap editor teks seperti NotePad atau editor teks lainnya dalam sistem operasi dapat digunakan untuk membuka file ini karena file ini berbasis teks.
* Ketika file CFM apa pun dibuka di editor teks, itu menampilkan kode yang terdiri dari tag dan skrip yang tidak akan dipahami kecuali dia adalah pengembang web.

## Contoh Penggunaan CFM ##

Berikut ini adalah contoh penggunaan sederhana file CFM.

### Dokumen CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Referensi ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

