{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "file stml", "format file stml", "jenis file stml", "file", "ketik", "apa itu file stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Berkas HTML SSI",
  "description":"Pelajari tentang format file STML dan API yang dapat membuat dan membuka file STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## Apa itu berkas STML?

File dengan ekstensi .stml adalah halaman web dengan instruksi sisi server yang dijalankan saat pengguna memuat halaman di browser web. Halaman STML berisi kode sisi server yang berisi sisi server termasuk untuk melakukan tugas-tugas yang tidak mungkin dicapai dengan HTML biasa. Meskipun mirip dengan [HTML](/id/web/html/), STML menawarkan kekuatan lebih dengan menjalankan perintah di server, juga disebut Server Side Included (SSI). Dengan diperkenalkannya bahasa pemrograman baru dengan skrip sisi server seperti PHP, penggunaan STML berkurang meskipun masih didukung oleh semua teknologi sisi server. File STML dapat dibuka di editor teks apa pun dan diedit untuk memperbarui perintah.

## Format File STML

STML didasarkan pada format file teks ascii biasa yang dapat dibaca manusia. Namun, ini mengikuti sintaks seperti yang ditentukan dan dijalankan menggunakan [perintah SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) yang dijalankan di sisi server. Seperti bahasa skrip sisi server lainnya, STML dapat menggunakan perintah sisi server untuk melakukan tugas seperti penghitung pengunjung halaman, kalender halaman web, mengambil catatan dari database, dan sejenisnya.

## Contoh STML

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

