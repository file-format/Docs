{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Изходен файл на Delphi Unit",
  "description":"Научете за файловия формат PAS с пример за PAS и API, които могат да създават и отварят PAS файлове.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Какво е PAS файл?
Файлът .pas всъщност е файл с изходен код, който може да бъде намерен в проект за програмиране на Delphi. Delphi е приложение за разработка на софтуер, използвано от разработчиците за изграждане на софтуер, базиран на Windows; написана на езика Delphi. Езикът Delphi е вариант на езика Object Pascal. Така че може да се компилира в нативен Win32 код с компилатора Delphi.

## PAS файлов формат

Файловият формат PAS е кодиращ файл, който е запазен за изходния код на Delphi. Единиците са реализирани като основни градивни елементи на приложенията на Delphi. Можете да видите изходния код на текущия Delphi проект чрез менюто **Проект > Преглед на изходния код**. Програмистите могат да създадат и запазят единица като самостоятелен файл, който всеки проект може да използва. След като единица бъде добавена към проекта, Delphi я регистрира в клаузата uses на проекта .DPR файл.

## Пример за PAS файл
Когато пишем един ред код. Delphi пише много редове за нас интелигентно. Целият изходен код е написан в PAS файл. Следва основен пример за изходна единица на Delphi или PAS файл:
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


## Препратки

* [Разбиране на проекти Delphi и файлове с изходен код на единици](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Писане на вашата първа програма Delphi](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

