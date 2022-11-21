{
  "date" : "2021-06-28",
  "keywords" :[ "ไฟล์ cgi", "ไฟล์ cgi คืออะไร", "ไฟล์", "ตัวอย่าง cgi", "นามสกุลไฟล์ cgi", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CGI และ API ที่สามารถสร้างและเปิดไฟล์ CGI",
  "title" :"CGI - ไฟล์สคริปต์อินเทอร์เฟซเกตเวย์ทั่วไป",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## ไฟล์ CGI คืออะไร??
ไฟล์ CGI เรียกว่าสคริปต์ Common Gateway Interface ที่เว็บเซิร์ฟเวอร์ใช้เพื่อเรียกใช้โปรแกรมภายนอกเพื่อประมวลผลคำขอของผู้ใช้ สคริปต์ที่บันทึกไว้ในไฟล์ที่มีนามสกุล .cgi โดยทั่วไปเขียนด้วยภาษาโปรแกรม C หรือ Perl สิ่งนี้ได้รับการแนะนำตั้งแต่ยุคแรก ๆ ของเว็บ เมื่อนักพัฒนาเว็บต้องการเชื่อมต่อฐานข้อมูลกับเว็บเซิร์ฟเวอร์ของตน เซิร์ฟเวอร์ที่รองรับเกตเวย์ทั่วไประหว่างเว็บเซิร์ฟเวอร์และฐานข้อมูลนั้นเหมาะสมอย่างยิ่งที่จะดำเนินการโค้ด CGI

## รูปแบบไฟล์ CGI
เว็บเซิร์ฟเวอร์ใช้สคริปต์ CGI เพื่ออำนวยความสะดวกแก่เจ้าของในการกำหนดค่าวิธีจัดการ URL ขั้นตอนมักจะทำโดยทำเครื่องหมายไดเร็กทอรีใหม่ (ซึ่งเอกสารส่วนใหญ่ตั้งอยู่) ว่ามีสคริปต์ CGI ชื่อที่รู้จักกันทั่วไปคือ cgi-bin ตัวอย่างเช่น เลือก /usr/local/apache/htdocs/cgi-bin เป็นไดเร็กทอรี CGI บนเว็บเซิร์ฟเวอร์ เมื่อเว็บเบราว์เซอร์ร้องขอ URL ที่ชี้ไปยังไฟล์ภายในไดเร็กทอรี CGI แทนที่จะส่งไฟล์นั้น (/th/usr/local/apache/htdocs/cgi-bin/printenv.pl) ไปยังเว็บเบราว์เซอร์ HTTP เซิร์ฟเวอร์รันสคริปต์ที่ระบุและส่งคืนเอาต์พุตของสคริปต์ไปยังเว็บเบราว์เซอร์ กล่าวโดยย่อ อะไรก็ตามที่สคริปต์ CGI ถูกส่งไปยังเอาต์พุตมาตรฐานจะถูกถ่ายโอนไปยังเว็บไคลเอ็นต์แทนที่จะแสดงในเทอร์มินัลของหน้าต่าง

### ตัวอย่าง CGI

สคริปต์ CGI ต่อไปนี้เขียนด้วย Perl ซึ่งแสดงตัวแปรสภาพแวดล้อมทั้งหมดที่ส่งผ่านโดยเว็บเซิร์ฟเวอร์:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

ผลลัพธ์จะเป็นดังนี้:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## การใช้สคริปต์ CGI
ไฟล์ CGI ที่มีสคริปต์ CGI มักจะใช้เพื่อประมวลผลข้อมูลอินพุตจากผู้ใช้และสร้างข้อมูลเอาต์พุตที่เกี่ยวข้อง การใช้ Wiki เป็นหนึ่งในตัวอย่างของโปรแกรม CGI หากตัวแทนผู้ใช้ส่งคำขอชื่อรายการ เว็บเซิร์ฟเวอร์จะรันโปรแกรม CGI โปรแกรม CGI รับแหล่งที่มาของหน้ารายการนั้น แปลงเป็น HTML และพิมพ์ผลลัพธ์ เว็บเซิร์ฟเวอร์ได้รับเอาต์พุตจากโปรแกรม CGI และส่งกลับไปยังตัวแทนผู้ใช้ จากนั้น หากตัวแทนผู้ใช้เรียกใช้ฟังก์ชันแก้ไขโดยคลิกปุ่ม "แก้ไขหน้า" โปรแกรม CGI จะแสดงพื้นที่ข้อความ HTML หรือตัวควบคุมการแก้ไขอื่นๆ พร้อมเนื้อหาของหน้า สุดท้าย หากตัวแทนผู้ใช้คลิกปุ่ม "เผยแพร่เพจ" โปรแกรม CGI จะแปลง HTML ที่อัปเดตเป็นแหล่งที่มาของเพจของรายการนั้นและบันทึก



## อ้างอิง

* [อินเทอร์เฟซเกตเวย์ทั่วไป - โดย Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

