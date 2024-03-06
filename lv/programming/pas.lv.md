{
  "date": "2021-04-22",
  "keywords": [
".pas fails",
"pas faila formātā",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS — Delphi vienības avota fails",
  "description": "Uzziniet par PAS faila formātu, izmantojot PAS piemēru un API, kas var izveidot un atvērt PAS failus.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-lvs"
}
},
  "lastmod": "2021-04-22"
}

## Kas ir PAS fails?
.pas fails patiesībā ir avota koda fails, ko var atrast Delphi programmēšanas projektā. Delphi ir programmatūras izstrādes lietojumprogramma, ko izstrādātāji izmanto Windows programmatūras izveidei; rakstīts Delfu valodā. Delphi valoda ir Object Pascal valodas variants. Tādējādi to var apkopot sākotnējā Win32 kodā, izmantojot Delphi kompilatoru.

## PAS faila formāts

PAS faila formāts ir kodēšanas fails, kas ir rezervēts Delphi vienības avotam. Vienības tiek realizētas kā galvenie Delphi lietotņu elementi. Pašreizējā Delphi projekta avota kodu varat apskatīt izvēlnē **Projekts > Skatīt avotu**. Programmētāji var izveidot un saglabāt vienību kā atsevišķu failu, ko var izmantot jebkurš projekts. Kad vienība ir pievienota projektam, Delphi reģistrē to projekta .DPR faila lietošanas klauzulā.

## PAS faila piemērs
Kad mēs rakstām vienu koda rindiņu. Delphi mums gudri raksta daudzas rindas. Viss avota kods ir rakstīts PAS failā. Tālāk ir sniegts Delphi avota vienības vai PAS faila pamata piemērs:
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


## Atsauces

 * [Informācija par Delphi projektu un vienības avota failiem](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Raksti savu pirmo Delphi programmu](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

