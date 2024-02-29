{
  "date": "2021-04-22",
  "keywords": [
"فایل .pas",
"فرمت فایل pas",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS - فایل منبع واحد دلفی",
  "description": "با نمونه PAS و APIهایی که می توانند فایل های PAS را ایجاد و باز کنند، درباره قالب فایل PAS بیاموزید.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-fas"
}
},
  "lastmod": "2021-04-22"
}

## فایل PAS چیست؟
فایل .pas در واقع یک فایل کد منبع است که در پروژه برنامه نویسی دلفی یافت می شود. دلفی یک برنامه توسعه نرم افزار است که توسط توسعه دهندگان برای ساخت نرم افزارهای مبتنی بر ویندوز استفاده می شود. به زبان دلفی نوشته شده است. زبان دلفی نوعی از زبان Object Pascal است. بنابراین می توان آن را با کامپایلر دلفی در کد Win32 بومی کامپایل کرد.

## فرمت فایل PAS

فرمت فایل PAS یک فایل کدگذاری است که برای منبع واحد دلفی رزرو شده است. واحدها به عنوان بلوک های اصلی سازنده برنامه های دلفی شناخته می شوند. می توانید کد منبع پروژه فعلی دلفی را از طریق منوی **پروژه > مشاهده منبع** مشاهده کنید. برنامه نویسان می توانند یک واحد را به عنوان یک فایل مستقل ایجاد و ذخیره کنند که هر پروژه می تواند از آن استفاده کند. هنگامی که یک واحد به پروژه اضافه می شود، دلفی آن را در قسمت use های فایل .DPR پروژه ثبت می کند.

## نمونه فایل PAS
وقتی یک خط کد می نویسیم. دلفی خطوط زیادی را برای ما هوشمندانه می نویسد. تمام کد منبع در فایل PAS نوشته شده است. در زیر یک مثال اساسی از واحد منبع دلفی یا فایل PAS آمده است:
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


## منابع

 * [درک پروژه دلفی و فایل‌های منبع واحد](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [نوشتن اولین برنامه دلفی شما](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

