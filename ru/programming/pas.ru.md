{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS — исходный файл модуля Delphi",
  "description":"Узнайте о формате файла PAS на примере PAS и API-интерфейсах, которые могут создавать и открывать файлы PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## .PAS вариант №
Файл .pas на самом деле является файлом исходного кода, который можно найти в проекте программирования Delphi. Delphi — это приложение для разработки программного обеспечения, используемое разработчиками для создания программного обеспечения для Windows; написан на языке Delphi. Язык Delphi является вариантом языка Object Pascal. Таким образом, его можно скомпилировать в собственный код Win32 с помощью компилятора Delphi.

## Формат PAS-файла

Формат файла PAS представляет собой файл кодирования, который зарезервирован для исходного кода модуля Delphi. Модули реализованы как основные строительные блоки приложений Delphi. Вы можете просмотреть исходный код текущего проекта Delphi через меню **Project > View Source**. Программисты могут создавать и сохранять модуль в виде отдельного файла, который можно использовать в любом проекте. Как только модуль добавляется в проект, Delphi регистрирует его в разделе uses файла проекта .DPR.

## Пример PAS-файла
Когда мы пишем одну строчку кода. Delphi грамотно пишет за нас много строк. Весь исходный код написан в файле PAS. Ниже приведен базовый пример исходного модуля Delphi или файла PAS:
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


## использованная литература

* [Понимание проекта Delphi и исходных файлов модулей] (https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Написание вашей первой программы Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

