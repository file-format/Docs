{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ PCX - ไฟล์ภาพบิตแมปพู่กัน",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PCX และ API ที่สามารถสร้างและเปิดไฟล์ PCX",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## ไฟล์ PCX คืออะไร??

ไฟล์ PCX ซึ่งเป็นไฟล์ Picture Exchange เป็นรูปแบบไฟล์ภาพแรสเตอร์ที่ใช้เป็นรูปแบบไฟล์เนทีฟสำหรับแอปพลิเคชัน PC Paintbrush ได้รับการพัฒนาโดย ZSoft Corporation ประเทศสหรัฐอเมริกาสำหรับแพลตฟอร์ม DOS และ Windows และถูกนำมาใช้เป็นรูปแบบไฟล์ภาพหลักก่อนที่ [BMP](/th/image/bmp/), [JPEG](/th/image/jpeg/) และ [ PNG](/th/image/png/) รูปแบบไฟล์ ไฟล์ PCX มีขนาดเล็กลงเนื่องจากบีบอัดโดยใช้การเข้ารหัส RLE ใช้ในไฟล์ [DCX](/th/image/dcx/) แบบหลายหน้าที่ใช้เป็นหลักในการสร้างไฟล์โทรสารดิจิทัล

## รูปแบบไฟล์ PCX

ไฟล์ PCX ถูกบันทึกลงดิสก์ในรูปแบบไฟล์ไบนารี โครงสร้างรูปแบบไฟล์ภายในเป็นไปตามการเรียงลำดับไบต์แบบ endian เล็กน้อย และมีสามส่วนต่อไปนี้:

**`PCX Header`** - PCX Header มีความยาว 128 ไบต์ ประกอบด้วยตัวระบุ หมายเลขรุ่น ขนาดภาพ จานสี 16 สี ระนาบสีตัวเลข และความลึกบิตของแต่ละระนาบ และค่าสำหรับวิธีการบีบอัด

PCX Header แสดงด้านล่างโดยอ้างอิงจาก Encyclopedia of graphics file formats (ครั้งที่ 2nd.)
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Image Data`** - ข้อมูลรูปภาพ PCX ตามหลังส่วนหัว ข้อมูลรูปภาพอาจถูกบีบอัดขึ้นอยู่กับการตั้งค่าฟิลด์ในส่วนหัว การจัดเก็บข้อมูลในไฟล์ PCX ขึ้นอยู่กับจำนวนระนาบสีที่กำหนด ข้อมูลรูปภาพถูกจัดเรียงเป็นแถว ในกรณีของระนาบหลายระนาบ ระนาบเหล่านี้จะถูกจัดเก็บในระนาบภายในแถวโดยจัดเรียงข้อมูลสีแดง เขียว และน้ำเงินตามลำดับ รูปแบบนี้ซ้ำสำหรับแต่ละบรรทัดในระนาบ

## อ้างอิง

* [PCX - โดย Wikipedia](https://en.wikipedia.org/wiki/PCX)

