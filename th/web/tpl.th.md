{
  "date" : "2019-10-11",
  "keywords" :[ "tpl","ไฟล์ tpl", "รูปแบบไฟล์ tpl", "ประเภทไฟล์ tpl", "ไฟล์", "ประเภท", "ไฟล์ tpl คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPL - เทมเพลตเซิร์ฟเวอร์ไฟล์ HTTP",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ TPL และ API ในการสร้างและเปิดไฟล์ TPL คืออะไร",
  "linktitle" : "TPL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## ไฟล์ TPL คืออะไร??

ไฟล์ที่มีนามสกุล .tpl เป็นไฟล์เทมเพลตที่สร้างและใช้โดย HTTP File Server (HFS) ซึ่งเป็นโปรแกรมแอปพลิเคชันแชร์ไฟล์เพื่อส่งและรับไฟล์ผ่านเทคโนโลยีเว็บ HTTP แทนโปรโตคอล FTP ใช้ในการสร้างหน้า [HTML](/th/web/html/) แบบไดนามิกตามข้อมูลเทมเพลตที่กำหนดให้มีการตั้งค่าที่มีเค้าโครง สไตล์ และสคริปต์ที่คล้ายกัน แอปพลิเคชันที่ต้องการการตั้งค่าเดียวกันสามารถกำหนดไฟล์เทมเพลตเดียวกันได้ และ HFS จะส่งคืนเพจที่ร้องขอแบบไดนามิกบนรันไทม์ตามไฟล์เทมเพลตนี้


## รูปแบบไฟล์ TPL

ไฟล์ TPL ถูกจัดเก็บในรูปแบบที่มนุษย์อ่านได้และมี HTML ซึ่งเป็นภาษามาร์กอัปที่มนุษย์อ่านได้ นอกจาก HTML แล้ว ไฟล์ TPL ยังอาจมี CSS ระดับเทมเพลตและ Javascript เพื่อกำหนดเลย์เอาต์และการดำเนินการที่จะดำเนินการโดยเพจทั้งหมดที่สร้างจากไฟล์เทมเพลตนี้

### ส่วน TPL

ส่วน TPL มีโค้ด HTML, CSS หรือ JavaScript ที่ใช้โดย HFS ขณะสร้างหน้าเอาต์พุต แต่ละส่วนเริ่มต้นด้วยวงเล็บเหลี่ยม ([]) และกำหนดด้วยเครื่องหมายเปอร์เซ็นต์ (%) ไฟล์ TPL อาจมีส่วนต่อไปนี้

#### ส่วนสไตล์ TPL

รวมถึงข้อมูลที่เกี่ยวข้องกับสไตล์ที่อาจใช้หรือไม่ใช้การอ้างอิงไฟล์ CSS ที่ฝังอยู่ ตัวอย่างของส่วนสไตล์มีดังนี้

```
[style]
.row { color: #666 }
span.size_file { font-size:10px; color:#666 }
.button, .big, .little, th { font-weight:normal; font-size:9pt; color:#222; }
#back { background:#222;border:1px solid #000;padding:5px;margin-top:10px;}
.little { font-size: 8pt; color:#2F4F4F;margin-top:10px; }
.path_title { color: #999;margin-top:10px; },
img { border-style:none }
.row { background:#f8f8f8;}
.row a { text-decoration:none; }
.comment { font-size:7pt; color:#666; background:#f3f3f3; padding:3px; border:1px solid #ccc; margin-top:2px; }
.column { color:#222; font-size:13pt; font-weight:bold; padding-bottom:0; }
.flag { font-weight:bold; font-size:8pt; background:#fff; color:#990000; text-align:center; border:1px solid #ff0000; }
.text { color:#222; }
span.desc { color: #999; }
#everything { margin-top:20px;border-top:1px solid #ccc;padding-top:10px; }
html {
font-size: 62.5%;
}
body {margin:0px; padding:0px; background-color:#fff; color:#222; font-family:"Lucida Grande", "Tahoma", "Helvetica", "Arial", sans-serif; font-size:120%;quotes:"\201C" "\201E" "\2018" "\2019";}
table, tr, td {font-size: inherit;}
a:link {color: #222;}
a:visited {color: #666;}
a:hover {	color: #000;}
a:active {}
a:focus {}
img, a img {border: none;}
#path {color: #333;background-color: #f8f8f8; border-bottom: 1px solid #ccc;padding: 3px 8px;margin: 0px;}
#path li {display: inline;padding-left: 13px; padding-right: 3px; background-image: url(arrow.gif);background-repeat: no-repeat;background-position: 1px 5px;}
#path span {font-weight: bold;}
#header {margin: 24px 48px;}
#header h1 {font-size: 250%;color: #222;  margin: 0;margin-bottom: 6px;}
#header h2 {font-size: 120%;color: #aaa;  margin: 0;}
#content { margin: 24px 48px;}
#footer {    margin-top: 48px;    border-top: 1px solid #ccc;    padding: 6px;    text-align: center;    color: #888;    font-size: 80%;}
#footer a {color: #888;}
```

#### ส่วนลิงค์ TPL

ส่วนลิงก์ประกอบด้วยข้อมูลเกี่ยวกับ URL และสามารถรวมการอ้างอิงถึงเหตุการณ์ต่างๆ เช่น ปุ่มและการดำเนินการ

```
[login-link]
<li><a href="%encoded-folder%~login" class=buttonx>Login</a></li>
[loggedin]
<li><a href="#" class=buttonx>Logged in as: %user%</a></li>
```

#### ส่วนความคิดเห็น

ส่วนความคิดเห็นของ TPL รวมไว้สำหรับสร้างความคิดเห็นและกำหนดไว้ดังต่อไปนี้
```
[comment]
<div class=comment>%item-comment%</div>
```

#### ส่วนการอัปโหลด

ส่วนการอัปโหลดจะส่งคืนการตอบสนอง HTML จริงจากเซิร์ฟเวอร์ตามการตั้งค่าเทมเพลตตามที่แสดงในตัวอย่างต่อไปนี้

```
[upload]
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<html><head>
<title>myHFS</title>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
<style type="text/css">\n%style%\n</style>
</head>
<body>
<ul id=path>
<li><strong>Folder:</strong> <a href="/">root</a>%folder%</li>
</ul>
<div id=header>
<h1>myHFS</h1>
<h2>Final HFS Template Framework for Ishare USM Community</h2>
</div>
<div id=content>

<h3>myHFS Rules</h3>
<p>I'm sharing stuffs unpaid, so please respect me by understanding these rules: </p>
<ul class="contacts">
<li>Sorry if your downloading activity was suddenly interrupted/disconnected. It might be due to some technical problems.</li>
<li>Be nice. Don't use IDM or any download manager program with many connections. Set it to 1 or you will be banned from my server.</li>
<li>Anything I shared here is the right of my freedom. Good or bad, the decision is in your hands. I'm not be responsible for any consequences.</li>
</ul>
<p class=credit>Sharing among my university fellows is an unique culture here, in Engineering Campus, USM. Sharing via LAN by using HFS software is the best underground activity for everyone. Sharing is loving!</p>
</div>

</body></html>
```

## อ้างอิง

* [HFS](https://www.rejetto.com/wiki/index.php/การปรับแต่ง)
* [ตัวอย่าง TPL - Github](https://github.com/heiswayi/hfs-templates/blob/master/HFSTemplate_myHFS.tpl)

