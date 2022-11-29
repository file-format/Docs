{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Delphi Unit Source File",
  "description":"Lär dig mer om PAS-filformat med PAS-exempel och API:er som kan skapa och öppna PAS-filer.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Vad är PAS fil?
En .pas-fil är faktiskt en källkodsfil som kan hittas i ett Delphi-programmeringsprojekt. Delphi är en mjukvaruutvecklingsapplikation som används av utvecklare för att bygga Windows-baserad mjukvara; skriven på Delphi-språket. Delphi-språket är en variant av Object Pascal-språket. Så det kan kompileras till inbyggd Win32-kod med Delphi-kompilatorn.

## PAS filformat

PAS-filformatet är en kodningsfil som är reserverad för Delphi-enhetskälla. Enheterna realiseras som de viktigaste byggstenarna i Delphi-appar. Du kan se det aktuella Delphi-projektets källkod genom menyn **Projekt > Visa källa**. Programmerarna kan skapa och spara en enhet som en fristående fil som alla projekt kan använda. När en enhet läggs till i projektet, registrerar Delphi den i uses-satsen i projektets .DPR-fil.

## Exempel på PAS-fil
När vi skriver en enda rad kod. Delphi skriver många rader åt oss intelligent. All källkod är skriven i PAS-fil. Följande är ett grundläggande exempel på Delphi källenhet eller PAS-fil:
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


## Referenser

* [Förstå Delphi Project and Unit Source Files](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Skriver ditt första Delphi-program](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

