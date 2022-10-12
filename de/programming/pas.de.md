{
  "date" : "2021-04-22",
"Schlüsselwörter": [ ".pas-Datei", "pas-Dateiformat", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Quelldatei der Delphi-Unit",
  "description":"Erfahren Sie mehr über das PAS-Dateiformat mit PAS-Beispiel und APIs, die PAS-Dateien erstellen und öffnen können.",
  "linktitle" :"PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Was ist eine PAS-Datei?
Eine .pas-Datei ist eigentlich eine Quellcodedatei, die in einem Delphi-Programmierprojekt zu finden ist. Delphi ist eine Softwareentwicklungsanwendung, die von Entwicklern zum Erstellen von Windows-basierter Software verwendet wird. in Delphi geschrieben. Die Sprache Delphi ist eine Variante der Sprache Object Pascal. Es kann also mit dem Delphi-Compiler in nativen Win32-Code kompiliert werden.

## PAS-Dateiformat

Das PAS-Dateiformat ist eine Codierungsdatei, die für Delphi-Unit-Quellen reserviert ist. Die Units sind als Hauptbausteine von Delphi-Apps realisiert. Sie können den Quellcode des aktuellen Delphi-Projekts über das Menü **Projekt > Quellcode anzeigen** anzeigen. Die Programmierer können eine Einheit als eigenständige Datei erstellen und speichern, die von jedem Projekt verwendet werden kann. Nachdem dem Projekt eine Unit hinzugefügt wurde, registriert Delphi sie in der uses-Klausel der .DPR-Datei des Projekts.

## Beispiel einer PAS-Datei
Wenn wir eine einzelne Codezeile schreiben. Delphi schreibt viele Zeilen intelligent für uns. Der gesamte Quellcode ist in eine PAS-Datei geschrieben. Es folgt ein einfaches Beispiel für eine Delphi-Quelleinheit oder eine PAS-Datei:
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


## Verweise

* [Delphi-Projekt- und Unit-Quelldateien verstehen](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Ihr erstes Delphi-Programm schreiben](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

