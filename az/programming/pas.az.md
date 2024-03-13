{
  "date": "2021-04-22",
  "keywords": [
".pas faylı",
"pas fayl formatı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS - Delphi vahidinin mənbə faylı",
  "description": "PAS faylları yarada və aça bilən PAS nümunəsi və API ilə PAS fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-azs"
}
},
  "lastmod": "2021-04-22"
}

## PAS faylı nədir?
.pas faylı əslində Delphi proqramlaşdırma layihəsində tapıla bilən mənbə kodu faylıdır. Delphi, Windows əsaslı proqram təminatı yaratmaq üçün tərtibatçılar tərəfindən istifadə edilən proqram inkişaf proqramıdır; Delfi dilində yazılmışdır. Delphi dili Object Pascal dilinin bir variantıdır. Beləliklə, Delphi kompilyatoru ilə yerli Win32 koduna tərtib edilə bilər.

## PAS fayl formatı

PAS fayl formatı Delphi vahid mənbəyi üçün qorunan kodlaşdırma faylıdır. Vahidlər Delphi proqramlarının əsas tikinti blokları kimi həyata keçirilir. Cari Delphi layihəsinin mənbə koduna **Layihə > Mənbəyə Bax** menyusu vasitəsilə baxa bilərsiniz. Proqramçılar vahidi istənilən layihənin istifadə edə biləcəyi müstəqil fayl kimi yarada və saxlaya bilərlər. Layihəyə vahid əlavə edildikdən sonra Delphi onu layihənin .DPR faylının istifadə bəndində qeyd edir.

## PAS fayl nümunəsi
Tək sətir kod yazdığımız zaman. Delphi bizim üçün çoxlu sətirləri ağıllı şəkildə yazır. Bütün mənbə kodu PAS faylında yazılmışdır. Aşağıda Delphi mənbə vahidinin və ya PAS faylının əsas nümunəsi verilmişdir:
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


## İstinadlar

 * [Delphi Layihəsi və Vahid Mənbə Fayllarını Anlamaq](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [İlk Delphi proqramınızın yazılması](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

