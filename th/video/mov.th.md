{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ mov", "รูปแบบไฟล์ mov", "ไฟล์ mov คืออะไร", "ไฟล์", "ตัวอย่าง mov", "นามสกุลไฟล์ mov", "ส่วนขยาย", "รูปแบบ", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ MOV - รูปแบบไฟล์ภาพยนตร์ Apple QuickTime",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MOV และ API ที่สามารถสร้างและเปิดไฟล์ MOV",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## ไฟล์ MOV คืออะไร??

ไฟล์ MOV เป็นประเภทไฟล์วิดีโอที่พัฒนาโดย Apple Inc. ซึ่งมีอย่างน้อยหนึ่งแทร็ก แต่ละแทร็กจัดเก็บภาพยนตร์ เสียง คลิปภาพยนตร์ และคำบรรยาย เป็นคอนเทนเนอร์มัลติมีเดียที่สามารถจัดเก็บองค์ประกอบสื่อประเภทต่างๆ รูปแบบวิดีโอ MOV เข้ากันได้กับทั้งระบบ Windows และ Macintosh มันใช้รหัส MPEG-4 สำหรับการบีบอัดและติดตามในวัตถุที่เรียกว่าอะตอมซึ่งอยู่ในโครงสร้างข้อมูลแบบลำดับชั้น

## ประวัติโดยย่อของรูปแบบไฟล์ MOV

รูปแบบไฟล์ MPEG-4 พัฒนามาจากข้อกำหนดรูปแบบไฟล์ QuickTime (**QTFF**) ในปี 2544 องค์การมาตรฐานระหว่างประเทศได้อนุมัติรูปแบบและข้อกำหนดระบบ MPEG-4 ส่วนที่ 1 ได้รับการเผยแพร่ในปี 2542 ในปี 2544 ไฟล์แก้ไข เผยแพร่รูปแบบ [MP4](/th/video/mp4/) แล้ว

เวอร์ชันแรกของ MP4 ได้รับการแก้ไขในปี 2546 เป็น MPEG-4 ส่วนที่ 14 (ISO/IEC 14496-14:2003) ในปี พ.ศ. 2547 MP4 ได้รับการทำให้เป็นแบบทั่วไปเพื่อกำหนดโครงสร้างทั่วไปสำหรับไฟล์มีเดียตามเวลาทั้งหมด ดังนั้นตอนนี้จึงใช้เป็นพื้นฐานสำหรับรูปแบบไฟล์มัลติมีเดียอื่น ๆ

## รูปแบบไฟล์ QuickTime (QTFF) - ข้อมูลเพิ่มเติม

ในการทำงานกับมัลติมีเดียดิจิทัล QTFF สามารถเก็บข้อมูลได้หลายประเภท เป็นรูปแบบแนวคิดในการแลกเปลี่ยนสื่อดิจิทัล เนื่องจากรูปแบบดังกล่าวกำหนดมาตรฐานในการอธิบายโครงสร้างสื่อประเภทต่างๆ รูปแบบไฟล์ประกอบด้วยคอลเลกชันที่ยืดหยุ่นของวัตถุเชิงวัตถุ สำหรับการจัดเก็บภาพยนตร์บนดิสก์ QuickTime ใช้สองโครงสร้าง ได้แก่ 'อะตอม' และ 'QT อะตอม'

### อะตอม

Atom เป็นหน่วยพื้นฐานของไฟล์ QuickTime มีสองฟิลด์หลักในอะตอมใด ๆ ก่อนฟิลด์อื่น: ฟิลด์ขนาดและประเภท ช่องขนาดแสดงขนาดของอะตอมในขณะที่ช่องประเภทระบุประเภทของข้อมูลที่จัดเก็บไว้ในอะตอม โดยธรรมชาติแล้ว อะตอมมีลักษณะเป็นลำดับชั้น ซึ่งหมายความว่าอะตอมหนึ่งสามารถบรรจุอะตอมอื่นๆ ได้ ซึ่งยังคงมีอะตอมอื่นๆ เค้าโครงของอะตอมตัวอย่างแสดงในรูปภาพต่อไปนี้

แต่ละอะตอมมีสองส่วน 'ส่วนหัว' และ 'ข้อมูล' ส่วนหัวประกอบด้วยฟิลด์ขนาดและประเภท และส่วนข้อมูลประกอบด้วยข้อมูลจริง นอกจากนี้ แต่ละฟิลด์มีคำอธิบายด้านล่าง:

### ขนาดอะตอม

ส่วนหัวและเนื้อหาของอะตอมระบุด้วยจำนวนเต็ม 32 บิตซึ่งเรียกว่าขนาดของอะตอม ฟิลด์ขนาดประกอบด้วยขนาดของอะตอมเป็นไบต์ ซึ่งแสดงเป็นจำนวนเต็มที่ไม่มีเครื่องหมาย 32 บิต

### ประเภทอะตอม

ประเภทของอะตอมยังแสดงด้วยจำนวนเต็ม 32 บิต ซึ่งส่วนใหญ่ถือเป็นฟิลด์สี่อักขระที่มีค่า knemonic เช่น 'moov' (0x6D6F6F76) สำหรับอะตอมภาพยนตร์ หรือ 'trak' (0x7472616B) สำหรับ ติดตามอะตอม เมื่อทราบชนิดของอะตอมแล้ว ก็จะอนุญาตให้ตีความข้อมูลได้

### QT Atoms และ Atom Containers

อะตอมของ QT เป็นรูปแบบการจัดเก็บสำหรับวัตถุประสงค์ทั่วไปและมีส่วนหัวเพิ่มเติมซึ่งประกอบด้วยฟิลด์ขนาด, ชนิด, รหัสอะตอม และจำนวนอะตอมลูก อะตอมของ QT ถูกห่อหุ้มไว้ในคอนเทนเนอร์อะตอม ซึ่งเป็นโครงสร้างข้อมูลเฉพาะที่มีส่วนหัวพร้อมจำนวนล็อค มีหนึ่งรูทอะตอมในแต่ละคอนเทนเนอร์อะตอมซึ่งเป็นอะตอม QT เค้าโครงของอะตอม QT แสดงในรูปด้านล่าง

ส่วนหัวของคอนเทนเนอร์อะตอม QT มีข้อมูลต่อไปนี้:

สงวนไว้: องค์ประกอบ 10 ไบต์ที่มีค่า 0

จำนวนล็อค: จำนวนเต็ม 16 บิตที่มีค่า 0

ส่วนหัวของอะตอม QT มีข้อมูลต่อไปนี้:

**ขนาด -** ส่วนหัวและเนื้อหาของอะตอม QT ระบุเป็นไบต์ด้วยจำนวนเต็ม 32 บิต ในกรณีของลีฟอะตอม ฟิลด์นี้จะมีขนาดของอะตอมเดี่ยว

**ประเภท -** ประเภทของอะตอมระบุด้วยจำนวนเต็ม 32 บิต ในกรณีที่เป็น root atom ค่าจะถูกตั้งค่าเป็น 'sean'

**Atom ID -** เป็นจำนวนเต็ม 32 บิตที่แสดง Atom ID และต้องไม่ซ้ำกันสำหรับพี่น้องทั้งหมด รูทอะตอมมีค่าของอะตอม ID เป็น 1 เสมอ

**สงวนไว้ -** จำนวนเต็ม 16 บิตที่ต้องตั้งค่าเป็น 0

**จำนวนลูก -** จำนวนเต็ม 16 บิตที่ระบุจำนวนอะตอมลูกของอะตอม

**สงวนไว้ -** จำนวนเต็ม 32 บิตที่ต้องตั้งค่าเป็น 0

## โครงสร้างไฟล์ของไฟล์ MOV

ไฟล์ MOV ประกอบด้วยส่วนที่ต่อเนื่องกัน ทุกอันมีส่วนหัว 8 ไบต์: ขนาดอัน 4 ไบต์ (big-endian, ไบต์สูงก่อน) และประเภทอัน 4 ไบต์ - หนึ่งในลายเซ็นที่กำหนดไว้ล่วงหน้า: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "กว้าง", "load", "ctab", "imap", "matt", "kmat", "คลิป", "crgn", "ซิงค์", "แชป", "tmcd", "scpt", "ssrc", "PICT" อันแรกเป็นประเภท "ftype" และมีประเภทย่อยที่ออฟเซ็ต 8 MOV กำหนดโดยประเภทย่อยซึ่งต้องเป็น "qt" ในการเขียนไฟล์ MOV จำเป็นต้องมีการวนซ้ำจนกว่าจะตรวจพบประเภทที่ไม่รู้จัก

นี่คือ `ตัวอย่างตัวอย่าง`: การตรวจสอบข้อมูลไบนารีของไฟล์ MOV ตัวอย่าง เห็นได้ชัดว่าเริ่มต้นด้วยลายเซ็น **ftyp** (ฐานสิบหก: 66 74 79 70) ที่ออฟเซ็ต 4 ซึ่งกำหนดประเภทไฟล์คอนเทนเนอร์ QuickTime ประเภทย่อยของไฟล์คือ **qt~_~_** (ฐานสิบหก: 71 74 20 20) ซึ่งชี้ไปที่ประเภทไฟล์ MOV ขนาดบล็อกแรกคือ 32 (hex: 00 00 00 20, big-endian, high byte ก่อน) ขนาดอยู่ที่ offset 0 ที่ offset 32 (hex: 20) จะอยู่ที่ chunk ที่สองซึ่งมีขนาด 8 และ พิมพ์ **mdat** (ฐานสิบหก: 6D 64 61 74)

ชิ้นถัดไปอยู่ที่ออฟเซ็ต 32+8#40 (ฐานสิบหก: 28) และมีขนาด 3,263,028 (ฐานสิบหก: 00 31 CA 34) และพิมพ์ **mdat** (ฐานสิบหก: 6D 64 61 74) ที่ออฟเซ็ต 44 (ฐานสิบหก : 2ค). ชิ้นถัดไปอยู่ที่ออฟเซ็ต 40 + 3,263,028#3,263,068 (ฐานสิบหก: 00 31 CA 5C) และมีขนาด 21,189 (ฐานสิบหก: 00 00 52 C5) และพิมพ์ **moov** (ฐานสิบหก: 6D 6F 6F 76) ที่ออฟเซ็ต 1,836,019,574 (ฐานสิบหก: 00 31 CA 60) นี่เป็นก้อนสุดท้าย ดังนั้นขนาดไฟล์ทั้งหมดคือ 3,263,068+21,189#3,284,257 ไบต์

## วิธีการแปลงไฟล์ MOV?

มีเครื่องเล่นมีเดียและโปรแกรมตัดต่อวิดีโอมากมายที่สามารถแปลงไฟล์ MOV เป็นรูปแบบไฟล์วิดีโอยอดนิยมอื่น ๆ ได้ เครื่องเล่นมีเดียบางตัวที่สามารถแปลงไฟล์ MOV เป็นรูปแบบอื่นได้ ได้แก่:

* เครื่องเล่นสื่อ VideoLAN VLC
* เครื่องเล่น Eltima Elmedia

เครื่องเล่นสื่อและโปรแกรมตัดต่อวิดีโอหลายรายการ รวมถึงเครื่องเล่นสื่อ VideoLAN VLC และ Eltima Elmedia Player สามารถแปลงไฟล์ MOV เป็นรูปแบบอื่นได้ ซอฟต์แวร์เหล่านี้สามารถแปลงไฟล์ MOV เป็นรูปแบบวิดีโอต่อไปนี้

* วิดีโอ MPEG-4 - [MP4](/th/วิดีโอ/mp4/)
* วิดีโอ WebM - [เว็บเอ็ม](/th/วิดีโอ/webm/)
* Video Transport Stream - [TS](/th/วิดีโอ/ts/)
* รูปแบบระบบขั้นสูง - [ASF](/th/video/ts/)
* เสียง Ogg Vorbis - [OGG](/th/เสียง/ogg/)
* เสียง MP3 - [MP3](/th/เสียง/mp3/)
* ตัวแปลงสัญญาณเสียงแบบไม่สูญเสียฟรี - [FLAC](/th/audio/flac/)
* เสียงคลื่น - [WAV](/th/เสียง/wav/)

## Open Source API สำหรับไฟล์ MOV

* [ตอบสนอง Native API เพื่อแปลง MOV เป็น MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API เพื่อซ่อมแซมไฟล์ MOV](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API เพื่อแปลง MOV เป็น GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## อ้างอิง

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)
