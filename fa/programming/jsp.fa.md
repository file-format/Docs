{
  "date": "2021-04-21",
  "keywords": [
"فایل jsp چیست",
"آموزش jsp",
"jsp یعنی",
"jsp",
"فایل های jsp",
"افزونه",
"قالب",
"آموزش jsp",
".jsp",
"jsp مثال",
"پسوند فایل jsp",
"نحوه باز کردن فایل jsp"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "JSP - فرمت فایل صفحات سرور جاوا",
  "description": "با نمونه JSP و APIهایی که می توانند فایل های JSP را ایجاد و باز کنند، درباره فرمت فایل JSP بیاموزید.",
  "linktitle": "JSP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-js-fap"
}
},
  "lastmod": "2021-05-07"
}

## فایل JSP چیست؟
فایل‌های JSP به‌عنوان صفحاتی پویا و مبتنی بر داده برای برنامه‌های کاربردی وب جاوا شما شناخته می‌شوند. JSP به معنای صفحات سرور جاوا است. می تواند به عنوان یک افزونه برای Servlet در نظر گرفته شود زیرا عملکردهای بیشتری را نسبت به Servlet مانند زبان بیان ممکن می کند. JSP و Servlet کار یکسانی را با هم در برنامه های وب قدیمی جاوا انجام می دهند. از منظر برنامه نویسی، واضح ترین تفاوت بین آنها این است که با servlet ها برنامه جاوا را می نویسید و سپس نشانه گذاری استاتیک (مانند HTML) را در آن کد قرار می دهید، در حالی که JSP با اسکریپت سمت مشتری یا نشانه گذاری شروع می شود، سپس تگ های JSP را در آن جاسازی می کنید. صفحه خود را به باطن جاوا متصل کنید.

## فرمت فایل JSP
یک فایل ذخیره شده با **پسوند فایل jsp** شامل بخش های زیر به ترتیب لیست شده است:

1. باز کردن نظرات
2. دستورالعمل(های) صفحه JSP
3. دستورالعمل(های) کتابخانه تگ اختیاری
4. اعلامیه(های) JSP اختیاری
5. کد HTML و JSP

### باز کردن نظرات
یک فایل JSP یا فایل قطعه با یک نظر سبک سمت سرور شروع می شود:

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

### دستورالعمل(های) صفحه JSP
یک دستورالعمل صفحه JSP ویژگی های مرتبط با صفحه JSPF را در زمان ترجمه تعریف می کند. مشخصات JSP محدودیتی برای تعداد دستورات صفحه JSP در یک صفحه ایجاد نمی کند. مثال زیر را ببینید:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
اگر یک دستورالعمل صفحه از عرض معمولی یک صفحه JSP بیشتر شود، دستورالعمل به چندین خط تقسیم می شود:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### دستورالعمل(های) کتابخانه برچسب اختیاری
در صفحه JSP، یک دستورالعمل کتابخانه برچسب، کتابخانه های برچسب سفارشی را اعلام می کند. یک دستورالعمل کوتاه را می توان در یک خط اعلام کرد. دستورالعمل های کتابخانه برچسب های متعدد در یک مکان در بدنه صفحه JSP با هم چیده می شوند:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### اعلامیه(های) JSP اختیاری

متدها و متغیرهای اعلام شده در یک فایل JSPF باید در اعلان های JSP وجود داشته باشند. این متدها و متغیرها مشابه اعلان‌های زبان برنامه‌نویسی جاوا هستند و به همین دلیل باید از قوانین کد مربوطه پیروی کرد. اعلان ها معمولاً در یک < % نوشته می شوند! ... %> بلوک اعلان JSP، برای متمرکز کردن اعلان ها در یک ناحیه از بدنه صفحه JSP. به نمونه های زیر نگاه کنید:

#### بلوک های اعلامی متفاوت:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### بلوک اعلان ترجیحی:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
کد ### HTML و JSP
این بخش از یک صفحه JSP، بدنه HTML صفحه JSP و کد JSPF، مانند عبارات JSP، اسکریپت‌ها و دستورالعمل‌های JavaBeans را نگه می‌دارد.

## چرخه حیات یک صفحه JSP

جریان صفحه JSP مبتنی بر فاز در اینجا آورده شده است:

- ترجمه JSP Page
- گردآوری صفحه JSP
- Classloading (Classloader فایل کلاس را بارگیری می کند)
- Instantiation (Object of Generated Servlet ایجاد می شود).
- مقداردهی اولیه ( کانتینر متد jspInit() را فراخوانی می کند.
- پردازش درخواست (کانتینر روش \_jspService() را فراخوانی می کند.
- Destroy ( کانتینر متد jspDestroy() را فراخوانی می کند.

{{< figure src="../jsp.jpg" alt="فرمت فایل JSP" >}}

## مثال JSP

یادگیری در مورد فن آوری های JSP امروزه بسیار آسان است زیرا بسیاری از آموزش های JSP از طریق اینترنت در دسترس هستند. مثال زیر JSP برای پردازش سفارش با به روز رسانی رکوردهای مناسب در پایگاه داده است.
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
## منابع

 * [کنوانسیون های کد برای صفحات جاوا سرور](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [آموزش JSP] (https://www.javatpoint.com/jsp-tutorial)

