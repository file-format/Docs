{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - 델파이 유닛 소스 파일",
  "description":"PAS 파일을 만들고 열 수 있는 API와 PAS 예제를 통해 PAS 파일 형식에 대해 알아보세요.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## .PAS 파일이란?
.pas 파일은 실제로 델파이 프로그래밍 프로젝트에서 찾을 수 있는 소스 코드 파일입니다. Delphi는 Windows 기반 소프트웨어를 구축하기 위해 개발자가 사용하는 소프트웨어 개발 응용 프로그램입니다. 델파이 언어로 작성되었습니다. 델파이 언어는 오브젝트 파스칼 언어의 변형입니다. 따라서 델파이 컴파일러를 사용하여 네이티브 Win32 코드로 컴파일할 수 있습니다.

## PAS 파일 형식

PAS 파일 형식은 델파이 유닛 소스용으로 예약된 코딩 파일입니다. 단위는 델파이 앱의 주요 빌딩 블록으로 구현됩니다. **Project > View Source** 메뉴를 통해 현재 Delphi 프로젝트의 소스 코드를 볼 수 있습니다. 프로그래머는 모든 프로젝트에서 사용할 수 있는 독립 실행형 파일로 장치를 만들고 저장할 수 있습니다. 유닛이 프로젝트에 추가되면 Delphi는 프로젝트 .DPR 파일의 uses 절에 이를 등록합니다.

## PAS 파일 예
한 줄의 코드를 작성할 때. 델파이는 우리를 위해 많은 줄을 지능적으로 작성합니다. 모든 소스 코드는 PAS 파일에 작성됩니다. 다음은 델파이 소스 유닛 또는 PAS 파일의 기본 예입니다.
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


## 참고문헌

* [델파이 프로젝트 및 유닛 소스 파일 이해하기](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [첫 델파이 프로그램 작성하기](http://www.delphibasics.co.uk/Article.php?Name=FirstPgm)

