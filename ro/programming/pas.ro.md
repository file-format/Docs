{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - fișierul sursă al unității Delphi",
  "description":"Aflați despre formatul de fișier PAS cu exemplu PAS și API-uri care pot crea și deschide fișiere PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Ce este un fișier PAS?
Un fișier .pas este de fapt un fișier de cod sursă care poate fi găsit într-un proiect de programare Delphi. Delphi este o aplicație de dezvoltare software utilizată de dezvoltatori pentru a construi software-uri bazate pe Windows; scris în limba Delphi. Limbajul Delphi este o variantă a limbajului Object Pascal. Deci poate fi compilat în cod Win32 nativ cu compilatorul Delphi.

## Format de fișier PAS

Formatul de fișier PAS este un fișier de codare care este rezervat sursei unității Delphi. Unitățile sunt realizate ca elemente de bază ale aplicațiilor Delphi. Puteți vizualiza codul sursă al proiectului actual Delphi prin meniul **Proiect > Vizualizare sursă**. Programatorii pot crea și salva o unitate ca fișier de sine stătător pe care îl poate folosi orice proiect. Odată ce o unitate este adăugată la proiect, Delphi o înregistrează în clauza de utilizare a fișierului .DPR al proiectului.

## Exemplu de fișier PAS
Când scriem o singură linie de cod. Delphi scrie multe rânduri pentru noi în mod inteligent. Tot codul sursă este scris în fișierul PAS. Următorul este un exemplu de bază de unitate sursă Delphi sau fișier PAS:
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


## Referințe

* [Înțelegerea proiectelor Delphi și a fișierelor sursă unității](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Scrierea primului tău program Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

