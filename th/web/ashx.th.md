{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"นามสกุลไฟล์ ASHX - ไฟล์ตัวจัดการเว็บ ASP.NET",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ ASHX และ API ที่สามารถสร้างและเปิดไฟล์ ASHX ได้",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## ไฟล์ ASHX คืออะไร??

ไฟล์ ASHX เป็นเว็บเพจที่ใช้โดย ASP.NET HTTP Handler เพื่อให้บริการผู้ใช้ด้วยเพจที่อ้างอิงภายในไฟล์นี้ ASP.NET HTTP Handler ประมวลผลคำขอที่เข้ามา อ้างอิงเพจจากไฟล์ .ashx และส่งเพจที่คอมไพล์แล้วกลับไปยังเบราว์เซอร์ของผู้ใช้ วิธีการประมวลผลส่วนใหญ่คล้ายกับไฟล์ ASPX โดยมีความแตกต่างคือในกรณีนี้ หน้า/เอกสารที่อ้างอิงจะได้รับการประมวลผลและส่งกลับ

## รูปแบบไฟล์ ASHX

ไฟล์ .ashx จะถูกบันทึกในรูปแบบไฟล์ข้อความล้วน และมีการอ้างอิงถึงหน้าหรือเอกสารอื่นๆ ที่ส่งกลับไปยังเบราว์เซอร์ของผู้ใช้เมื่อมีการร้องขอ สามารถเปิดได้ในโปรแกรมแก้ไขข้อความและ IDE ของนักพัฒนา เช่น Xamarin Studio, Microsoft Notepad, Notepad++ และอื่นๆ อีกมากมาย ไฟล์ ASHX มีประโยชน์ในกรณีที่คุณมี:
* ไฟล์ไบนารี
* มุมมองภาพแบบไดนามิก
* หน้าเว็บที่เน้นประสิทธิภาพ
* ไฟล์ XML
* หน้าเว็บขั้นต่ำ

## จะรวบรวมไฟล์ ASHX แบบไดนามิกได้อย่างไร

สามารถใช้ขั้นตอนต่อไปนี้เพื่อเพิ่มและคอมไพล์ไฟล์ ASHX โดยใช้ Microsoft Visual Studio

* เพิ่มตัวจัดการทั่วไป - Handler1.ashx ใน Visual Studio
* ลบไฟล์ cs ที่สร้างอัตโนมัติ
* เปิด ashx อีกครั้ง
** ลบ CodeBehind="Handler1.ashx.cs"
** เพิ่มรหัส c# ด้านล่าง

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### ตัวอย่าง ASHX

รหัส ASHX ต่อไปนี้ส่งคืนไฟล์ภาพตามคำขอของผู้ใช้ เมื่อไฟล์ ASHX ถูกเรียกในเบราว์เซอร์อินเทอร์เน็ต


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## อ้างอิง

* [รวบรวมไฟล์ ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


