{
  "date": "2021-04-22",
  "keywords": [
"comhad .pas",
"formáid comhaid pas",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "PAS - Comhad Foinse Aonaid Delphi",
  "description": "Foghlaim faoi fhormáid comhaid PAS le sampla PAS agus APIanna ar féidir leo comhaid PAS a chruthú agus a oscailt.",
  "linktitle": "PAS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pa-gas"
}
},
  "lastmod": "2021-04-22"
}

## Cad is comhad PAS ann?
Is comhad cód Foinse é comhad .pas atá le fáil i dtionscadal ríomhchláraithe Delphi. Feidhmchlár forbartha bogearraí é an Delphi a úsáideann forbróirí chun bogearraí atá bunaithe ar Windows a thógáil; scríofa sa teanga Delphi. Is malairt í an teanga Delphi den teanga Object Pascal. Mar sin is féidir é a thiomsú i gcód dúchais Win32 leis an tiomsaitheoir Delphi.

## Formáid comhaid PAS

Is comhad códaithe é formáid comhaid PAS atá curtha in áirithe d'fhoinse aonaid Delphi. Tá na haonaid réadaithe mar phríomhbhloic thógála aipeanna Delphi. Is féidir leat cód foinse an tionscadail Delphi reatha a fheiceáil tríd an roghchlár **Project > View Source**. Is féidir leis na ríomhchláraitheoirí aonad a chruthú agus a shábháil mar chomhad aonair is féidir le haon tionscadal a úsáid. Nuair a chuirtear aonad leis an tionscadal, cláraíonn Delphi é i gclásal úsáidí an chomhaid .DPR tionscadail.

## Sampla comhad PAS
Nuair a scríobhaimid líne amháin de chód. Scríobhann Delphi go leor línte dúinn go cliste. Tá an cód foinse ar fad scríofa i gcomhad PAS. Seo a leanas sampla bunúsach d'aonad foinse Delphi nó comhad PAS:
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


## Tagairtí

 * [Tionscadal Delphi agus Comhaid Foinse Aonaid a Thuiscint](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
 * [Do chéad chlár Delphi á scríobh](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

