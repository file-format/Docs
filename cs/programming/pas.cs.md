{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Delphi Unit Source File",
  "description":"Další informace o formátu souboru PAS s příkladem PAS a rozhraními API, která mohou vytvářet a otevírat soubory PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Co je soubor PAS?
Soubor .pas je ve skutečnosti soubor se zdrojovým kódem, který lze nalézt v programovacím projektu Delphi. Delphi je aplikace pro vývoj softwaru, kterou používají vývojáři pro vytváření softwaru na bázi Windows; napsané v jazyce Delphi. Jazyk Delphi je variantou jazyka Object Pascal. Lze jej tedy zkompilovat do nativního kódu Win32 pomocí kompilátoru Delphi.

## Formát souboru PAS

Formát souboru PAS je kódovací soubor, který je vyhrazen pro zdroj jednotky Delphi. Jednotky jsou realizovány jako hlavní stavební bloky aplikací Delphi. Zdrojový kód aktuálního projektu Delphi můžete zobrazit prostřednictvím nabídky **Projekt > Zobrazit zdroj**. Programátoři mohou vytvořit a uložit jednotku jako samostatný soubor, který může použít jakýkoli projekt. Jakmile je jednotka přidána do projektu, Delphi ji zaregistruje v klauzuli použití souboru .DPR projektu.

## Příklad souboru PAS
Když napíšeme jeden řádek kódu. Delphi pro nás píše mnoho řádků inteligentně. Veškerý zdrojový kód je zapsán v souboru PAS. Níže je uveden základní příklad zdrojové jednotky Delphi nebo souboru PAS:
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


## Reference

* [Porozumění Delphi Project a Unit Source Files](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Psaní svého prvního programu Delphi](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

