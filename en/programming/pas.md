{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PAS - Delphi Unit Source File",
  "description":"Learn about PAS file format with PAS example and APIs that can create and open PAS files.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-22"
}

## What is a PAS file?
A .pas file is actually a Source code file which can be found in a Delphi programming project. The Delphi is a software development application used by developers for building Windows based softwares; written in the Delphi language. The Delphi language is a variant of the Object Pascal language. So it can be compiled into native Win32 code with the Delphi compiler.

## PAS file format

The PAS file format is a coding file which is reserved for Delphi unit source. The units are realized as the main building blocks of Delphi apps. You can view the current Delphi project's source code through the **Project > View Source** menu. The programmers can create and save a unit as a stand-alone file that any project can use. Once a unit is added to the project, Delphi registers it in the uses clause of the project .DPR file.

## PAS file example
When we write a single line of code. Delphi writes many lines for us intelligently. All the source code is written in PAS file. Following is a basic example of Delphi source unit or PAS file:
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


## References

 * [Understanding Delphi Project and Unit Source Files](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Writing your first Delphi program](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)
