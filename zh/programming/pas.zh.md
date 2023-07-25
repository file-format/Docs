{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - 德尔福单元源文件",
  "description":"通过 PAS 示例和可以创建和打开 PAS 文件的 API 了解 PAS 文件格式。",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## 什么是一 .pas 文件？
.pas 文件实际上是一个源代码文件，可以在 Delphi 编程项目中找到。 Delphi 是开发人员用于构建基于 Windows 的软件的软件开发应用程序；用德尔福语言编写。 Delphi 语言是 Object Pascal 语言的变体。所以它可以用Delphi编译器编译成本机Win32代码。

## PAS 文件格式

PAS 文件格式是为 Delphi 单元源保留的编码文件。这些单元被实现为 Delphi 应用程序的主要构建块。您可以通过 **Project > View Source** 菜单查看当前 Delphi 项目的源代码。程序员可以创建一个单元并将其保存为任何项目都可以使用的独立文件。一旦一个单元被添加到项目中，Delphi 就会在项目 .DPR 文件的 uses 子句中注册它。

## PAS 文件示例
当我们编写一行代码时。 Delphi 智能地为我们编写了许多行。所有源代码都写在 PAS 文件中。以下是 Delphi 源单元或 PAS 文件的基本示例：
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


## 参考

* [了解Delphi项目和单元源文件](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [编写你的第一个 Delphi 程序](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

