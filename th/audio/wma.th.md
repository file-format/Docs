{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "file", "extension", "format", "audio interchange file format", "music" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WMA และ API ที่สามารถสร้างและเปิดไฟล์ WMA",
  "title" :"WMA - ไฟล์เสียง Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## ไฟล์ WMA คืออะไร??

ไฟล์ที่มีนามสกุล .wma แสดงถึงไฟล์เสียงที่บันทึกในรูปแบบ Advanced Systems Format (ASF) ASF เป็นรูปแบบกรรมสิทธิ์ของ Microsoft ที่มีบิตสตรีมที่เข้ารหัสโดย Windows Media Audio 9 นอกจากเนื้อหาที่เป็นเสียงแล้ว ไฟล์ WMA ยังมีวัตถุข้อมูลเมตา เช่น ชื่อเรื่อง อัลบั้ม ศิลปิน และประเภทของแทร็ก ไฟล์ WMA ส่วนใหญ่จะใช้สำหรับการสตรีมผ่านเว็บ คล้ายกับไฟล์ [.mp3](/th/audio/mp3/)

## รูปแบบไฟล์ WMA

ไฟล์ WMA เป็นรูปแบบไฟล์ไบนารีและอยู่ในรูปแบบไฟล์ ASF โดยจะระบุการเข้ารหัสของข้อมูลเมตาเกี่ยวกับไฟล์ที่คล้ายกับแท็ก ID3 ที่ใช้โดยไฟล์ MP3 Microsoft ใช้งานตัวแปลงสัญญาณ WMA ในรูปแบบไฟล์ที่ทำงานร่วมกันระหว่างกัน (Protected Interoperable File Format - PIFF) ตั้งแต่ปี 2551 อย่างไรก็ตาม ตัวแปลงสัญญาณดังกล่าวยังไม่ได้รับการประกาศให้เป็นตัวแปลงสัญญาณเสียงมาตรฐานตามมาตรฐานอุตสาหกรรมที่เกี่ยวข้อง เช่น DECE UltraViolet และ MPEG-DASH

### ข้อมูลเฉพาะประเภท WMA

ข้อมูลเฉพาะประเภทสำหรับตัวแปลงสัญญาณ Windows Media Audio ถูกจัดเก็บไว้ในรูปแบบต่อไปนี้โดยเป็นส่วนหนึ่งของข้อมูลเฉพาะประเภทของวัตถุคุณสมบัติสตรีม

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## อ้างอิง

* [ภาพรวม ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

