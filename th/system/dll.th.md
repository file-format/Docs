{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "ไดนามิกลิงก์ไลบรารี", "การตั้งค่า", "โปรแกรม", "คอมพิวเตอร์", "แอปพลิเคชัน" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - ไดนามิกลิงก์ไลบรารี",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DLL และ API ที่สามารถสร้างและเปิดไฟล์ DLL",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ไฟล์ DLL คืออะไร?? ##

ไฟล์ DLL หรือ Dynamic Link Library เป็นไฟล์ปฏิบัติการประเภทหนึ่ง เป็นไฟล์ส่วนขยายที่พบได้บ่อยที่สุดในอุปกรณ์ของคุณ และมักจะจัดเก็บไว้ในโฟลเดอร์ System32 บน Windows ของคุณ ไฟล์นามสกุล DLL ได้รับการพัฒนาโดย Microsoft และเป็นที่นิยมใช้โดยพวกเขา มีคะแนนความนิยมจากผู้ใช้สูง DLL ทำงานเป็นชั้นวางที่มี *ไดรเวอร์/ขั้นตอน/ฟังก์ชัน/คุณสมบัติ* ที่ได้รับการออกแบบและนำไปใช้กับโปรแกรม/แอปพลิเคชันโดยเซิร์ฟเวอร์ windows ไฟล์ DLL ไฟล์เดียวสามารถใช้ร่วมกันระหว่างโปรแกรม Windows ต่างๆ ไฟล์ส่วนขยายเหล่านี้มีความสำคัญต่อการเรียกใช้โปรแกรม Windows บนอุปกรณ์ของคุณอย่างราบรื่น เนื่องจากไฟล์เหล่านี้มีหน้าที่รับผิดชอบในการเปิดใช้งานและเรียกใช้ฟังก์ชันต่างๆ ในโปรแกรม เช่น การเขียนและการอ่านไฟล์ การเชื่อมต่อกับอุปกรณ์อื่นๆ ที่อยู่ภายนอกการตั้งค่าของคุณ
อย่างไรก็ตาม ไฟล์เหล่านี้สามารถเปิดได้บนอุปกรณ์ที่รองรับ Windows รุ่นใดก็ได้เท่านั้น (windows 7/windows 10/อื่นๆ) ดังนั้นจึงไม่สามารถเปิดได้โดยตรงบนอุปกรณ์ที่รองรับ Mac OS (หากคุณต้องการเปิดไฟล์ DLL บน Mac OS แอปพลิเคชันภายนอกต่างๆ สามารถช่วยเปิดได้)


## รูปแบบไฟล์ DLL ##

ไฟล์ DLL ได้รับการพัฒนาโดย Microsoft และมีนามสกุล ".dll" ที่แสดงถึงประเภท เป็นส่วนสำคัญของเซิร์ฟเวอร์ Windows 1.0 และหลังจากนั้น เป็นไฟล์ประเภทไบนารีและรองรับโดย Microsoft Windows ทุกรุ่น ไฟล์ประเภทนี้สร้างขึ้นเพื่อใช้สร้างระบบไลบรารีที่ใช้ร่วมกันภายในโปรแกรม Windows เพื่ออนุญาตให้มีการแก้ไขหรือเปลี่ยนแปลงแยกต่างหากและเป็นอิสระในไลบรารีของโปรแกรม โดยไม่จำเป็นต้องเชื่อมโยงโปรแกรมใหม่


## ตัวอย่าง DLL ##

โค้ดตัวอย่างสำหรับจุดเข้าใช้งาน DLL อยู่ด้านล่าง:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## อ้างอิง ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
