{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" : "JSP - জাভা সার্ভার পেজ ফাইল ফরম্যাট",
  "description":"JSP উদাহরণ সহ JSP ফাইল বিন্যাস সম্পর্কে জানুন এবং JSP ফাইলগুলি তৈরি এবং খুলতে পারে এমন APIগুলি।",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## একটি JSP ফাইল কি?
JSP ফাইলগুলি আপনার জাভা ওয়েব অ্যাপ্লিকেশনগুলির জন্য গতিশীল, ডেটা-চালিত পৃষ্ঠা হিসাবে উপলব্ধি করা হয়। JSP মানে জাভা সার্ভার পেজ; সার্ভলেটের এক্সটেনশন হিসাবে উপলব্ধি করা যেতে পারে কারণ এটি সার্ভলেটের চেয়ে বেশি কার্যকারিতা সক্ষম করে যেমন অভিব্যক্তি ভাষা। JSP এবং Servlet পুরানো জাভা ওয়েব অ্যাপ্লিকেশনগুলিতে একসাথে একই কাজ করে। একটি প্রোগ্রামিং দৃষ্টিকোণ থেকে, তাদের মধ্যে সবচেয়ে স্পষ্ট পার্থক্য হল যে সার্লেটগুলির সাথে আপনি জাভা প্রোগ্রাম লেখেন এবং তারপরে স্ট্যাটিক মার্কআপ (যেমন এইচটিএমএল) সেই কোডে এম্বেড করেন, যেখানে, JSP ক্লায়েন্ট-সাইড স্ক্রিপ্ট বা মার্কআপ দিয়ে শুরু হয়, তারপরে JSP ট্যাগগুলি এম্বেড করে আপনার পৃষ্ঠাটিকে জাভা ব্যাকএন্ডের সাথে সংযুক্ত করুন।

## JSP ফাইল ফরম্যাট
**jsp ফাইল এক্সটেনশন** এর সাথে সংরক্ষিত একটি ফাইলের তালিকায় নিম্নলিখিত বিভাগগুলি রয়েছে:

1. খোলা মন্তব্য
2. JSP পৃষ্ঠা নির্দেশিকা(গুলি)
3. ঐচ্ছিক ট্যাগ লাইব্রেরি নির্দেশিকা(গুলি)
4. ঐচ্ছিক JSP ঘোষণা(গুলি)
5. HTML এবং JSP কোড

### খোলার মন্তব্য
একটি JSP ফাইল বা ফ্র্যাগমেন্ট ফাইল একটি সার্ভার সাইড স্টাইল মন্তব্য দিয়ে শুরু হয়:

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

### JSP পৃষ্ঠা নির্দেশিকা(গুলি)
একটি JSP পৃষ্ঠা নির্দেশিকা অনুবাদের সময় JSPF পৃষ্ঠার সাথে সম্পর্কিত বৈশিষ্ট্যগুলিকে সংজ্ঞায়িত করে। JSP স্পেসিফিকেশন একক পৃষ্ঠায় কতগুলি JSP পৃষ্ঠা নির্দেশিকা লিখতে পারে তার উপর কোন সীমাবদ্ধতা আরোপ করে না। নিম্নলিখিত উদাহরণ দেখুন:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
যদি একটি পৃষ্ঠা নির্দেশিকা, একটি JSP পৃষ্ঠার স্বাভাবিক প্রস্থকে অতিক্রম করে, নির্দেশিকাটি কয়েকটি লাইনে বিভক্ত হয়:

```
<%@ page    session="false"
            import="java.util.*"
            errorPage="/common/errorPage.jsp"
%>
```
### ঐচ্ছিক ট্যাগ লাইব্রেরি নির্দেশিকা(গুলি)
JSP পৃষ্ঠায়, একটি ট্যাগ লাইব্রেরি নির্দেশিকা কাস্টম ট্যাগ লাইব্রেরি ঘোষণা করে। একটি সংক্ষিপ্ত নির্দেশ একটি একক লাইনে ঘোষণা করা যেতে পারে। একাধিক ট্যাগ লাইব্রেরি নির্দেশিকা JSP পৃষ্ঠার মূল অংশের মধ্যে একই অবস্থানে একসাথে স্ট্যাক করা হয়:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### ঐচ্ছিক JSP ঘোষণা(গুলি)

একটি JSPF ফাইলে ঘোষিত পদ্ধতি এবং ভেরিয়েবলগুলি JSP ঘোষণায় বিদ্যমান থাকা উচিত। এই পদ্ধতি এবং ভেরিয়েবলগুলি জাভা প্রোগ্রামিং ভাষার ঘোষণার মতোই, এবং সেই কারণেই প্রাসঙ্গিক কোড কনভেনশনগুলি অনুসরণ করা উচিত। ঘোষণা সাধারণত একক < % লেখা হয়! ... %> JSP ঘোষণা ব্লক, JSP পৃষ্ঠার মূল অংশের একটি এলাকার মধ্যে ঘোষণাকে কেন্দ্রীভূত করতে। নিম্নলিখিত উদাহরণ তাকান:

#### ভিন্ন ঘোষণা ব্লক:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### পছন্দের ঘোষণা ব্লক:
```
<%!
        private int hitCount;
        private Date today;

        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML এবং JSP কোড
একটি JSP পৃষ্ঠার এই বিভাগে JSP পৃষ্ঠার HTML বডি এবং JSPF কোড, যেমন JSP এক্সপ্রেশন, স্ক্রিপ্টলেট এবং JavaBeans নির্দেশাবলী রয়েছে।

## একটি JSP পৃষ্ঠার জীবনচক্র

ফেজ অনুযায়ী JSP পৃষ্ঠা প্রবাহ এখানে দেওয়া হয়েছে:

- JSP পৃষ্ঠার অনুবাদ
- JSP পৃষ্ঠার সংকলন
- ক্লাসলোডিং (ক্লাসলোডার ক্লাস ফাইল লোড করে)
- ইনস্ট্যান্টিয়েশন (জেনারেটেড সার্ভলেটের অবজেক্ট তৈরি করা হয়)।
- ইনিশিয়ালাইজেশন ( কন্টেইনারটি jspInit() পদ্ধতিকে আহ্বান করে)।
- অনুরোধ প্রক্রিয়াকরণ ( ধারক \_jspService() পদ্ধতির আহ্বান করে)।
- ধ্বংস করুন ( ধারকটি jspDestroy() পদ্ধতিকে আহ্বান করে)।

{{< figure src="../jsp.jpg" alt="JSP ফাইল ফরম্যাট" >}}

## JSP উদাহরণ

JSP প্রযুক্তি সম্পর্কে শেখা এখন খুব সহজ কারণ ইন্টারনেটে প্রচুর JSP টিউটোরিয়াল পাওয়া যায়। নিম্নলিখিত JSP উদাহরণটি ডাটাবেসে উপযুক্ত রেকর্ড আপডেট করে অর্ডার প্রক্রিয়াকরণের জন্য।
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
## তথ্যসূত্র

 * [জাভা সার্ভার পৃষ্ঠাগুলির জন্য কোড কনভেনশন](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP টিউটোরিয়াল](https://www.javatpoint.com/jsp-tutorial)

