{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - plik źródłowy jednostki Delphi",
  "description":"Poznaj format pliku PAS z przykładem PAS i interfejsami API, które mogą tworzyć i otwierać pliki PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Czym jest plik PAS?
Plik .pas jest w rzeczywistości plikiem kodu źródłowego, który można znaleźć w projekcie programistycznym Delphi. Delphi to aplikacja do tworzenia oprogramowania używana przez programistów do tworzenia oprogramowania opartego na systemie Windows; napisany w języku Delphi. Język Delphi jest odmianą języka Object Pascal. Można go więc skompilować do natywnego kodu Win32 za pomocą kompilatora Delphi.

## Format pliku PAS

Format pliku PAS to plik kodowania zarezerwowany dla źródła jednostki Delphi. Jednostki są realizowane jako główne elementy składowe aplikacji Delphi. Możesz przeglądać kod źródłowy bieżącego projektu Delphi poprzez menu **Projekt > Wyświetl źródło**. Programiści mogą tworzyć i zapisywać jednostkę jako samodzielny plik, z którego może korzystać każdy projekt. Po dodaniu jednostki do projektu, Delphi rejestruje ją w klauzuli użytkowania pliku .DPR projektu.

## Przykład pliku PAS
Kiedy piszemy pojedynczą linię kodu. Delphi inteligentnie pisze dla nas wiele wierszy. Cały kod źródłowy jest zapisany w pliku PAS. Poniżej znajduje się podstawowy przykład jednostki źródłowej Delphi lub pliku PAS:
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


## Bibliografia

* [Understanding Delphi Project and Unit Source Files](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Pisanie pierwszego programu w Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

