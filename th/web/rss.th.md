{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "บางส่วน", "นามสกุล", "ไฟล์", "รูปแบบ", "เว็บ", "Really Simple Syndication", "Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - การเผยแพร่ที่ง่ายจริงๆ",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ RSS และ API ที่สามารถสร้างและเปิดไฟล์ RSS",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## ไฟล์ RSS คืออะไร? ##

ไฟล์ที่มีนามสกุล .rss เรียกว่า Really Simple Syndication RSS เป็นไฟล์ประเภทที่คอมพิวเตอร์อ่านได้ง่ายหรืออ่านง่าย ซึ่งก็คือไฟล์ XML ไฟล์ XML เหล่านี้จะได้รับการอัปเดตโดยอัตโนมัติเมื่อมีการเปลี่ยนแปลงข้อมูลหรือการอัปเดตของเว็บไซต์หรือเว็บเพจ ข้อมูลที่อัปเดตพร้อมกับข้อมูลเมตา (ชื่อผู้แต่ง ชื่อผู้เผยแพร่ วันที่เผยแพร่ ฯลฯ) และเนื้อหาเว็บอื่นๆ ของเว็บไซต์จะถูกแยกโดยไฟล์ RSS ของผู้ใช้และนำเสนอในรูปแบบที่อ่านง่าย คุณลักษณะที่ดีที่สุดของไฟล์ RSS เหล่านี้คือการทำงานแบบเรียลไทม์ และการอัปเดต ข่าวสาร การเผยแพร่ ซึ่งเป็นข้อมูลล่าสุดจะแสดงที่ด้านบนของไฟล์ เมื่อใช้ไฟล์ RSS คุณสามารถสร้างไฟล์ที่มีการอัปเดตล่าสุดของหัวข้อใดๆ ที่คุณสนใจได้อย่างง่ายดาย โดยดึงเนื้อหาที่เกี่ยวข้องจากเว็บและอ่านโดยใช้ไฟล์ RSS

## ประวัติย่อ ##

โดยเนื้อแท้แล้ว ไฟล์ RSS ถูกสร้างขึ้นครั้งแรกโดย Netscape พวกเขาได้คิดค้นเวอร์ชันแรกของไฟล์ RSS แต่เลิกล้มความคิดนั้นไป และไม่ได้ดำเนินการกับเวอร์ชันที่ใหม่กว่า ตอนนั้นเป็น **Userland Software** ที่ทำงานในรูปแบบไฟล์ RSS และยังคงสร้างสรรค์สิ่งใหม่ๆ ด้วยเวอร์ชันที่ใหม่กว่า นี่คือวิธีที่ RSS v2 เข้ามาในตลาด อย่างไรก็ตาม การประดิษฐ์ RSS สามารถเชื่อมโยงกลับไปที่ Resource Description Framework โดย Ramanathan V ในปี 1997 การทำงานของไฟล์ทั้งสองนั้นค่อนข้างคล้ายกัน และค่อนข้างปลอดภัยที่จะสันนิษฐานว่าแนวคิดของ RSS นั้นถูกสร้างขึ้นจากการทำงานของ RDF โปรแกรมอ่านไฟล์ที่ใช้ในการรวบรวมข้อมูลเมตา

## ข้อมูลจำเพาะทางเทคนิค ##

ไฟล์ RSS เป็นไฟล์ XML ประเภทหนึ่ง และไฟล์ RSS ทั้งหมดจะต้องเป็นไปตามมาตรฐานของ XML 1.0 มีไฟล์ RSS ที่แตกต่างกันหลายเวอร์ชัน เช่น 0.91, 0.92, 2.0 เป็นต้น ไฟล์ของแต่ละเวอร์ชันเป็นไปตามข้อกำหนดและมาตรฐานของเวอร์ชันนั้นๆ

## ตัวอย่าง RSS ##

ต่อไปนี้เป็นตัวอย่างของ RSS แบบง่าย

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## อ้างอิง ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
