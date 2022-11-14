{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Archivo fuente de la unidad Delphi",
  "description":"Obtenga información sobre el formato de archivo PAS con el ejemplo de PAS y las API que pueden crear y abrir archivos PAS",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## ¿Qué es un archivo PAS?
Un archivo .pas es en realidad un archivo de código fuente que se puede encontrar en un proyecto de programación de Delphi. Delphi es una aplicación de desarrollo de software utilizada por los desarrolladores para crear software basado en Windows; escrito en lengua de Delfos. El lenguaje Delphi es una variante del lenguaje Object Pascal. Por lo tanto, se puede compilar en código Win32 nativo con el compilador Delphi.

## formato de archivo PAS

El formato de archivo PAS es un archivo de codificación que está reservado para la fuente de la unidad Delphi. Las unidades se realizan como los principales componentes básicos de las aplicaciones Delphi. Puede ver el código fuente del proyecto Delphi actual a través del menú **Proyecto > Ver código fuente**. Los programadores pueden crear y guardar una unidad como un archivo independiente que cualquier proyecto puede usar. Una vez que se agrega una unidad al proyecto, Delphi la registra en la cláusula de usos del archivo .DPR del proyecto.

## Ejemplo de archivo PAS
Cuando escribimos una sola línea de código. Delphi nos escribe inteligentemente muchas líneas. Todo el código fuente está escrito en un archivo PAS. A continuación se muestra un ejemplo básico de unidad de origen de Delphi o archivo PAS:
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


## Referencias

* [Comprensión de los archivos de origen de unidades y proyectos Delphi] (https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Escribiendo su primer programa Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

