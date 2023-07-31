{
  "date" : "2019-10-11",
  "keywords" :[ "asax","ไฟล์ asax", "รูปแบบไฟล์ asax", "ประเภทไฟล์ asax", "ไฟล์", "ประเภท", "ไฟล์ asax คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์แอปพลิเคชันเซิร์ฟเวอร์ ASAX - ASP.NET",
  "description" :"เรียนรู้ว่าไฟล์ ASAX และ API คืออะไรที่สามารถสร้างและเปิดไฟล์ ASAX ได้",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## ไฟล์ ASAX คืออะไร??

ไฟล์ที่มีนามสกุล .asax คือไฟล์ที่ใช้โดยแอปพลิเคชัน ASP.NET ซึ่งอยู่ในฝั่งเซิร์ฟเวอร์ ประกอบด้วยรหัสสำหรับตอบสนองต่อเหตุการณ์ระดับแอปพลิเคชันและระดับเซสชันที่ ASP.NET หรือโมดูล HTTP สร้างขึ้น ซึ่งรวมถึงการจัดการเหตุการณ์บางอย่างเมื่อเปิดหรือปิดแอปพลิเคชัน ไฟล์ ASAX เป็นทางเลือกและมีเพียงไฟล์ ASAX ไฟล์เดียวที่เพิ่มไปยังเว็บแอปพลิเคชันเพื่อจัดการกับเหตุการณ์ระดับแอปพลิเคชันและข้อผิดพลาดในระดับโลก ซึ่งแตกต่างจากหน้า ASPX ไฟล์ ASAX ไม่มีรหัสใด ๆ เพื่อใช้ฟังก์ชันการทำงานของแอปพลิเคชัน

## รูปแบบไฟล์ ASAX

ไฟล์ ASAX เขียนในรูปแบบไฟล์ข้อความธรรมดาและสามารถอ่านได้ ไฟล์ ASAX ที่ใช้บ่อยที่สุดคือ Global.asax ซึ่งอยู่ในไดเรกทอรีรากของแอปพลิเคชัน ASP.NET เว็บเซิร์ฟเวอร์ได้รับการกำหนดค่าให้ปฏิเสธสายที่เรียกเข้ามาที่ไฟล์นี้ เพื่อห้ามไม่ให้ผู้ใช้ดาวน์โหลดหรือดูโค้ดของไฟล์นี้

### Global.ASAX - ตัวอย่างของรูปแบบไฟล์ ASAX

ไฟล์ ASAX ไฟล์เดียวประกอบด้วยหลายส่วนที่เขียนขึ้นเพื่อจัดการเหตุการณ์ระดับแอปพลิเคชัน มีดังต่อไปนี้

* **คำสั่งแอปพลิเคชัน** - คำสั่งแอปพลิเคชันคือแท็กที่ใช้เพื่อกำหนดการตั้งค่าเฉพาะแอปพลิเคชันเพิ่มเติมที่จะใช้โดยโปรแกรมแยกวิเคราะห์ ASP.NET เมื่อประมวลผลไฟล์ Global.asax คำสั่งเหล่านี้อยู่ในส่วนเริ่มต้นของไฟล์ Global.asax และกำหนดไว้ดังนี้

```
<%@ คำสั่งแอตทริบิวต์=ค่า [แอตทริบิวต์=ค่า … ]%>
```
* **Code Declaration Blocks** - บล็อกการประกาศรหัสใช้เพื่อกำหนดส่วนของรหัสเซิร์ฟเวอร์ที่ฝังอยู่ในไฟล์แอปพลิเคชัน ASP.NET ภายใน \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - สิ่งเหล่านี้กำหนดโค้ดหรือนิพจน์แบบอินไลน์ที่ดำเนินการเมื่อเพจถูกเรนเดอร์ บล็อกการแสดงโค้ดสองสไตล์ประกอบด้วยโค้ดแบบอินไลน์และนิพจน์แบบอินไลน์ แบบแรกใช้เพื่อกำหนดบรรทัดหรือบล็อกของโค้ดที่มีในตัวเอง ในขณะที่ด้านข้างใช้เป็นทางลัดสำหรับการเรียกใช้เมธอด Write

## อ้างอิง

* [ภาพรวมตัวจัดการ HTTP และโมดูล HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [ไวยากรณ์ Global.asax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

