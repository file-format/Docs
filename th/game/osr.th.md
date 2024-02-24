{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OSR และ API ที่สามารถสร้างและเปิดไฟล์ OSR",
  "title" : "ไฟล์ OSR - osu! รูปแบบไฟล์เล่นซ้ำ",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-th",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## ไฟล์ OSR คืออะไร??

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**ประเภท MIME ของรูปแบบไฟล์ OSR:** x-osu-replay

## รูปแบบไฟล์ OSR

ไฟล์ OSR จะถูกบันทึกเป็นไฟล์ไบนารีพร้อมช่องข้อมูลคงที่และความยาวผันแปรได้

|ชนิดข้อมูล| รูปแบบ|
---|---|
|ไบต์ |โหมดเกมของรีเพลย์ (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|จำนวนเต็ม |เวอร์ชันของเกมเมื่อมีการสร้างการเล่นซ้ำ (เช่น 20131216)|
|สตริง |osu! บีทแมป MD5 แฮช |
|สตริง| ชื่อผู้เล่น|
|สตริง| โอสึ! เล่นซ้ำแฮช MD5 (รวมถึงคุณสมบัติบางอย่างของการเล่นซ้ำ) |
|สั้น| จำนวน 300s|
|สั้น| จำนวน 100 ในมาตรฐาน, 150 ใน Taiko, 100 ใน CTB, 100 ใน Mania|
|สั้น| จำนวน 50 ในมาตรฐาน ผลไม้ลูกเล็กใน CTB และ 50 ในความบ้าคลั่ง|
|สั้น| จำนวน Gekis ในมาตรฐาน สูงสุด 300 วินาทีในความบ้าคลั่ง|
|สั้น| จำนวน Katus ในมาตรฐาน 200 วินาทีในความบ้าคลั่ง|
|สั้น| จำนวนครั้งที่พลาด|
|จำนวนเต็ม| คะแนนรวมที่แสดงในรายงานคะแนน|
|สั้น| คอมโบที่ยิ่งใหญ่ที่สุดที่แสดงในรายงานคะแนน|
|ไบต์| คอมโบที่สมบูรณ์แบบ/เต็มรูปแบบ (1 = ไม่พลาด และไม่มีตัวเลื่อนพัง และไม่มีตัวเลื่อนที่ทำเสร็จเร็ว)|
|จำนวนเต็ม| โมเดอเรเตอร์ที่ใช้ ดูรายการค่า mod ด้านล่าง|
|สตริง| กราฟแท่งชีวิต: คู่ที่คั่นด้วยเครื่องหมายจุลภาค u/v โดยที่ u คือเวลาในหน่วยมิลลิวินาทีของเพลง และ v คือค่าทศนิยมจาก 0 - 1 ซึ่งแสดงถึงจำนวนชีวิตที่คุณมีอยู่ในช่วงเวลาที่กำหนด (0 = แถบชีวิตคือ ว่างเปล่า 1= แถบชีวิตเต็ม)|
|ยาว| การประทับเวลา (เครื่องหมาย Windows)|
|จำนวนเต็ม| ความยาวเป็นไบต์ของข้อมูลเล่นซ้ำที่บีบอัด|
|ไบต์ |ข้อมูลการเล่นซ้ำแบบบีบอัดอาร์เรย์|
|ยาว| รหัสคะแนนออนไลน์|
|สองเท่า| ข้อมูลม็อดเพิ่มเติม แสดงเฉพาะเมื่อเปิดใช้งาน Target Practice เท่านั้น|

## อ้างอิง

* [โอสึ! เกมจับจังหวะ](https://osu.ppy.sh/home)

* [รูปแบบไฟล์ OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


