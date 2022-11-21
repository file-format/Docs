{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","ไฟล์ shtml", "รูปแบบไฟล์ shtml", "ประเภทไฟล์ shtml", "ไฟล์", "ประเภท", "ไฟล์ shtml คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - ฝั่งเซิร์ฟเวอร์รวมไฟล์ HTML",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ SHTML และ API ที่สามารถสร้างและเปิดไฟล์ SHTML",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## ไฟล์ SHTML คืออะไร?

ไฟล์ที่มีนามสกุล .shtml คือหน้าเว็บที่เขียนด้วย [HTML](/th/web/html/) และมีคำแนะนำเกี่ยวกับเซิร์ฟเวอร์ นอกจากนี้ยังอาจมีการรวมฝั่งเซิร์ฟเวอร์ที่คล้ายกับไฟล์ ASP เพื่อการโหลดที่เร็วขึ้น ไฟล์ฝั่งเซิร์ฟเวอร์ยังสามารถมีรหัสปฏิบัติการที่สามารถทำให้เซิร์ฟเวอร์โหลดช้ากว่าปกติ ไฟล์ SHTML คล้ายกับ HTML แต่ยังอนุญาตให้ใช้คำสั่งเซิร์ฟเวอร์อย่างง่าย คำสั่งเซิร์ฟเวอร์เหล่านี้ดำเนินการในภาษาการเขียนโปรแกรมคอมพิวเตอร์อย่างง่ายที่เรียกว่า Server Side รวม (SSI) SHTML ถูกแทนที่โดยภาษาโปรแกรมฝั่งเซิร์ฟเวอร์อื่นๆ เช่น [PHP](/th/programming/php/)

## รูปแบบไฟล์ SHTML

ไฟล์ SHTML เขียนด้วยข้อความล้วนและใช้ [คำสั่ง SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) ที่ดำเนินการทางฝั่งเซิร์ฟเวอร์ คำสั่งฝั่งเซิร์ฟเวอร์เหล่านี้สามารถใช้เพื่อเชื่อมต่อกับฐานข้อมูลโดยใช้ไดรเวอร์ฐานข้อมูลและดึงข้อมูลผู้ใช้จากตาราง

## ตัวอย่าง SHTML

คำแนะนำฝั่งเซิร์ฟเวอร์ใช้ในแอปพลิเคชัน เช่น สำหรับตัวนับผู้เข้าชมเพจหรือปฏิทินหน้าเว็บ ตัวอย่างต่อไปนี้ แสดงสี่คอลัมน์แรกของสามบรรทัดแรกของฐานข้อมูลผู้ใช้

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
## อ้างอิง

* [รวมฝั่งเซิร์ฟเวอร์](https://en.wikipedia.org/wiki/Server_Side_Includes)

