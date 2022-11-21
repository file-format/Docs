{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ DDS- ไฟล์ภาพพื้นผิว DirectDraw",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DDS และ API ที่สามารถสร้างและเปิดไฟล์ DDS",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## ไฟล์ DDS คืออะไร??

ไฟล์ DDS เป็นไฟล์ภาพแรสเตอร์ที่ใช้รูปแบบคอนเทนเนอร์ DirectDraw Surface (DDS) มันเก็บพื้นผิวที่ไม่บีบอัดและบีบอัด (DXTn) และใช้ประเภทต่าง ๆ เพื่อจัดเก็บข้อมูลประเภทต่าง ๆ นอกจากนี้ยังสนับสนุนข้อมูลหลายประเภท เช่น พื้นผิวชั้นเดียว พื้นผิวที่มีแผนที่ mipmap แผนที่ลูกบาศก์ แผนที่ปริมาตร และอาร์เรย์พื้นผิว สิ่งนี้ทำให้ไฟล์ DDS สามารถจัดเก็บโมเดลหน่วยพื้นผิวของวิดีโอเกมนอกเหนือจากภาพถ่ายดิจิทัลและพื้นหลังเดสก์ท็อป Windows รูปแบบไฟล์ DDS ได้รับการพัฒนาโดย Microsoft เพื่อใช้กับ DirectX SDK

## รูปแบบไฟล์ ท.บ

ไฟล์ DDS ถูกบันทึกเป็นไฟล์ไบนารีและสามารถใช้กับ DirectX SDK ใช้พลังของ DirectX เพื่อพัฒนาแอปพลิเคชันการเรนเดอร์ตามเวลาจริง เช่น เกม 3 มิติ

### เค้าโครงไฟล์ DDS

[รูปแบบไฟล์ DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) ได้รับการบันทึกโดย Microsoft อย่างละเอียด ไฟล์ Binary DDS มีข้อมูลต่อไปนี้

* DWORD (ตัวเลขมหัศจรรย์) ที่มีค่ารหัสอักขระสี่ตัว 'DDS' (0x20534444)
* คำอธิบายของข้อมูลในไฟล์

DDS_HEADER อธิบายข้อมูลและ DDS_PIXELFORMAT อธิบายรูปแบบพิกเซล ทั้งคู่แทนที่โครงสร้าง DDSURFACEDESC2, DDSCAPS2 และ DDPIXELFORMAT DirectDraw 7 ที่เลิกใช้แล้ว

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[คู่มือการเขียนโปรแกรมของรูปแบบไฟล์ DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) ให้รายละเอียดเพิ่มเติมทางเทคนิคของรูปแบบไฟล์นี้

## อ้างอิง

* [ท.บ. - โดยวิกิพีเดีย](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [คู่มืออ้างอิงทางเทคนิครูปแบบไฟล์ ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

