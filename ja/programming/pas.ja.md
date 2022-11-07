{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - Delphi ユニット ソース ファイル",
  "description":"PAS の例と,PAS ファイルを作成して開くことができる API を使用して,PAS ファイル形式について学びます。",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## .PAS ファイルとは何ですか?
.pas ファイルは、実際には Delphi プログラミング プロジェクトにあるソース コード ファイルです。 Delphi は、開発者が Windows ベースのソフトウェアを構築するために使用するソフトウェア開発アプリケーションです。 Delphi 言語で書かれています。 Delphi 言語は、Object Pascal 言語の変形です。そのため、Delphi コンパイラを使用してネイティブの Win32 コードにコンパイルできます。

## PAS ファイル形式

PAS ファイル形式は、Delphi ユニット ソース用に予約されているコーディング ファイルです。ユニットは、Delphi アプリの主要なビルディング ブロックとして実現されます。 **Project > View Source** メニューから、現在の Delphi プロジェクトのソース コードを表示できます。プログラマーは、任意のプロジェクトで使用できるスタンドアロン ファイルとしてユニットを作成および保存できます。ユニットがプロジェクトに追加されると、Delphi はそれをプロジェクトの .DPR ファイルの uses 句に登録します。

## PAS ファイルの例
1行のコードを書くとき。 Delphi は、インテリジェントに多くの行を作成してくれます。すべてのソース コードは PAS ファイルに記述されています。以下は、Delphi ソース ユニットまたは PAS ファイルの基本的な例です。
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


## 参考文献

* [Delphi プロジェクトとユニット ソース ファイルについて](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [初めての Delphi プログラムを書く](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

