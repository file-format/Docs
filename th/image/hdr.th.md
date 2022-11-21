{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ HDR - ไฟล์ภาพ HDR คืออะไร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ HDR และ API ที่สามารถสร้างและเปิดไฟล์ HDR",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## ไฟล์ HDR คืออะไร?

ไฟล์ HDR เป็นรูปแบบไฟล์ภาพแรสเตอร์ High Dynamic Range (HDR) สำหรับจัดเก็บภาพถ่ายจากกล้องดิจิทัล ช่วยให้โปรแกรมแก้ไขภาพสามารถเพิ่มสีและความสว่างของภาพดิจิทัลที่มีช่วงไดนามิกจำกัดได้ การปรับเปลี่ยนนี้สามารถปรับปรุงความสว่างรอบ ๆ มุม ทำให้ได้ภาพที่ใกล้เคียงกับธรรมชาติ ไฟล์ HDR มักจะบันทึกเป็นภาพแรสเตอร์ 32 บิต Adobe Photoshop สามารถสร้างและเปิดไฟล์ HDR

ไฟล์ HDR เรียกอีกอย่างว่า HDRI

## รูปแบบไฟล์ HDR - ข้อมูลเพิ่มเติม

รูปแบบไฟล์ HDR อ้างอิงจากรูปแบบไฟล์ Radiance Picture (.pic) ดั้งเดิม ข้อมูลพิกเซลของไฟล์ HDR มักจะถูกจัดเก็บโดยไม่บีบอัด แต่ในบางกรณี ข้อมูลพิกเซลจะถูกบีบอัดโดยใช้ระบบการเข้ารหัสความยาวรันไทม์ที่ไม่ซับซ้อน

### โครงสร้างไฟล์ HDR

ไฟล์ภาพ HDR ประกอบด้วยสามส่วนต่อไปนี้:

* **ส่วนหัว:** ไฟล์ HDR ระบุด้วยไบต์แรกในไฟล์ภาพ เช่น "#?RADIANCE"
* **Resolution String:** ส่วนหัวจะตามด้วยบรรทัดความละเอียดเดียวที่ประกอบด้วย 4 ค่า; ป้ายกำกับ X และ Y ตามด้วยค่าตัวเลขจำนวนเต็ม ลำดับของ X และ Y หมายถึงการหมุน การรวมกันของ X และ Y ที่มีค่าบวกและลบครอบคลุมการวางแนวและการหมุนภาพที่เป็นไปได้ทั้งหมด
* **ข้อมูลพิกเซล:** ข้อมูลพิกเซลของไฟล์ HDR ไม่ถูกบีบอัดหรือถูกบีบอัดโดยใช้การเข้ารหัสความยาวรันมาตรฐาน

## Open-Source HDR/HDRI APIs

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - ไลบรารีส่วนหัวเดียวที่เร็วเป็นพิเศษข้ามแพลตฟอร์ม [C++](/th/programming/cpp/) เพื่อรับขนาดและรูปแบบรูปภาพโดยไม่ต้องโหลด/ถอดรหัส
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - ห้องสมุด Rust เพื่อรับขนาดและรูปแบบภาพโดยไม่ต้องโหลด/ถอดรหัส รองรับ [.avif](/th/image/avif/), [.bmp](/th/image/bmp), [.cur](/th/image/cur/), [.dds](/th/image/dds/), [ . gif](/th/image/gif/), hdr (รูปภาพ), [heic (heif)](/th/image/heic/), [.icns](/th/image/icns/), [.ico](/th/image/ico /), [.jp2](/th/image/jp2/), [jpeg (jpg)](/th/image/jpeg/), [jpx](/th/image/jpx/), ktx, [png](/th/image/png /), [psd](/th/image/psd/), qoi, tga, tiff (tif) และ webp
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - การใช้งาน Java ของ HdrHistogram

## อ้างอิง

* [เรเดียนซ์ HDR](http://paulbourke.net/dataformats/pic/)
* [ข้อมูลภาพ](https://github.com/xiaozhuai/imageinfo )

