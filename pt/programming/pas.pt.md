{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Arquivo de origem da unidade Delphi",
  "description":"Saiba mais sobre o formato de arquivo PAS com exemplo de PAS e APIs que podem criar e abrir arquivos PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## O que é um arquivo PAS?
Um arquivo .pas é na verdade um arquivo de código fonte que pode ser encontrado em um projeto de programação Delphi. O Delphi é um aplicativo de desenvolvimento de software utilizado por desenvolvedores para construção de softwares baseados em Windows; escrito na linguagem Delphi. A linguagem Delphi é uma variante da linguagem Object Pascal. Assim, ele pode ser compilado em código Win32 nativo com o compilador Delphi.

## Formato de arquivo PAS

O formato de arquivo PAS é um arquivo de codificação que é reservado para a fonte da unidade Delphi. As unidades são percebidas como os principais blocos de construção dos aplicativos Delphi. Você pode visualizar o código fonte do projeto Delphi atual através do menu **Project > View Source**. Os programadores podem criar e salvar uma unidade como um arquivo autônomo que qualquer projeto pode usar. Uma vez que uma unidade é adicionada ao projeto, o Delphi a registra na cláusula uses do arquivo .DPR do projeto.

## Exemplo de arquivo PAS
Quando escrevemos uma única linha de código. Delphi escreve muitas linhas para nós de forma inteligente. Todo o código fonte é escrito em arquivo PAS. A seguir está um exemplo básico de unidade de origem Delphi ou arquivo PAS:
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


## Referências

* [Entendendo o projeto Delphi e os arquivos de origem da unidade](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Escrevendo seu primeiro programa Delphi](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

