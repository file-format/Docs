{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS – Delphi egység forrásfájlja",
  "description":"Tudjon meg többet a PAS-fájlformátumról a PAS-példával és az API-kkal, amelyek PAS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Mi az a PAS fájl?
A .pas fájl valójában egy forráskód fájl, amely egy Delphi programozási projektben található. A Delphi egy szoftverfejlesztő alkalmazás, amelyet a fejlesztők Windows alapú szoftverek készítésére használnak; Delphi nyelven írva. A Delphi nyelv az Object Pascal nyelv egy változata. Így a Delphi fordítóval natív Win32 kódba fordítható.

## PAS fájlformátum

A PAS fájlformátum egy kódoló fájl, amely a Delphi egységforrás számára van fenntartva. Az egységek a Delphi alkalmazások fő építőelemeiként valósulnak meg. Az aktuális Delphi projekt forráskódját a **Projekt > Forrás megtekintése** menüben tekintheti meg. A programozók létrehozhatnak és elmenthetnek egy egységet önálló fájlként, amelyet bármely projekt használhat. Miután hozzáadott egy egységet a projekthez, a Delphi regisztrálja azt a projekt .DPR fájl uses záradékában.

## PAS fájl példa
Amikor egyetlen kódsort írunk. A Delphi sok sort ír nekünk intelligensen. Az összes forráskód PAS fájlba van írva. Az alábbiakban egy alapvető példa a Delphi forrásegységre vagy PAS fájlra:
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


## Hivatkozások

* [A Delphi projekt és az egység forrásfájljainak ismertetése](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Az első Delphi-program megírása](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

