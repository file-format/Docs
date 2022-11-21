{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java Sunucu Sayfaları Dosya Biçimi",
  "description":"JSP örneği ve JSP dosyaları oluşturabilen ve açabilen API'ler ile JSP dosya formatı hakkında bilgi edinin.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## JSP dosyası nedir?
JSP dosyaları, Java web uygulamalarınız için dinamik, veri odaklı sayfalar olarak gerçekleştirilir. JSP, Java Sunucu Sayfaları anlamına gelir; ifade dili gibi servlet'ten daha fazla işlevsellik sağladığı için Servlet'in bir uzantısı olarak gerçekleştirilebilir. JSP ve Servlet, eski Java web uygulamalarında aynı işi birlikte yapar. Programlama açısından bakıldığında, aralarındaki en açık fark, servlet'lerde Java programı yazıp ardından statik işaretlemeyi (HTML gibi) bu koda gömmenizdir, oysa JSP, istemci tarafı komut dosyası veya işaretlemeyle başlar, ardından JSP etiketlerini gömer. sayfanızı Java arka ucuna bağlayın.

## JSP Dosya Biçimi
**jsp dosya uzantısı** ile kaydedilen bir dosya, listelendikleri sırayla aşağıdaki bölümleri içerir:

1. Yorumları açma
2. JSP sayfası direktif(ler)i
3. İsteğe bağlı etiket kitaplığı direktif(ler)i
4. İsteğe bağlı JSP bildirim(ler)i
5. HTML ve JSP kodu

### Açılış Yorumları
Bir JSP dosyası veya parça dosyası, sunucu tarafı stil yorumuyla başlar:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Yukarıdaki yorum, sayfayı tarayıcıda işlerken kaldırıldığı için yalnızca sunucu tarafında görünür. Yorum, yazar(lar) hakkında bilgi, revizyonun tarihi ve telif hakkı bildirimi, bir tanımlayıcı ve geliştiriciler için JSP sayfası hakkında bir açıklama içerebilir. " @(#)" karakterlerinin birleştirilmesi, belirli programlar tarafından bir tanımlayıcının başlangıcını belirtmek olarak tanınır.

### JSP Sayfa Yönergeleri
Bir JSP sayfa yönergesi, çeviri zamanında JSPF sayfasıyla ilişkili öznitelikleri tanımlar. JSP belirtimi, tek bir sayfada kaç tane JSP sayfa yönergesinin yazılabileceği konusunda bir kısıtlama getirmez. Aşağıdaki örneğe bakın:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Bir sayfa yönergesi, bir JSP sayfasının normal genişliğini aşarsa, yönerge birkaç satıra bölünür:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### İsteğe Bağlı Etiket Kitaplığı Yönergeleri
JSP sayfasında, bir etiket kitaplığı yönergesi, özel etiket kitaplıklarını bildirir. Kısa bir yönerge tek bir satırda bildirilebilir. Birden çok etiket kitaplığı yönergesi, JSP sayfasının gövdesi içinde aynı konumda bir arada istiflenir:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### İsteğe bağlı JSP bildirim(ler)i
  


Bir JSPF dosyasında bildirilen yöntemler ve değişkenler, JSP bildirimlerinde bulunmalıdır. Bu yöntemler ve değişkenler, Java programlama dilindeki bildirimlere benzer ve bu nedenle ilgili kod kurallarına uyulmalıdır. Beyannameler genellikle tek bir < %! ... %> JSP bildirim bloğu, bildirimleri JSP sayfasının gövdesinin bir alanı içinde merkezileştirmek için. aşağıdaki örneklere bakın:

#### Farklı bildirim blokları:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Tercih edilen bildirim bloğu:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML ve JSP Kodu
Bir JSP sayfasının bu bölümü, JSP sayfasının HTML gövdesini ve JSPF kodunu, bu tür JSP ifadelerini, komut dosyalarını ve JavaBeans yönergelerini tutar.

## Bir JSP Sayfasının Yaşam Döngüsü

Aşamalı JSP sayfa akışı burada verilmiştir:

- JSP Sayfasının Çevirisi
- JSP Sayfasının Derlenmesi
- Sınıf yükleme (sınıf yükleyici, sınıf dosyasını yükler)
- Örnekleme (Oluşturulan Servlet'in Nesnesi oluşturulur).
- Başlatma (kap, jspInit() yöntemini çağırır).
- İstek işleme (kapsayıcı, _jspService() yöntemini çağırır).
- Yok Et (kap, jspDestroy() yöntemini çağırır).

{{< figure src="../jsp.jpg" alt="JSP Dosya Biçimi" >}}

## JSP Örneği

JSP teknolojileri hakkında bilgi edinmek artık günümüzde çok kolay çünkü internet üzerinden birçok JSP öğreticisi mevcut. Aşağıdaki JSP örneği, veritabanındaki uygun kayıtları güncelleyerek siparişi işlemek içindir.
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


 


## Referanslar

* [Java Sunucu Sayfaları için Kod Kuralları](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP Eğitimi](https://www.javatpoint.com/jsp-tutorial)

