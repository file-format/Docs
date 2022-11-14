{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Delphi Unit-bronbestand",
  "description":"Meer informatie over PAS-bestandsindeling met PAS-voorbeeld en API's die PAS-bestanden kunnen maken en openen.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Wat is een PAS-bestand?
Een .pas-bestand is eigenlijk een broncodebestand dat te vinden is in een Delphi-programmeerproject. De Delphi is een softwareontwikkelingstoepassing die door ontwikkelaars wordt gebruikt voor het bouwen van op Windows gebaseerde software; geschreven in de Delphi-taal. De Delphi-taal is een variant van de Object Pascal-taal. Het kan dus worden gecompileerd tot native Win32-code met de Delphi-compiler.

## PAS-bestandsindeling

Het PAS-bestandsformaat is een coderingsbestand dat is gereserveerd voor de Delphi-eenheidsbron. De units worden gerealiseerd als de belangrijkste bouwstenen van Delphi apps. U kunt de broncode van het huidige Delphi-project bekijken via het menu **Project > Bron weergeven**. De programmeurs kunnen een eenheid maken en opslaan als een op zichzelf staand bestand dat door elk project kan worden gebruikt. Zodra een eenheid aan het project is toegevoegd, registreert Delphi deze in de gebruiksclausule van het project .DPR-bestand.

## PAS-bestand voorbeeld
Wanneer we een enkele regel code schrijven. Delphi schrijft intelligent veel regels voor ons. Alle broncode is geschreven in PAS-bestand. Hieronder volgt een eenvoudig voorbeeld van een Delphi-broneenheid of PAS-bestand:
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


## Referenties

* [Inzicht in Delphi Project- en Unit-bronbestanden](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Uw eerste Delphi-programma schrijven](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

