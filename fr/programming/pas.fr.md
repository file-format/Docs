{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Fichier source de l'unité Delphi",
  "description":"En savoir plus sur le format de fichier PAS avec un exemple PAS et des API qui peuvent créer et ouvrir des fichiers PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Qu'est-ce qu'un fichier PAS ?
Un fichier .pas est en fait un fichier de code source qui peut être trouvé dans un projet de programmation Delphi. Delphi est une application de développement logiciel utilisée par les développeurs pour créer des logiciels basés sur Windows. écrit en langage Delphi. Le langage Delphi est une variante du langage Object Pascal. Il peut donc être compilé en code Win32 natif avec le compilateur Delphi.

## Format de fichier PAS

Le format de fichier PAS est un fichier de codage réservé à la source unitaire Delphi. Les unités sont réalisées en tant que blocs de construction principaux des applications Delphi. Vous pouvez afficher le code source du projet Delphi actuel via le menu **Projet > Afficher la source**. Les programmeurs peuvent créer et enregistrer une unité en tant que fichier autonome que n'importe quel projet peut utiliser. Une fois qu'une unité est ajoutée au projet, Delphi l'enregistre dans la clause uses du fichier .DPR du projet.

## Exemple de fichier PAS
Lorsque nous écrivons une seule ligne de code. Delphi écrit de nombreuses lignes pour nous intelligemment. Tout le code source est écrit dans un fichier PAS. Voici un exemple de base d'unité source Delphi ou de fichier PAS :
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


## Références

* [Comprendre le projet Delphi et les fichiers source d'unité] (https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Écrire votre premier programme Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

