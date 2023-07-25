{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - File Sumber Unit Delphi",
  "description":"Pelajari tentang format file PAS dengan contoh PAS dan API yang dapat membuat dan membuka file PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Apa itu file PAS?
File .pas sebenarnya adalah file kode Sumber yang dapat ditemukan di proyek pemrograman Delphi. Delphi adalah aplikasi pengembangan perangkat lunak yang digunakan oleh pengembang untuk membangun perangkat lunak berbasis Windows; ditulis dalam bahasa Delphi. Bahasa Delphi adalah varian dari bahasa Object Pascal. Sehingga dapat dikompilasi menjadi kode asli Win32 dengan kompiler Delphi.

## format file PAS

Format file PAS adalah file pengkodean yang dicadangkan untuk sumber unit Delphi. Unit direalisasikan sebagai blok bangunan utama aplikasi Delphi. Anda dapat melihat kode sumber proyek Delphi saat ini melalui menu **Project > View Source**. Pemrogram dapat membuat dan menyimpan unit sebagai file yang berdiri sendiri yang dapat digunakan oleh proyek apa pun. Setelah unit ditambahkan ke proyek, Delphi mendaftarkannya di klausa penggunaan file .DPR proyek.

## contoh file PAS
Saat kita menulis satu baris kode. Delphi menulis banyak baris untuk kita dengan cerdas. Semua kode sumber ditulis dalam file PAS. Berikut adalah contoh dasar unit sumber Delphi atau file PAS:
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


## Referensi

* [Memahami Proyek Delphi dan File Sumber Unit](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Menulis program Delphi pertama Anda](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

