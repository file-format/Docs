{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - ไฟล์ต้นฉบับหน่วย Delphi",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PAS พร้อมตัวอย่าง PAS และ API ที่สามารถสร้างและเปิดไฟล์ PAS",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## ไฟล์ PAS คืออะไร??
ไฟล์ .pas เป็นไฟล์ซอร์สโค้ดซึ่งสามารถพบได้ในโครงการเขียนโปรแกรม Delphi Delphi เป็นแอปพลิเคชั่นพัฒนาซอฟต์แวร์ที่นักพัฒนาใช้สำหรับสร้างซอฟต์แวร์ที่ใช้ Windows; เขียนด้วยภาษาเดลฟี ภาษา Delphi เป็นตัวแปรของภาษา Object Pascal ดังนั้นจึงสามารถรวบรวมเป็นรหัส Win32 ดั้งเดิมด้วยคอมไพเลอร์ Delphi

## รูปแบบไฟล์ PAS

รูปแบบไฟล์ PAS เป็นไฟล์เข้ารหัสซึ่งสงวนไว้สำหรับหน่วยต้นทางของ Delphi หน่วยต่างๆ ได้รับการยอมรับว่าเป็นหน่วยการสร้างหลักของแอพ Delphi คุณสามารถดูซอร์สโค้ดของโครงการ Delphi ปัจจุบันผ่านเมนู **โครงการ > ดูแหล่งที่มา** โปรแกรมเมอร์สามารถสร้างและบันทึกหน่วยเป็นไฟล์แบบสแตนด์อโลนที่โครงการใด ๆ สามารถใช้ได้ เมื่อเพิ่มยูนิตในโครงการแล้ว Delphi จะลงทะเบียนยูนิตนั้นในส่วนคำสั่งการใช้งานของไฟล์ .DPR ของโครงการ

## ตัวอย่างไฟล์ PAS
เมื่อเราเขียนโค้ดเพียงบรรทัดเดียว เดลฟีเขียนหลายบรรทัดให้เราอย่างชาญฉลาด ซอร์สโค้ดทั้งหมดเขียนด้วยไฟล์ PAS ต่อไปนี้เป็นตัวอย่างพื้นฐานของหน่วยต้นทาง Delphi หรือไฟล์ PAS:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## อ้างอิง

* [ทำความเข้าใจโครงการ Delphi และไฟล์ต้นฉบับของหน่วย](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [การเขียนโปรแกรม Delphi ครั้งแรกของคุณ](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

