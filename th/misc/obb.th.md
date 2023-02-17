{
  "date" : "2022-02-16",
  "keywords" :[ "ไฟล์ obb", "รูปแบบไฟล์ obb", "ไฟล์ obb คืออะไร", "ไฟล์", "ตัวอย่าง obb", "นามสกุลไฟล์ obb", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ OBB - ไฟล์ Android Binary Blob ทึบ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OBB และ API ที่สามารถสร้างและเปิดไฟล์ OBB",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## ไฟล์ OBB คืออะไร??

ไฟล์ OBB เป็นไฟล์ขยายที่มีข้อมูลเพิ่มเติมนอกเหนือจากไฟล์ Android [APK](/th/compression/apk/) Google Play สโตร์ไม่อนุญาตให้มีไฟล์ Android APK ที่มีขนาดเกิน 100 MB แต่บางแอปพลิเคชันอาจต้องการกราฟิกความละเอียดสูง ไฟล์มีเดีย หรือเนื้อหาขนาดใหญ่อื่นๆ เพื่อโฮสต์นอกเหนือจากไฟล์ APK นั่นคือที่มาของประเภทไฟล์ OBB Google Play อนุญาตให้แนบไฟล์ขยายเหล่านี้เป็นส่วนเสริมของไฟล์ APK

## รูปแบบไฟล์ OBB

ไฟล์ OBB จะถูกบันทึกเป็นไฟล์ไบนารีพร้อมกับไฟล์ APK เมื่อ APK มาพร้อมกับไฟล์ OBB Google Play จะโฮสต์ไฟล์สำหรับขยายไว้บนเซิร์ฟเวอร์และไม่มีการเรียกเก็บค่าใช้จ่ายเพิ่มเติมจากนักพัฒนาซอฟต์แวร์ ไฟล์เพิ่มเติมเหล่านี้จะถูกจัดเก็บไว้ในที่จัดเก็บข้อมูลที่ใช้ร่วมกันของอุปกรณ์ในการ์ด SD หรือพาร์ติชันที่ต่อกับ USB ได้เมื่อดาวน์โหลดแอปเพื่อติดตั้ง

ไฟล์ OBB จะถูกดาวน์โหลดและติดตั้งเมื่อดาวน์โหลด แต่ในบางกรณี สิ่งเหล่านี้จะถูกดาวน์โหลดเพื่อติดตั้งเมื่อเรียกใช้แอปพลิเคชันเป็นครั้งแรก

### OBB ขนาดไฟล์สูงสุด

Google Play Store ให้คุณอัปโหลดไฟล์ขยาย OBB ขนาดสูงสุด 2 GB ไฟล์ขนาดใหญ่แนะนำให้อัปโหลดเป็นไฟล์บีบอัด [ZIP](/th/compression/zip/) เพื่อการอัปโหลดผ่านอินเทอร์เน็ตอย่างมีประสิทธิภาพ

ไฟล์สำหรับขยายเหล่านี้สามารถโฮสต์เป็นไฟล์เสริมหลัก **main** สำหรับทรัพยากรเพิ่มเติมที่แอปต้องการ หรือไฟล์เสริมสำหรับแพตช์เสริมที่มีไว้สำหรับการอัปเดตเล็กน้อยในไฟล์สำหรับขยายหลัก

## อ้างอิง

* [นักพัฒนาซอฟต์แวร์ Android - ไฟล์สำหรับขยาย](https://developer.android.com/google/play/expansion-files)
