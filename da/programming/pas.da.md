{
  "date": "2021-04-22",
  "keywords": [
".pas-fil",
"pas filformat",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS - Delphi Unit Source File",
  "description": "Lær om PAS-filformat med PAS-eksempel og API'er, der kan oprette og åbne PAS-filer.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-das"
}
},
  "lastmod": "2021-04-22"
}

## Hvad er en PAS fil?
En .pas-fil er faktisk en kildekodefil, som kan findes i et Delphi-programmeringsprojekt. Delphi er en softwareudviklingsapplikation, der bruges af udviklere til at bygge Windows-baseret software; skrevet på Delphi-sproget. Delphi-sproget er en variant af Object Pascal-sproget. Så det kan kompileres til native Win32-kode med Delphi-kompileren.

## PAS filformat

PAS-filformatet er en kodningsfil, som er reserveret til Delphi-enhedskilde. Enhederne er realiseret som de vigtigste byggesten i Delphi-apps. Du kan se det aktuelle Delphi-projekts kildekode gennem menuen **Projekt > Vis kilde**. Programmørerne kan oprette og gemme en enhed som en selvstændig fil, som ethvert projekt kan bruge. Når en enhed er føjet til projektet, registrerer Delphi den i uses-klausulen i projektets .DPR-fil.

## PAS fil eksempel
Når vi skriver en enkelt linje kode. Delphi skriver mange linjer for os intelligent. Al kildekoden er skrevet i PAS-fil. Følgende er et grundlæggende eksempel på Delphi-kildeenhed eller PAS-fil:
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


## Referencer

 * [Forstå Delphi-projekt- og enhedskildefiler](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Skriver dit første Delphi-program](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

