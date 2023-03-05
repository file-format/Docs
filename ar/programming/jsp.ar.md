{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - تنسيق ملف صفحات خادم جافا" ,
  "description":"تعرف على تنسيق ملف JSP باستخدام مثال JSP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات JSP وفتحها." ,
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-05-07"
}

## ما هو ملف JSP؟
يتم إدراك ملفات JSP كصفحات ديناميكية تعتمد على البيانات لتطبيقات الويب Java الخاصة بك. JSP تعني صفحات خادم Java ؛ يمكن تحقيقه كملحق لـ Servlet لأنه يتيح وظائف أكثر من servlet مثل لغة التعبير. يقوم JSP و Servlet بنفس المهمة معًا في تطبيقات ويب Java القديمة. من منظور البرمجة ، يتمثل الاختلاف الأكثر وضوحًا بينهما في أنه باستخدام servlets تكتب برنامج Java ثم تقوم بتضمين ترميز ثابت (مثل HTML) في هذا الرمز ، بينما يبدأ JSP بالنص أو الترميز من جانب العميل ، ثم تضمين علامات JSP في قم بتوصيل صفحتك بخلفية Java الخلفية.

## تنسيق ملف JSP
يحتوي الملف المحفوظ بامتداد ** jsp file ** على الأقسام التالية بالترتيب المذكور:

1. افتتاحيات التعليقات
2. توجيه (تعليمات) صفحة JSP
3. توجيه (توجيهات) اختيارية لمكتبة العلامات
4. إعلان (إعلانات) JSP الاختياري
5. كود HTML و JSP

### التعليقات الافتتاحية
يبدأ ملف JSP أو ملف الجزء بتعليق على نمط جانب الخادم:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
يظهر التعليق أعلاه على جانب الخادم فقط لأنه تمت إزالته أثناء عرض الصفحة في المستعرض. قد يحتوي التعليق على معلومات حول المؤلف (المؤلفين) والتاريخ وإشعار حقوق النشر للمراجعة ومعرف ووصف حول صفحة JSP للمطورين. تتعرف برامج معينة على دمج الأحرف "@ (#)" على أنها تشير إلى بداية المعرف.

### توجيهات صفحة JSP
يحدد توجيه صفحة JSP السمات المرتبطة بصفحة JSPF في وقت الترجمة. لا تفرض مواصفات JSP قيدًا على عدد توجيهات صفحة JSP التي يمكن كتابتها في صفحة واحدة. انظر المثال التالي:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
إذا تجاوز توجيه الصفحة العرض العادي لصفحة JSP ، فسيتم تقسيم التوجيه إلى عدة أسطر:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### توجيه (توجيهات) مكتبة العلامات الاختيارية
في صفحة JSP ، يعلن توجيه مكتبة العلامات عن مكتبات علامات مخصصة. يمكن الإعلان عن توجيه قصير في سطر واحد. يتم تكديس توجيهات مكتبة العلامات المتعددة معًا في نفس الموقع داخل نص صفحة JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### إعلان (إعلانات) JSP الاختياري
  


يجب أن تكون الطرق والمتغيرات المعلنة في ملف JSPF موجودة في تعريفات JSP. تتشابه هذه الأساليب والمتغيرات مع الإعلانات في لغة برمجة Java ، ولهذا السبب يجب اتباع اصطلاحات الكود ذات الصلة. عادة ما يتم كتابة التصريحات في واحد <٪! ...٪> كتلة إعلان JSP ، لمركزية الإعلانات داخل منطقة واحدة من جسم صفحة JSP. انظر إلى الأمثلة التالية:

#### كتل التصريح المتباينة:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### كتلة الإعلان المفضلة:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### كود HTML و JSP
يحتوي هذا القسم من صفحة JSP على نص HTML لصفحة JSP وكود JSPF ، مثل تعبيرات JSP و scriptlets وتعليمات JavaBeans.

## دورة حياة صفحة JSP

يتم تقديم تدفق صفحة JSP الحكيم هنا:

- ترجمة صفحة JSP
- تجميع صفحة JSP
- Classloading (أداة تحميل الفصل تقوم بتحميل ملف الفصل)
- مثيل (يتم إنشاء كائن من Servlet المُنشأ).
- التهيئة (الحاوية تستدعي طريقة jspInit ()).
- معالجة الطلب (الحاوية تستدعي طريقة _jspService ()).
- إتلاف (الحاوية تستدعي طريقة jspDestroy ()).

{{< figure src="../jsp.jpg" alt="تنسيق ملف JSP" >}}

## مثال JSP

يعد التعرف على تقنيات JSP أمرًا سهلاً للغاية الآن بعد أيام لأن الكثير من دروس JSP متوفرة عبر الإنترنت. مثال JSP التالي هو لمعالجة الطلب ، عن طريق تحديث السجلات المناسبة في قاعدة البيانات.
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


 


## مراجع

* [اصطلاحات التعليمات البرمجية لصفحات JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)

