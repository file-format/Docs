{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Delphi Birim Kaynak Dosyası",
  "description":"PAS örneği ve PAS dosyaları oluşturabilen ve açabilen API'ler ile PAS dosya formatı hakkında bilgi edinin.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## .pas dosyası nedir?
.pas dosyası aslında bir Delphi programlama projesinde bulunabilen bir Kaynak kod dosyasıdır. Delphi, geliştiriciler tarafından Windows tabanlı yazılımlar oluşturmak için kullanılan bir yazılım geliştirme uygulamasıdır; Delphi dilinde yazılmıştır. Delphi dili, Object Pascal dilinin bir çeşididir. Böylece Delphi derleyicisi ile yerel Win32 koduna derlenebilir.

## PAS dosya formatı

PAS dosya formatı, Delphi birim kaynağı için ayrılmış bir kodlama dosyasıdır. Birimler, Delphi uygulamalarının ana yapı taşları olarak gerçekleştirilir. Geçerli Delphi projesinin kaynak kodunu **Proje > Kaynağı Görüntüle** menüsünden görüntüleyebilirsiniz. Programcılar, herhangi bir projenin kullanabileceği bağımsız bir dosya olarak bir birim oluşturabilir ve kaydedebilir. Projeye bir birim eklendiğinde, Delphi bunu proje .DPR dosyasının kullanımlar yan tümcesine kaydeder.

## PAS dosyası örneği
Tek satır kod yazdığımızda. Delphi bizim için akıllıca birçok satır yazar. Tüm kaynak kodu PAS dosyasında yazılmıştır. Aşağıda, Delphi kaynak biriminin veya PAS dosyasının temel bir örneği verilmiştir:
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


## Referanslar

* [Delphi Projesi ve Birim Kaynak Dosyalarını Anlama](https://www.thinktco.com/understanding-delphi-project-files-dpr-1057652)
* [İlk Delphi programınızı yazmak](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

