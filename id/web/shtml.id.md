{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "file shtml", "format file shtml", "tipe file shtml", "file", "ketik", "apa itu file shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Sisi Server Sertakan File HTML",
  "description":"Pelajari tentang format file SHTML dan API yang dapat membuat dan membuka file SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Apa itu file SHTML?

File dengan ekstensi .shtml adalah halaman web yang ditulis dalam [HTML](/id/web/html/) dan menyertakan instruksi server. Ini mungkin juga berisi sisi server yang mirip dengan file ASP untuk memuat lebih cepat. File sisi server juga dapat berisi kode yang dapat dieksekusi yang dapat membuat server memuat lebih lambat dari biasanya. File SHTML mirip dengan HTML tetapi juga memungkinkan penggunaan perintah server sederhana. Perintah server ini dilakukan dalam bahasa pemrograman komputer sederhana yang disebut Server Side Included (SSI). SHTML sebagian besar telah digantikan oleh bahasa pemrograman sisi server lainnya seperti [PHP](/id/programming/php/).

## Format Berkas SHTML

File SHTML ditulis dalam teks biasa dan menggunakan [perintah SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) yang dijalankan di sisi server. Perintah sisi server ini bahkan dapat digunakan untuk terhubung ke database menggunakan driver database dan mengambil data pengguna dari tabel.

## Contoh SHTML

Instruksi sisi server digunakan dalam aplikasi seperti untuk penghitung pengunjung halaman atau kalender halaman web. Contoh berikut, menampilkan empat kolom pertama dari tiga baris pertama database pengguna.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Referensi

* [Sisi Server Termasuk](https://en.wikipedia.org/wiki/Server_Side_Includes)

