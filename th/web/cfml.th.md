{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ไฟล์ภาษามาร์กอัป ColdFusion",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ CFML และ API ที่สามารถสร้างและเปิดไฟล์ CFML ได้",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## ไฟล์ CFML คืออะไร??

ไฟล์ที่มีนามสกุล .cfml คือไฟล์ภาษามาร์กอัป ColdFusion ที่ใช้สร้างหน้าเว็บ หมายถึงชุดของกฎที่ใช้กำหนดว่าโปรแกรมเมอร์ ColdFusion จะพัฒนาอย่างไร ColdFusion เป็นภาษาโปรแกรมที่ใช้สร้างเว็บแอปพลิเคชันฝั่งเซิร์ฟเวอร์อย่างรวดเร็วและใช้เทคโนโลยีน้อยกว่าอื่นๆ เช่น [ASP](/th/web/asp/), [PHP](/th/programming/php/) เป็นต้น บางภาษา แอปพลิเคชันที่สามารถเปิดไฟล์ CML ได้แก่ Adobe ColdFusion 2018, Adobe ColdFusion Builder และ Adobe Dreamweaver

## รูปแบบไฟล์ CFML - ข้อมูลเพิ่มเติม

ไฟล์ CFML เป็นไฟล์มาร์กอัปและมีองค์ประกอบเว็บในรูปแบบของแท็ก ไฟล์เหล่านี้เป็นไฟล์ข้อความที่สามารถเปิดและแก้ไขได้ในโปรแกรมแก้ไขข้อความใดๆ ไฟล์ CFML ประกอบด้วยแท็กหลายแท็กที่คล้ายกับ [HTML](/th/web/html/) และมักจะประกอบด้วยแท็กเปิดและแท็กปิด แท็กเหล่านี้สามารถมีแอตทริบิวต์ตั้งแต่หนึ่งรายการขึ้นไป

### แท็กไวยากรณ์

ต่อไปนี้คือไวยากรณ์ทั่วไปของแท็ก CFML

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

แท็กส่วนใหญ่ยอมรับแอตทริบิวต์และถูกกำหนดดังนี้

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

แท็กเหล่านี้บางแท็กยังยอมรับแอตทริบิวต์หลายรายการด้วยไวยากรณ์ต่อไปนี้

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## ตัวอย่างรหัส CFML

นี่คือตัวอย่างที่ใช้แท็ก CFML จริง - แท็ก `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## อ้างอิง

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

