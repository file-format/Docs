{
  "date" : "2020-08-20",
  "keywords" :[ "ไฟล์ eot", "รูปแบบไฟล์ eot", "ไฟล์ eot คืออะไร", "ไฟล์", "ตัวอย่าง eot", "นามสกุลไฟล์ eot","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - รูปแบบไฟล์แบบอักษร TrueType",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ EOT และ API เพื่อสร้างและเปิดไฟล์ EOT",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## ไฟล์ EOT คืออะไร??

ไฟล์ที่มีนามสกุล .eot เป็นฟอนต์ OpenType ที่ฝังอยู่ในเอกสาร ส่วนใหญ่จะใช้ในไฟล์เว็บ เช่น เว็บเพจ สร้างขึ้นโดย Microsoft และรองรับโดยผลิตภัณฑ์ของ Microsoft รวมถึงไฟล์งานนำเสนอ PowerPoint [.pps](/th/presentation/pps) ไฟล์นี้ไม่ใช่การใช้งานหลักและเป็นเอกสารประกอบกับเอกสารหลักหรือหน้าเว็บ เช่นเดียวกับแบบอักษร OTF EOT รองรับทั้งโครงร่าง Postscript และ TrueType สำหรับสัญลักษณ์ ไฟล์ EOT มีขนาดเล็กลงเนื่องจากบีบอัดโดยใช้การบีบอัด LZ EOT ใช้เครื่องมือของ Microsoft เพื่อสร้างฟอนต์จากฟอนต์ TTF/OTF ที่มีอยู่

## ประวัติย่อ

ฟอนต์ EOT ถูกส่งไปยัง W3C ในปี 2550 โดยเป็นส่วนหนึ่งของ CSS3 แต่เนื่องจากข้อกำหนดในการติดตั้งอย่างถาวรบนระบบระยะไกลจึงกลายเป็นสาเหตุของการปฏิเสธ มีการส่งอีกครั้งในเดือนมีนาคม 2551 แต่ในที่สุด W3C เลือก [รูปแบบแบบอักษรของเว็บ](/th/font/woff/) (WOFF) ซึ่งเป็นมาตรฐานในตอนนั้น

## รูปแบบไฟล์ EOT

ดูรายละเอียดรูปแบบไฟล์ EOT ได้ที่ [หน้าส่ง W3](https://www.w3.org/Submission/EOT/#FileFormat) และอธิบายรายละเอียดเกี่ยวกับโครงสร้างที่ใช้โดยรูปแบบตัวอักษรนี้ EOT ประกอบด้วยโครงสร้าง EMBEDDEDFONT เดียวที่ให้ข้อมูลพื้นฐานเพียงพอเกี่ยวกับชื่อแบบอักษร hte และอักขระที่รองรับ การบรรจุข้อมูลนี้ทำให้ User Agent หลีกเลี่ยงการแกะ ขยายขนาด หรือติดตั้งฟอนต์หากมีอยู่แล้วในเครื่อง

### โครงสร้าง EMBEDDEDFONT
โครงสร้าง EMBEDDEDFONT ได้รับการแก้ไขสามครั้ง โดยมีการเพิ่มข้อมูลเพิ่มเติมที่ส่วนท้ายของโครงสร้างในการแก้ไขแต่ละครั้ง การแก้ไขล่าสุดของโครงสร้าง EMBEDDEDFONT แสดงไว้ด้านล่าง

|ประเภทข้อมูล|ชื่อรายการ|รายละเอียด|
---|---|---|
|unsigned long|EOTSize|ความยาวโครงสร้างทั้งหมดเป็นไบต์ (รวมถึงข้อมูลสตริงและแบบอักษร)|
|ความยาวที่ไม่ได้ลงนาม|FontDataSize|ความยาวของแบบอักษร OpenType (FontData) ในหน่วยไบต์|
|ความยาวที่ไม่ได้ลงนาม|เวอร์ชัน|หมายเลขเวอร์ชันของรูปแบบนี้ - 0x00020002|
|ความยาวที่ไม่ได้ลงนาม|แฟล็ก|กำลังประมวลผลแฟล็ก|
|byte[10]|FontPANOSE|ค่า PANOSE สำหรับฟอนต์นี้ - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|ใน Windows สิ่งนี้ได้มาจาก TEXTMETRIC.tmCharSet ค่านี้ระบุชุดอักขระของฟอนต์ DEFAULT_CHARSET (0x01) ระบุว่าไม่มีการตั้งค่า - ดู https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|หากตั้งค่าบิตสำหรับ ITALIC ใน OS/2.fsSelection ค่าจะเป็น 0x01 - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|ค่าน้ำหนักสำหรับแบบอักษรนี้ - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|ธงประเภทที่ให้ข้อมูลเกี่ยวกับสิทธิ์ในการฝัง - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Magic number สำหรับไฟล์ EOT - 0x504C. ใช้ในการตรวจสอบความเสียหายของข้อมูล|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (บิต 0-31) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (บิต 32-63) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (บิต 64-95) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (บิต 96-127) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|ความยาวที่ไม่ได้ลงนาม|CodePageRange1|CodePageRange1 (บิต 0-31) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|ความยาวที่ไม่ได้ลงนาม|CodePageRange2|CodePageRange2 (บิต 32-63) - ดู https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|ความยาวที่ไม่ได้ลงชื่อ|CheckSumAdjustment|head.CheckSumAdjustment - ดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|ไม่ได้ลงนามยาว|สงวน1|สงวน - ต้องเป็น 0|
|ไม่ได้ลงนามยาว|สงวน2|สงวน - ต้องเป็น 0|
|ความยาวที่ไม่ได้ลงชื่อ|สงวนไว้ 3|สงวนไว้ - ต้องเป็น 0|
|ไม่ได้ลงชื่อยาว|สงวนไว้4|สงวนไว้ - ต้องเป็น 0|
|unsigned short|Padding1|Padding เพื่อรักษาแนวยาว ค่าการเติมจะต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|FamilyNameSize|จำนวนไบต์ที่ใช้โดยอาร์เรย์ FamilyName|
|byte|FamilyName[FamilyNameSize]|อาร์เรย์ UTF-16 อักขระที่มีความยาวเท่ากับ FamilyNameSize ไบต์ นี่คือสตริงตระกูลฟอนต์ภาษาอังกฤษที่พบในตารางชื่อของฟอนต์ (ชื่อ ID = 1) - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|ค่า Padding ต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|StyleNameSize|จำนวนไบต์ที่ใช้โดย StyleName|
|byte|StyleName[StyleNameSize]|อาร์เรย์ของอักขระ UTF-16 ที่มีความยาวเท่ากับไบต์ของ StyleNameSize นี่คือสตริงตระกูลย่อยของฟอนต์ภาษาอังกฤษที่พบในตารางชื่อของฟอนต์ (ชื่อ ID = 2) - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|ค่า Padding ต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|VersionNameSize|จำนวนไบต์ที่ใช้โดย VersionName|
|bytes|VersionName[VersionNameSize]|อาร์เรย์ของอักขระ UTF-16 ที่มีความยาวเท่ากับ Bytes VersionNameSize นี่คือสตริงเวอร์ชันภาษาอังกฤษที่พบในตารางชื่อของแบบอักษร (ชื่อ ID = 5) - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|ค่า Padding ต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|FullNameSize|จำนวนไบต์ที่ใช้โดย FullName|
|byte|FullName[FullNameSize]|อาร์เรย์ของอักขระ UTF-16 ที่มีความยาวเท่ากับไบต์ FullNameSize นี่คือสตริงชื่อเต็มภาษาอังกฤษที่พบในตารางชื่อของแบบอักษร (ชื่อ ID = 4) - โปรดดูที่ https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|ค่า Padding ต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|RootStringSize|จำนวนไบต์ที่ใช้โดยอาร์เรย์ RootString|
|byte|RootString[RootStringSize]|อาร์เรย์ของอักขระ UTF-16 ที่มีความยาวเท่ากับ RootStringSize ไบต์|
|ความยาวที่ไม่ได้ลงชื่อ|RootStringCheckSum|ค่า RootString CheckSum ดูอัลกอริทึมในการประมวลผล RootStringChecksum ด้านล่าง|
|unsigned long|EUDCCodePage|ค่า Codepage ที่จำเป็นสำหรับการสนับสนุนแบบอักษร EUDC|
|unsigned short|Padding6|ค่า Padding ต้องตั้งค่าเป็น 0x0000 เสมอ|
|unsigned short|SignatureSize|จำนวนไบต์ที่ใช้โดยอาร์เรย์ Signature สงวนไว้ในขณะนี้และควรตั้งค่าเป็น 0x0000|
|byte|Signature[SignatureSize]|ปัจจุบันสงวนไว้ ถ้า SignatureSize เป็น 0x0000 แสดงว่าอาร์เรย์นี้ไม่มีความยาว|
|unsigned long|EUDCFlags|กำลังประมวลผลแฟล็กสำหรับฟอนต์ EUDC ค่าทั่วไปอาจเป็น TTEMBED_XORENCRYPTDATA และ TTEMBED_TTCOMPRESSED|
|unsigned long|EUDCFontSize|จำนวนไบต์ที่ใช้โดยอาร์เรย์ Signature|
|byte|EUDCFontData[EUDCFontSize]|จำนวนไบต์ที่ใช้สำหรับข้อมูลแบบอักษร EUDC ถ้า EUDCFontSize เป็น 0x00000000 แสดงว่าอาร์เรย์นี้ไม่มีความยาว|
|byte|FontData[FontDataSize]|ข้อมูลฟอนต์สำหรับไฟล์ EOT นี้ ข้อมูลอาจถูกบีบอัดหรือเข้ารหัส XOR ตามที่ระบุโดยแฟล็กการประมวลผล|

## อ้างอิง

* [รูปแบบไฟล์ EOT](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [การฝังแบบอักษร](https://en.wikipedia.org/wiki/Font_embedding)

