{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Tệp nguồn đơn vị Delphi",
  "description":"Tìm hiểu về định dạng tệp PAS với ví dụ về PAS và các API có thể tạo và mở tệp PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Tệp PAS là gì?
Tệp .pas thực sự là tệp Mã nguồn có thể tìm thấy trong dự án lập trình Delphi. Delphi là một ứng dụng phát triển phần mềm được các nhà phát triển sử dụng để xây dựng phần mềm dựa trên Windows; được viết bằng ngôn ngữ Delphi. Ngôn ngữ Delphi là một biến thể của ngôn ngữ Object Pascal. Vì vậy, nó có thể được biên dịch thành mã Win32 gốc bằng trình biên dịch Delphi.

## Định dạng tệp PAS

Định dạng tệp PAS là tệp mã hóa dành riêng cho nguồn đơn vị Delphi. Các đơn vị được coi là khối xây dựng chính của ứng dụng Delphi. Bạn có thể xem mã nguồn của dự án Delphi hiện tại thông qua menu **Dự án > Xem nguồn**. Các lập trình viên có thể tạo và lưu một đơn vị dưới dạng một tệp độc lập mà bất kỳ dự án nào cũng có thể sử dụng. Khi một đơn vị được thêm vào dự án, Delphi sẽ đăng ký nó trong mệnh đề sử dụng của tệp .DPR của dự án.

## Ví dụ về tệp PAS
Khi chúng ta viết một dòng mã. Delphi viết nhiều dòng cho chúng tôi một cách thông minh. Tất cả mã nguồn được viết trong tệp PAS. Sau đây là một ví dụ cơ bản về đơn vị nguồn Delphi hoặc tệp PAS:
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


## Người giới thiệu

* [Tìm hiểu tệp nguồn đơn vị và dự án Delphi](https://www.thoughtco.com/under Hiểu-delphi-project-files-dpr-1057652)
* [Viết chương trình Delphi đầu tiên của bạn](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

