{
  "date" : "2020-01-11",
  "keywords" :[ "x file", "x file format", "x file คืออะไร", "file", "x example", "x file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ X - DirectX 2.0",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ DirectX X และ API ที่สามารถเปิดและสร้างไฟล์ DirectX X",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## ไฟล์ X คืออะไร?

ไฟล์ที่มีนามสกุล .x อ้างอิงถึง [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) รูปแบบไฟล์ดั้งเดิมของกราฟิก 3D ที่นำมาใช้กับ Microsoft DirectX 2.0 ใช้สำหรับการเรนเดอร์กราฟิก 3 มิติในเกม และระบุโครงสร้างสำหรับตาข่าย พื้นผิว ภาพเคลื่อนไหว และวัตถุที่ผู้ใช้กำหนด มันถูกเลิกใช้ตั้งแต่ปี 2014 เนื่องจากรูปแบบไฟล์ Autodesk FBX ทำหน้าที่ได้ดีกว่าในรูปแบบที่ทันสมัยกว่า X ขับเคลื่อนด้วยเทมเพลตและไม่มีความรู้ด้านการใช้งานใดๆ

คุณสามารถเปิดไฟล์ DirectX X ได้โดยใช้ Microsoft DirectX และโปรแกรมแก้ไขข้อความทั่วไป

## X รูปแบบไฟล์

[การอ้างอิงไฟล์ X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) มีข้อมูลอ้างอิงสำหรับองค์ประกอบ API ที่ใช้ในการ ทำงานกับไฟล์ DirectX .x รูปแบบจัดเตรียมข้อมูลเบื้องต้นระดับต่ำที่แอปพลิเคชันอื่นใช้เพื่อกำหนดข้อมูลเบื้องต้นระดับสูงกว่าผ่านเทมเพลตข้อมูล DirectX 6.0 แนะนำอินเทอร์เฟซและวิธีการที่ช่วยให้สามารถอ่านและเขียนไฟล์ .x ได้ DirectX 3.0 แนะนำรูปแบบไฟล์ไบนารีเวอร์ชันนี้

[การอ้างอิงรูปแบบไฟล์ X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) ที่กำหนดโดย DirectX 9 มีข้อมูลอ้างอิงสำหรับ .x ไฟล์ในไบนารีเช่นเดียวกับการเข้ารหัสข้อความ

### การเข้ารหัสไบนารี

[รูปแบบไบนารี](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) กำหนดรูปแบบ DirectX X เป็นการแสดงโทเค็นของรูปแบบข้อความ โทเค็นเหล่านี้สามารถเป็นแบบสแตนด์อโลนเพื่อให้มีโครงสร้างทางไวยากรณ์หรือสามารถเป็นโทเค็นที่มีการบันทึกซึ่งให้ข้อมูลที่จำเป็น

#### หัวข้อ

ส่วนหัวไบนารีสามารถอ่านและเขียนได้โดยใช้คำจำกัดความต่อไปนี้

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### การเข้ารหัสข้อความ

ไฟล์ DirectX .x ไม่ได้ขึ้นอยู่กับวิธีการใช้ไฟล์ และไม่เฉพาะเจาะจงกับแอปพลิเคชันใดๆ วิธีการที่ขับเคลื่อนด้วยเทมเพลตนี้ช่วยให้แอปพลิเคชันไคลเอ็นต์ใช้รูปแบบไฟล์ .x ได้


#### หัวข้อ

ส่วนหัวที่มีความยาวผันแปรเป็นค่าบังคับและต้องอยู่ที่จุดเริ่มต้นของสตรีมข้อมูล ส่วนหัวประกอบด้วยข้อมูลต่อไปนี้

|ประเภท |ประเภทย่อย |ขนาด |เนื้อหา |ความหมายของเนื้อหา|
---|---|---|---|---|
|เลขวิเศษ (จำเป็น)| | 4 ไบต์ |xof |
|หมายเลขเวอร์ชัน (จำเป็น) |หมายเลขหลัก |2 ไบต์ |03 |เวอร์ชันหลัก 3|
| |จำนวนรอง |2 ไบต์ |02 |รุ่นรอง 2|
|ประเภทรูปแบบ (จำเป็น)| |4 ไบต์ |"txt " |ไฟล์ข้อความ|
| | | |"ถัง" | ไฟล์ไบนารี|
| | | |"ซิป"| ไฟล์ข้อความบีบอัด MSZip|
| | | |"bzip"| ไฟล์ไบนารีบีบอัด MSZip|
|ขนาดลูกลอย (จำเป็น)| |4 ไบต์| 0064| โฟลต 64 บิต|
| | | |0032 |โฟลต 32 บิต|


## อ้างอิง

* [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [การอ้างอิงรูปแบบไฟล์ DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

