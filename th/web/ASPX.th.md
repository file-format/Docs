{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","ไฟล์ aspx", "รูปแบบไฟล์ aspx", "ประเภทไฟล์ aspx", "ไฟล์", "ประเภท", "ไฟล์ aspx คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ ASPX",
  "description" :"คู่มือรูปแบบไฟล์ของคุณเพื่อเรียนรู้ว่าไฟล์ ASPX และ API ใดที่สามารถสร้างและเปิดไฟล์ ASPX ได้",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ไฟล์ ASPX คืออะไร??

ไฟล์ที่มีนามสกุล .aspx คือเว็บเพจที่สร้างขึ้นโดยใช้กรอบงาน Microsoft ASP.NET ที่ทำงานบนเว็บเซิร์ฟเวอร์ ASPX ย่อมาจาก Active Server Pages Extended และหน้าเหล่านี้จะแสดงในเว็บเบราว์เซอร์ที่ปลายทางของผู้ใช้เมื่อเข้าถึง URL เป็นผู้สืบทอดของเทคโนโลยี [ASP](/th/web/asp/) ซึ่งสร้างขึ้นที่ฝั่งเซิร์ฟเวอร์เช่นกัน แต่ไม่ได้ใช้ .NET framework หน้า ASP.NET อาจมีสคริปต์ [C#](/th/programming/cs/) หรือ [VB.NET](/th/programming/vb/) ที่เว็บเซิร์ฟเวอร์แปลเป็น HTML เพื่อนำเสนอต่อผู้ใช้ในเว็บเบราว์เซอร์ หน้า ASPX เรียกอีกอย่างว่า .NET Web Forms สามารถเปิดและสร้างด้วยแอปพลิเคชันเช่น Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ และโปรแกรมแก้ไขข้อความใดๆ

## รูปแบบไฟล์ ASPX

เว็บฟอร์ม ASP.NET ขึ้นอยู่กับโมเดลที่ขับเคลื่อนด้วยเหตุการณ์สำหรับการโต้ตอบกับเว็บแอปพลิเคชัน เบราว์เซอร์ที่เป็นผู้ใช้ส่งแบบฟอร์มเว็บไปยังเซิร์ฟเวอร์และเซิร์ฟเวอร์ส่งคืนหน้ามาร์กอัปแบบเต็มหรือหน้า HTML เพื่อตอบสนอง โมเดลคอมโพเนนต์ ASP.NET มีโมเดลวัตถุสำหรับเพจ ASPX โมเดลนี้อธิบายถึง:

* คู่ฝั่งเซิร์ฟเวอร์ขององค์ประกอบหรือแท็ก HTML เกือบทั้งหมด เช่น \<form> และ \<input> .
* การควบคุมเซิร์ฟเวอร์ซึ่งช่วยในการพัฒนาส่วนติดต่อผู้ใช้ที่ซับซ้อน ตัวอย่างเช่น ตัวควบคุมปฏิทินหรือตัวควบคุม Gridview

ไฟล์ ASPX ใช้ ASP.NET **Code Behind model** สำหรับการสร้างเพจเหล่านี้

### รหัสในบรรทัด

โค้ดตัวอย่างที่ฝังแบบอินไลน์ในเพจ ASPX และมีฟังก์ชันทั้งหมดสำหรับการใช้งานของผู้ใช้ โค้ด [C#](/th/programming/cs/) ต่อไปนี้แสดงถึงเพจ ASP.NET ตัวอย่างที่มีโค้ดแบบอินไลน์:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### รหัสเบื้องหลัง

โค้ดสามารถเขียนและจัดเก็บไว้ในไฟล์คลาสที่แยกจากกันเพื่อแยก HTML ออกจากตรรกะการนำเสนอ สิ่งนี้ทำให้เลเยอร์การนำเสนอเป็นอิสระจากรหัสปฏิบัติการ ต่อไปนี้คือโค้ดเบื้องหลังสำหรับการนำเสนอต่อผู้ใช้

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

การใช้ C# ของตรรกะจริงสำหรับเลเยอร์การนำเสนอมีดังนี้

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## อ้างอิง

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

