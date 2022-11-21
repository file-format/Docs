{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ซอร์สโค้ด M - Matlab",
  "description":"เรียนรู้เกี่ยวกับไฟล์ซอร์สโค้ด Matlab .m และ API ที่สามารถสร้างและเปิดไฟล์ MF",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - ไฟล์ซอร์สโค้ด Matlab

## ไฟล์ M (Matlab) คืออะไร?

ไฟล์ที่มีนามสกุล .m คือไฟล์ซอร์สโค้ดที่ใช้โดย Matlab ซึ่งเป็นแพลตฟอร์มการเขียนโปรแกรมและการคำนวณเชิงตัวเลขที่ใช้สำหรับการวิเคราะห์ การพัฒนาอัลกอริทึม และการสร้างแบบจำลองการจำลอง เช่นเดียวกับรูปแบบไฟล์การเขียนโปรแกรมอื่นๆ ไฟล์ M มีซอร์สโค้ดที่รันคำสั่ง Matlab เพื่อลงจุดกราฟ รันการจำลอง และการดำเนินการทางคณิตศาสตร์อื่นๆ การจำลอง Matlab เดียวสามารถครอบคลุมไฟล์ .m หลายไฟล์ที่สามารถจัดประเภทแอปพลิเคชันในสคริปต์ คลาส ฟังก์ชัน หรือการประกาศ ไฟล์ Matlab M สามารถเปิดได้ด้วยโปรแกรมแก้ไขข้อความ

## รูปแบบไฟล์ Matlab M - ข้อมูลเพิ่มเติม

ไฟล์ Matlab .m เป็นไฟล์ข้อความที่มีรหัสโปรแกรมในภาษาโปรแกรม Matlab สิ่งเหล่านี้สามารถเปิดและแก้ไขได้ในโปรแกรมแก้ไขข้อความใดๆ และบันทึกกลับเพื่อดำเนินการในซอฟต์แวร์ Matlab Matlab เองมี Live Editor ที่ใช้สำหรับสร้างสคริปต์ที่ผสมผสานระหว่างโค้ด เอาต์พุต และข้อความที่จัดรูปแบบ

### ไฟล์ฟังก์ชัน Matlab

เช่นเดียวกับภาษาการเขียนโปรแกรมอื่นๆ คุณสามารถสร้างไฟล์ .m ที่มีเฉพาะคำจำกัดความของฟังก์ชันที่ทำงานเฉพาะอย่างเท่านั้น ไฟล์ดังกล่าวจะถูกบันทึกด้วยนามสกุล .m และใช้ฟังก์ชันที่เกี่ยวข้องกับฟังก์ชันนั้นเท่านั้น

### ตัวอย่างไฟล์ .M

ต่อไปนี้คือตัวอย่างไฟล์ฟังก์ชัน Matlab ที่คำนวณเวลาที่ใช้สำหรับวัตถุที่หล่นลงมาจากความสูง h

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

หากต้องการเรียกใช้ฟังก์ชันนี้จากโปรแกรมแก้ไข Matlab หรือจากไฟล์ .m อื่น สามารถใช้โค้ดต่อไปนี้ได้
```C++
TimeToGround(100)
```

## อ้างอิง

* [Matlab - รูปแบบไฟล์ที่รองรับ](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [การใช้ Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - ไฟล์การใช้งาน Objective-C

## ไฟล์ M (Objective-C) คืออะไร?

ไฟล์ M ยังหมายถึงไฟล์การใช้งานที่มีซอร์สโค้ดของคลาสที่เขียนด้วยภาษา Objective-C ซึ่งเป็นภาษาโปรแกรมที่ใช้ในการเขียนแอปพลิเคชันซอฟต์แวร์สำหรับ OS X และ iOS Objective-C เป็นภาษาโปรแกรมหลักที่ใช้โดย API หลักของ Apple, Cocoa และ Cocoa Touch สำหรับแพลตฟอร์มเหล่านี้ แอปพลิเคชันซอฟต์แวร์เดียวที่พัฒนาในภาษานี้อาจมีไฟล์ .m หลายไฟล์ ซึ่งมีการใช้งานคลาสของโปรแกรม สามารถเปิดได้โดยใช้ Apple XCode, jEdit และโปรแกรมแก้ไขข้อความทั่วไปอื่นๆ

## รูปแบบไฟล์ Objective-CM - ข้อมูลเพิ่มเติม

ไฟล์ M ถูกเขียนในรูปแบบข้อความธรรมดาโดยใช้ไวยากรณ์การเขียนโปรแกรมของ Objective-C ทุกเมธอดของคลาสต้องถูกกำหนดด้วยรหัสที่จำเป็นทั้งหมดในไฟล์การใช้งานเหล่านี้ ไฟล์ M การใช้งานเหล่านี้สามารถนำเข้าไฟล์ส่วนหัว .h ตั้งแต่หนึ่งไฟล์ขึ้นไปตามความต้องการ คำสั่งการนำเข้าจะบอกคอมไพเลอร์ว่าจะค้นหาไฟล์ส่วนหัวที่เป็นของไฟล์การใช้งานนี้ได้จากที่ใด คำชี้แจงการนำเข้าเขียนดังนี้

```C++
#import "network.h"
```

การใช้งานไฟล์ M แต่ละไฟล์จะเริ่มต้นด้วยคำสั่ง `@implementation` ตามด้วยชื่อไฟล์คลาสการใช้งาน ตามด้วยการดำเนินการตามวิธีการทั้งหมดที่ประกาศไว้ในไฟล์ส่วนหัว

### ตัวอย่างรูปแบบไฟล์ M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## อ้างอิง
* [เกี่ยวกับวัตถุประสงค์ C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [คู่มือ Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

