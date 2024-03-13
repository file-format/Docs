{
  "date": "2021-04-21",
  "keywords": [
"jsp faylı nədir",
"jsp üzrə dərslər",
"jsp deməkdir",
"jsp",
"jsp faylları",
"uzadılması",
"format",
"jsp dərsliyi",
".jsp",
"jsp nümunəsi",
"jsp fayl uzantısı",
"jsp faylını necə açmaq olar"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP - Java Server Səhifələri Fayl Formatı",
  "description": "JSP faylları yarada və aça bilən JSP nümunəsi və API ilə JSP fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-azp"
}
},
  "lastmod": "2021-05-07"
}

## JSP faylı nədir?
JSP faylları Java veb proqramlarınız üçün dinamik, verilənlərə əsaslanan səhifələr kimi həyata keçirilir. JSP Java Server Səhifələri deməkdir; Servlet-in genişləndirilməsi kimi həyata keçirilə bilər, çünki ifadə dili kimi servletdən daha çox funksionallıq təmin edir. JSP və Servlet köhnə Java veb proqramlarında eyni işi görür. Proqramlaşdırma nöqteyi-nəzərindən onların arasında ən aydın fərq ondan ibarətdir ki, servletlərlə siz Java proqramını yazırsınız və sonra həmin koda statik işarələmə (HTML kimi) yerləşdirirsiniz, halbuki JSP müştəri tərəfi skripti və ya işarələmə ilə başlayır, sonra JSP teqlərini daxil edirsiniz. səhifənizi Java backendinə qoşun.

## JSP fayl formatı
**jsp fayl uzantısı** ilə yadda saxlanılan faylda sadalanan ardıcıllıqla aşağıdakı bölmələr var:

1. Şərhlərin açılması
2. JSP səhifə direktiv(ləri)
3. Könüllü etiket kitabxanası direktiv(lər)i
4. Könüllü JSP bəyannaməsi(lər)i
5. HTML və JSP kodu

### Şərhlərin açılışı
JSP faylı və ya fraqment faylı server tərəfi stil şərhi ilə başlayır:

```
<%--
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description:
  --%>
```
Above comment is appeared only on the server side because it is removed while rendering the page in browser. The comment may contain the information about the author(s), the date, and the copyright notice of the revision, an identifier and a description about the JSP page for developers. Combining the characters " @(#)" is recognized by certain programs as indicating the start of an identifier.

### JSP Səhifə Direktiv(ləri)
JSP səhifə direktivi tərcümə zamanı JSPF səhifəsi ilə əlaqəli atributları müəyyən edir. JSP spesifikasiyası bir səhifədə neçə JSP səhifə direktivinin yazıla biləcəyinə məhdudiyyət qoymur. Aşağıdakı nümunəyə baxın:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Əgər səhifə direktivi JSP səhifəsinin normal genişliyini aşırsa, direktiv bir neçə sətirə bölünür:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### Könüllü Etiket Kitabxanası Direktiv(lər)i
JSP səhifəsində etiket kitabxanası direktivi xüsusi etiket kitabxanalarını elan edir. Qısa direktiv bir sətirdə elan edilə bilər. Çoxsaylı etiket kitabxanası direktivləri JSP səhifəsinin gövdəsində eyni yerdə yığılmışdır:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Əlavə JSP bəyannaməsi(lər)i

JSPF faylında elan edilən metodlar və dəyişənlər JSP bəyannamələrində mövcud olmalıdır. Bu üsullar və dəyişənlər Java proqramlaşdırma dilindəki bəyannamələrə bənzəyir və buna görə də müvafiq kod konvensiyalarına əməl edilməlidir. Bəyanatlar adətən tək < % ilə yazılır! ... %> JSP bəyannamə bloku, bəyannamələri JSP səhifəsinin gövdəsinin bir sahəsi daxilində mərkəzləşdirmək üçün. aşağıdakı nümunələrə baxın:

#### Fərqli bəyannamə blokları:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Üstünlük verilən bəyannamə bloku:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML və JSP kodu
JSP səhifəsinin bu bölməsində JSP səhifəsinin HTML gövdəsi və JSPF kodu, məsələn, JSP ifadələri, skriptlər və JavaBeans təlimatları var.

## JSP səhifəsinin həyat dövrü

Faza baxımından JSP səhifə axını burada verilmişdir:

- JSP səhifəsinin tərcüməsi
- JSP Səhifəsinin tərtibi
- Classloading (sinif yükləyicisi sinif faylını yükləyir)
- Instantiation (Yaradılmış Servletin Obyekti yaradılır).
- Başlama (konteyner jspInit() metodunu işə salır).
- Sorğunun işlənməsi (konteyner \_jspService() metodunu işə salır).
- Destroy (konteyner jspDestroy() metodunu işə salır).

{{< figure src="../jsp.jpg" alt="JSP fayl formatı" >}}

## JSP nümunəsi

JSP texnologiyalarını öyrənmək indi çox asandır, çünki internet üzərindən çoxlu JSP dərslikləri mövcuddur. Aşağıdakı JSP nümunəsi verilənlər bazasındakı müvafiq qeydləri yeniləməklə sifarişin işlənməsi üçündür.
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
## İstinadlar

 * [JavaServer Səhifələri üçün Kod Konvensiyaları](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

