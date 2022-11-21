{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - รูปแบบไฟล์ Java Server Pages",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ JSP พร้อมตัวอย่าง JSP และ API ที่สามารถสร้างและเปิดไฟล์ JSP",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## ไฟล์ JSP คืออะไร??
ไฟล์ JSP ถูกรับรู้เป็นไดนามิกเพจที่ขับเคลื่อนด้วยข้อมูลสำหรับเว็บแอปพลิเคชัน Java ของคุณ JSP หมายถึง Java Server Pages; สามารถรับรู้ได้ว่าเป็นส่วนขยายของ Servlet เนื่องจากเปิดใช้งานฟังก์ชันการทำงานมากกว่าเซิร์ฟเล็ต เช่น ภาษานิพจน์ JSP และ Servlet ทำงานเดียวกันร่วมกันในเว็บแอปพลิเคชัน Java รุ่นเก่า จากมุมมองของการเขียนโปรแกรม ความแตกต่างที่ชัดเจนที่สุดระหว่างสองสิ่งนี้คือด้วยเซิร์ฟเล็ต คุณเขียนโปรแกรม Java แล้วฝังสแตติกมาร์กอัป (เช่น HTML) ลงในโค้ดนั้น ในขณะที่ JSP เริ่มต้นด้วยสคริปต์หรือมาร์กอัปฝั่งไคลเอ็นต์ จากนั้นฝังแท็ก JSP เชื่อมต่อหน้าของคุณกับแบ็กเอนด์ Java

## รูปแบบไฟล์ JSP
ไฟล์ที่บันทึกด้วย **นามสกุลไฟล์ jsp** มีส่วนต่อไปนี้ตามลำดับที่แสดง:

1. เปิดความคิดเห็น
2. คำสั่งหน้า JSP
3. คำสั่งไลบรารีแท็กเพิ่มเติม
4. การประกาศ JSP ที่เป็นทางเลือก
5. รหัส HTML และ JSP

### เปิดความคิดเห็น
ไฟล์ JSP หรือไฟล์แฟรกเมนต์เริ่มต้นด้วยความคิดเห็นเกี่ยวกับสไตล์ฝั่งเซิร์ฟเวอร์:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
ความคิดเห็นด้านบนปรากฏเฉพาะในฝั่งเซิร์ฟเวอร์เนื่องจากถูกลบออกขณะแสดงผลหน้าในเบราว์เซอร์ ความคิดเห็นอาจมีข้อมูลเกี่ยวกับผู้เขียน วันที่ และประกาศเกี่ยวกับลิขสิทธิ์ของการแก้ไข ตัวระบุและคำอธิบายเกี่ยวกับหน้า JSP สำหรับนักพัฒนา การรวมอักขระ " @(#)" ได้รับการยอมรับโดยบางโปรแกรมว่าเป็นการระบุการเริ่มต้นของตัวระบุ

### คำสั่งหน้า JSP
คำสั่งเพจ JSP กำหนดแอตทริบิวต์ที่เกี่ยวข้องกับเพจ JSPF ณ เวลาแปล ข้อมูลจำเพาะของ JSP ไม่ได้กำหนดข้อจำกัดว่าสามารถเขียนไดเร็กทีฟหน้า JSP ได้กี่หน้าในหน้าเดียว ดูตัวอย่างต่อไปนี้:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
หากไดเร็กทีฟของเพจเกินความกว้างปกติของเพจ JSP ไดเร็กทีฟจะแบ่งออกเป็นหลายบรรทัด:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### คำสั่งคลังแท็กทางเลือก
ในหน้า JSP คำสั่งไลบรารีแท็กจะประกาศไลบรารีแท็กที่กำหนดเอง สามารถประกาศคำสั่งสั้น ๆ ในบรรทัดเดียว คำสั่งไลบรารีแท็กหลายชุดซ้อนกันในตำแหน่งเดียวกันภายในเนื้อหาของหน้า JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### การประกาศ JSP ที่เป็นทางเลือก
  


เมธอดและตัวแปรที่ประกาศในไฟล์ JSPF ควรมีอยู่ในการประกาศ JSP เมธอดและตัวแปรเหล่านี้คล้ายกับการประกาศในภาษาโปรแกรม Java และนั่นคือเหตุผลที่ควรปฏิบัติตามข้อตกลงรหัสที่เกี่ยวข้อง การประกาศมักจะเขียนด้วย < %! ... %> บล็อกการประกาศ JSP เพื่อรวมศูนย์การประกาศไว้ภายในพื้นที่หนึ่งของเนื้อหาของเพจ JSP ดูตัวอย่างต่อไปนี้:

#### บล็อกการประกาศที่แตกต่างกัน:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### บล็อกการประกาศที่ต้องการ:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### รหัส HTML และ JSP
ส่วนนี้ของหน้า JSP จะเก็บเนื้อหา HTML ของหน้า JSP และโค้ด JSPF เช่น นิพจน์ JSP, scriptlets และคำสั่ง JavaBeans

## วงจรชีวิตของหน้า JSP

โฟลว์เพจ JSP ที่ชาญฉลาดของเฟสมีให้ที่นี่:

- แปลหน้า JSP
- การรวบรวมหน้า JSP
- Classloading (ตัวโหลดคลาสโหลดไฟล์คลาส)
- การสร้างอินสแตนซ์ (สร้างวัตถุของ Servlet ที่สร้างขึ้น)
- การเริ่มต้น (คอนเทนเนอร์เรียกใช้เมธอด jspInit())
- การประมวลผลคำขอ (คอนเทนเนอร์เรียกใช้เมธอด _jspService())
- ทำลาย (คอนเทนเนอร์เรียกใช้เมธอด jspDestroy())

{{< figure src="../jsp.jpg" alt="รูปแบบไฟล์ JSP" >}}

## ตัวอย่าง JSP

ทุกวันนี้การเรียนรู้เกี่ยวกับเทคโนโลยี JSP นั้นง่ายมาก เพราะมีแบบฝึกหัด JSP มากมายทางอินเทอร์เน็ต ตัวอย่าง JSP ต่อไปนี้ใช้สำหรับการประมวลผลคำสั่งซื้อ โดยอัพเดตเรกคอร์ดที่เหมาะสมในฐานข้อมูล
```
<html>
<head>
  <title>Order Book</title>,
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


 


## อ้างอิง

* [ข้อตกลงรหัสสำหรับหน้า JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [การสอน JSP](https://www.javatpoint.com/jsp-tutorial)

