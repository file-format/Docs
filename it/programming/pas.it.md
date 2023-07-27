{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - File sorgente unità Delphi",
  "description":"Scopri il formato di file PAS con l'esempio PAS e le API che possono creare e aprire file PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Che cos'è un file PAS?
Un file .pas è in realtà un file di codice sorgente che può essere trovato in un progetto di programmazione Delphi. Il Delphi è un'applicazione di sviluppo software utilizzata dagli sviluppatori per la creazione di software basati su Windows; scritto in lingua Delphi. Il linguaggio Delphi è una variante del linguaggio Object Pascal. Quindi può essere compilato in codice Win32 nativo con il compilatore Delphi.

## Formato file PAS

Il formato di file PAS è un file di codifica riservato alla sorgente dell'unità Delphi. Le unità sono realizzate come elementi costitutivi principali delle app Delphi. È possibile visualizzare il codice sorgente del progetto Delphi corrente tramite il menu **Progetto > Visualizza sorgente**. I programmatori possono creare e salvare un'unità come file autonomo che può essere utilizzato da qualsiasi progetto. Una volta aggiunta un'unità al progetto, Delphi la registra nella clausola use del file .DPR del progetto.

## Esempio di file PAS
Quando scriviamo una singola riga di codice. Delphi scrive molte righe per noi in modo intelligente. Tutto il codice sorgente è scritto nel file PAS. Di seguito è riportato un esempio di base di unità sorgente Delphi o file PAS:
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


## Riferimenti

* [Capire il progetto Delphi e i file di origine dell'unità](https://www.thinktco.com/understanding-delphi-project-files-dpr-1057652)
* [Scrivere il tuo primo programma Delphi](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

