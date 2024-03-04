{
  "date": "2021-04-22",
  "keywords": [
".pas failą",
"pas failo formatą",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS – Delphi vieneto šaltinio failas",
  "description": "Sužinokite apie PAS failo formatą naudodami PAS pavyzdį ir API, kurios gali kurti ir atidaryti PAS failus.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-lts"
}
},
  "lastmod": "2021-04-22"
}

## Kas yra PAS failas?
.pas failas iš tikrųjų yra šaltinio kodo failas, kurį galima rasti Delphi programavimo projekte. Delphi yra programinės įrangos kūrimo programa, kurią kūrėjai naudoja kurdami Windows pagrindu veikiančią programinę įrangą; parašytas Delphi kalba. Delphi kalba yra Object Pascal kalbos variantas. Taigi jį galima sukompiliuoti į savąjį Win32 kodą naudojant Delphi kompiliatorių.

## PAS failo formatas

PAS failo formatas yra kodavimo failas, skirtas Delphi įrenginio šaltiniui. Vienetai realizuojami kaip pagrindiniai Delphi programų elementai. Dabartinio Delphi projekto šaltinio kodą galite peržiūrėti meniu **Projektas > Žiūrėti šaltinį**. Programuotojai gali sukurti ir išsaugoti įrenginį kaip atskirą failą, kurį gali naudoti bet kuris projektas. Kai vienetas pridedamas prie projekto, Delphi užregistruoja jį projekto .DPR failo naudojimo sąlygoje.

## PAS failo pavyzdys
Kai rašome vieną kodo eilutę. Delphi daug eilučių mums rašo protingai. Visas šaltinio kodas parašytas PAS faile. Toliau pateikiamas pagrindinis Delphi šaltinio vieneto arba PAS failo pavyzdys:
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


## Nuorodos

 * [Delphi projekto ir vieneto šaltinio failų supratimas](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Rašau savo pirmąją Delphi programą](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

