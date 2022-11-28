{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "ไฟล์", "นามสกุล", "รูปแบบ", "eBook", "หนังสือดิจิทัล" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ LRF และ API ที่สามารถสร้างและเปิดไฟล์ LRF",
  "title" :"รูปแบบไฟล์ LRF - ไฟล์ Sony Portable Reader",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## ไฟล์ LRF คืออะไร??

ไฟล์ที่มีนามสกุล .lrf คือไฟล์ Broad Band eBook (BBeB) ที่มีข้อมูลสำหรับ Sony BBeB รวมถึงข้อความ รูปภาพ และข้อมูลการแบ่งหน้า ไฟล์ถูกบันทึกในรูปแบบไบนารีที่บีบอัดซึ่งประกอบด้วยส่วนหัว จำนวนวัตถุที่ระบุ และดัชนีวัตถุ ไฟล์ LRF และ LRX แนบรูปแบบหนังสือ BBeB สองรูปแบบที่มีให้ ไฟล์ LRF ไม่ได้เข้ารหัสและสามารถรวบรวมได้จากไฟล์ [LRX](/th/ebook/lrf/) ไฟล์ LRF สามารถแปลงจากไฟล์ประเภทอื่นๆ รวมถึง PDF และ HTML หากคอมพิวเตอร์ของคุณไม่สามารถเปิดไฟล์ LRF แสดงว่าคุณอาจไม่ได้ติดตั้งซอฟต์แวร์เพื่อเปิดหรือแก้ไขไฟล์ LRF โปรแกรมที่สามารถเปิดไฟล์ LRF ได้แก่ Calibre, BookDesigner, Makelrf และ Canon Book Creator สำหรับ Windows, Calibre สำหรับ Linux, Calibre และ Sony Reader สำหรับ Macintosh

## ประวัติย่อ

ประเภทไฟล์ LRF เชื่อมโยงกับ Line Rider เป็นอย่างแรกและสำคัญที่สุดโดย [inXile Entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) Line Rider เป็นของเล่นฟิสิกส์ทางอินเทอร์เน็ตและถูกประดิษฐ์ขึ้นในเดือนกันยายน พ.ศ. 2549 โดย Boštjan Čadež นักศึกษามหาวิทยาลัยชาวสโลวีเนีย eBook eReaders ยี่ห้อ Sony (เช่น เครื่องอ่าน Sony PRS-500 และ Sony Librie) ใช้นามสกุลไฟล์ LRF สำหรับเอกสารและข้อความ ประเภทไฟล์ที่เป็นกรรมสิทธิ์นี้ล้าสมัยแล้ว เช่นเดียวกับไฟล์ LRS และ LRX ที่เกี่ยวข้อง ไฟล์ทั้งสามประเภทนี้ประกอบกันเป็น BroadBand eBook (BBeB) ซึ่งหยุดให้บริการในปี 2010 เมื่อ Sony เริ่มขาย ebooks ในรูปแบบ EPUB

## รูปแบบไฟล์ LRF

ดูข้อกำหนดโดยละเอียดของรูปแบบไฟล์ LRF ได้ที่ [เว็บอาร์ไคฟ์](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat) ไฟล์ LRF ประกอบด้วย:
* ส่วนหัว
* จำนวนของวัตถุ
* ดัชนีวัตถุ

ค่าทั้งหมดเหล่านี้อยู่ในลำดับของ Intel (LSB ก่อน)

### ส่วนหัว LRF

|ออฟเซ็ต (ฐานสิบหก) |ขนาด(ไบต์) |ชื่อ/ความหมาย| ค่าตัวอย่าง|
---|---|---|---|
|0 |8| ลายเซ็น LRF| 4C 00 52 00 46 00 00 00 = "LRF" ใน Unicode|
|8 |2| รุ่น?| 999 ในไฟล์ส่วนใหญ่|
|ก |2| "Psuedo-Encryption" |คีย์ไบต์ 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| จำนวนวัตถุ |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| ไม่รู้จัก| 0|
|24 |1| ธง| (16 - จากหลังไปหน้า 1 = จากหน้าไปหลัง) 16|
|25 |1| ไม่ทราบ |(ช่องว่างภายใน?) 0|
|26 |2| ไม่รู้จัก| 1600|
|28 |2| ไม่รู้จัก| (ช่องว่างภายใน?) 0|
|2A |2| ส่วนสูง?| 600|
|2C |2| ความกว้าง?| 800|
|2E |1| ไม่รู้จัก| 24|
|2F |1| ไม่ทราบ |(ช่องว่างภายใน?) 0|
|30 |0x14| ไม่รู้จัก| เลขศูนย์|
|44 |4| ID วัตถุของวัตถุ PlaneStream (0x1E) เท่านั้น| 0x0042|
|48 |4| ไม่รู้จัก |0x1536|
|4C |2| XMLCompSize| 0x035C|


## อ้างอิง

* [รูปแบบไฟล์ LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - โดย Wikipedia](https://en.wikipedia.org/wiki/BBeB)
