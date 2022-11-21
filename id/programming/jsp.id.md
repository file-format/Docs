{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Format File Halaman Server Java",
  "description":"Pelajari tentang format file JSP dengan contoh JSP dan API yang dapat membuat dan membuka file JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Apa itu file JSP?
File JSP direalisasikan sebagai halaman dinamis berbasis data untuk aplikasi web Java Anda. JSP berarti Halaman Server Java; dapat direalisasikan sebagai ekstensi ke Servlet karena memungkinkan fungsionalitas lebih dari servlet seperti bahasa ekspresi. JSP dan Servlet melakukan pekerjaan yang sama bersama-sama di aplikasi web Java yang lebih lama. Dari perspektif pemrograman, perbedaan paling jelas di antara mereka adalah bahwa dengan servlet Anda menulis program Java dan kemudian menyematkan markup statis (seperti HTML) ke dalam kode itu, sedangkan, JSP dimulai dengan skrip atau markup sisi klien, lalu menyematkan tag JSP ke menghubungkan halaman Anda ke backend Java.

## Format File JSP
File yang disimpan dengan **ekstensi file jsp** berisi bagian berikut sesuai urutannya:

1. Membuka komentar
2. Arahan halaman JSP
3. Direktif pustaka tag opsional
4. Deklarasi JSP opsional
5. Kode HTML dan JSP

### Komentar Pembuka
File JSP atau file fragmen dimulai dengan komentar gaya sisi server:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Komentar di atas hanya muncul di sisi server karena dihapus saat merender halaman di browser. Komentar dapat berisi informasi tentang penulis, tanggal, dan pemberitahuan hak cipta dari revisi, pengidentifikasi dan deskripsi tentang halaman JSP untuk pengembang. Menggabungkan karakter " @(#)" dikenali oleh program tertentu sebagai indikasi dimulainya suatu pengidentifikasi.

### Direktif Laman JSP
Arahan halaman JSP mendefinisikan atribut yang terkait dengan halaman JSPF pada waktu terjemahan. Spesifikasi JSP tidak memaksakan batasan pada berapa banyak arahan halaman JSP yang dapat ditulis dalam satu halaman. Lihat contoh berikut:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Jika direktif halaman melebihi lebar normal halaman JSP, direktif dipecah menjadi beberapa baris:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Direktif Perpustakaan Tag Opsional
Di halaman JSP, direktif pustaka tag mendeklarasikan pustaka tag khusus. Arahan singkat dapat dideklarasikan dalam satu baris. Beberapa arahan perpustakaan tag ditumpuk bersama di lokasi yang sama di dalam badan halaman JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Deklarasi JSP opsional
  


Metode dan variabel yang dideklarasikan dalam file JSPF harus ada dalam deklarasi JSP. Metode dan variabel ini serupa dengan deklarasi dalam bahasa pemrograman Java, dan karena itulah konvensi kode yang relevan harus diikuti. Deklarasi biasanya ditulis dalam satu <%! ... %> blok deklarasi JSP, untuk memusatkan deklarasi dalam satu area badan halaman JSP. lihat contoh berikut:

#### Blok deklarasi berbeda:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Blok deklarasi pilihan:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Kode HTML dan JSP
Bagian halaman JSP ini menampung badan HTML dari halaman JSP dan kode JSPF, seperti ekspresi JSP, skrip kecil, dan instruksi JavaBeans.

## Siklus Hidup Halaman JSP

Alur halaman JSP fase bijaksana diberikan di sini:

- Terjemahan Halaman JSP
- Kompilasi Halaman JSP
- Classloading (classloader memuat file kelas)
- Instansiasi (Objek Servlet yang Dihasilkan dibuat).
- Inisialisasi (wadah memanggil metode jspInit()).
- Meminta pemrosesan (wadah memanggil metode _jspService()).
- Hancurkan (wadah memanggil metode jspDestroy()).

{{< figure src="../jsp.jpg" alt="Format File JSP" >}}

## Contoh JSP

Belajar tentang teknologi JSP sekarang sangat mudah karena banyak tutorial JSP tersedia melalui internet. Contoh JSP berikut adalah untuk memproses pesanan, dengan memperbarui record yang sesuai di database.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## Referensi

* [Konvensi Kode untuk Halaman JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutorial JSP](https://www.javatpoint.com/jsp-tutorial)

