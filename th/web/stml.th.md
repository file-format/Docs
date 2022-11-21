{
  "date" : "2021-05-20",
  "keywords" :[ "stml","ไฟล์ stml", "รูปแบบไฟล์ stml", "ประเภทไฟล์ stml", "ไฟล์", "ประเภท", "ไฟล์ stml คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - ไฟล์ HTML SSI",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ STML และ API ที่สามารถสร้างและเปิดไฟล์ STML",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## ไฟล์ STML คืออะไร??

ไฟล์ที่มีนามสกุล .stml คือเว็บเพจที่มีคำสั่งฝั่งเซิร์ฟเวอร์ที่จะดำเนินการเมื่อผู้ใช้โหลดเพจในเว็บเบราว์เซอร์ หน้า STML มีโค้ดฝั่งเซิร์ฟเวอร์ที่รวมฝั่งเซิร์ฟเวอร์เพื่อดำเนินงานที่ไม่สามารถทำได้ด้วย HTML ธรรมดา แม้ว่าจะคล้ายกับ [HTML](/th/web/html/) แต่ STML ให้ประสิทธิภาพที่มากกว่าด้วยการเรียกใช้คำสั่งบนเซิร์ฟเวอร์ หรือเรียกอีกอย่างว่า รวมฝั่งเซิร์ฟเวอร์ (SSI) ด้วยการแนะนำภาษาโปรแกรมใหม่พร้อมสคริปต์ฝั่งเซิร์ฟเวอร์ เช่น PHP ทำให้การใช้ STML ลดลง แม้ว่าเทคโนโลยีฝั่งเซิร์ฟเวอร์ทั้งหมดจะยังคงรองรับอยู่ก็ตาม ไฟล์ STML สามารถเปิดได้ในโปรแกรมแก้ไขข้อความและแก้ไขเพื่ออัปเดตคำสั่ง

## รูปแบบไฟล์ STML

STML ขึ้นอยู่กับรูปแบบไฟล์ข้อความ ASCII ธรรมดาที่มนุษย์สามารถอ่านได้ อย่างไรก็ตาม เป็นไปตามไวยากรณ์ที่กำหนดและใช้ [คำสั่ง SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) ที่ดำเนินการทางฝั่งเซิร์ฟเวอร์ เช่นเดียวกับภาษาสคริปต์ฝั่งเซิร์ฟเวอร์อื่นๆ STML สามารถใช้คำสั่งฝั่งเซิร์ฟเวอร์เพื่อดำเนินการต่างๆ เช่น ตัวนับผู้เข้าชมเพจ ปฏิทินหน้าเว็บ ดึงข้อมูลบันทึกจากฐานข้อมูล และอื่นๆ ที่คล้ายกัน

## ตัวอย่าง STML

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

