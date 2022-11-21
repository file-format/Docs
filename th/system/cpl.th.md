{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "ไฟล์แผงควบคุม", "Windows", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - ไฟล์แผงควบคุม",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CPL และ API ที่สามารถสร้างและเปิดไฟล์ CPL",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ไฟล์ CPL คืออะไร?? ##

ไฟล์ CPL เป็นไฟล์ประเภท "ระบบ" มันถูกใช้งานโดยระบบปฏิบัติการ Windows ไฟล์ CPL ย่อมาจากไฟล์แผงควบคุม ไฟล์เหล่านี้เป็นไฟล์ไบนารีที่เปิดด้วยแผงควบคุมในระบบปฏิบัติการ Microsoft Windows และใช้เพื่อแสดงและเปิดเครื่องมือที่มีอยู่ในแผงควบคุม เช่น เมาส์ จอแสดงผล ระบบเครือข่าย และอื่นๆ โดยทั่วไป ไฟล์ CPL จะถูกจัดเก็บไว้ในโฟลเดอร์ระบบบนอุปกรณ์ของคุณ ไม่ควรเปิดไฟล์เหล่านี้ด้วยตนเอง


## รูปแบบไฟล์ CPL ##

ไฟล์ CPL ต่างๆ ในระบบปฏิบัติการ Windows ของคุณเชื่อมต่อกันเพื่อแสดงรายการแผงควบคุมต่างๆ รายการแผงควบคุมทั้งหมดเชื่อมโยงกับไฟล์ CPL และมีส่วนต่อท้าย ".cpl" ต่อท้ายรายการ

ไฟล์ CPL บางประเภททั่วไปที่มีรูปแบบคือ:

* Inetcpl.cpl – สำหรับคุณสมบัติของอินเทอร์เน็ตบนอุปกรณ์ของคุณ
* Appwiz.cpl – เพื่อเพิ่มหรือลบคุณสมบัติของโปรแกรมบนอุปกรณ์ของคุณ
* Desk.cpl – สำหรับคุณสมบัติการแสดงผล
* Main.cpl – สำหรับคุณสมบัติที่เกี่ยวข้องกับเมาส์ แบบอักษร แป้นพิมพ์ และเครื่องพิมพ์
* Netcpl.cpl – สำหรับคุณสมบัติที่เกี่ยวข้องกับเครือข่าย
* System.cpl – สำหรับคุณสมบัติที่เกี่ยวข้องกับระบบและเพื่อเพิ่มตัวช่วยสร้างฮาร์ดแวร์ใหม่
* TimeDate.cpl – สำหรับคุณสมบัติวันที่หรือเวลา
* Mlcfg32.cpl – สำหรับคุณสมบัติ Microsoft Exchange หรือ Windows Messaging
* Intl.cpl – สิ่งนี้เกี่ยวข้องกับคุณสมบัติการตั้งค่าภูมิภาค
* Modem.cpl – สำหรับคุณสมบัติที่เกี่ยวข้องกับโมเด็ม
* Themes.cpl – จัดเก็บธีมและคุณสมบัติของเดสก์ท็อป
* Password.cpl – สำหรับคุณสมบัติรหัสผ่าน
* Mmsys.cpl – สำหรับคุณสมบัติมัลติมีเดีย
* Wgpocpl.cpl – เกี่ยวข้องกับ Microsoft Mail Post Office

## ประวัติย่อ ##

ประเภทไฟล์ CPL ได้รับการพัฒนาโดย Microsoft Windows และเป็นส่วนสำคัญของระบบปฏิบัติการ Windows ตั้งแต่ Windows 1.0 ยังคงใช้ใน Windows ทุกรุ่น และคุณสมบัติรายการแผงควบคุมทั้งหมดจะถูกจัดเก็บโดยใช้ไฟล์ประเภทนี้

## ตัวอย่าง CPL ##

ตัวอย่างไฟล์ CPL สามารถดูได้ที่ด้านล่าง:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
