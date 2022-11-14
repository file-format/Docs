{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "파일", "확장자", "파일 형식", "비주얼 베이직", "프로그래밍 가이드" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic 코드 파일",
  "description":"VB 파일 형식과 VB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .VB 파일이란?

VB 파일은 .NET 응용 프로그램 개발을 위해 Microsoft에서 만든 Visual Basic 언어로 만든 소스 코드 파일입니다. 구문이 다른 또 다른 유사한 언어는 파일이 [.CS](/ko/programming/cs/) 파일 확장자로 저장되는 C#입니다. 파일 형식은 EXE 또는 DLL 형식의 최종 출력 파일을 생성하기 위해 컴파일되는 코드를 작성하기 위한 저수준 프로그래밍 언어를 제공합니다. Microsoft Visual Studio로 만들고 컴파일할 수 있습니다. Microsoft Visual Studio Express를 사용하여 무료 IDE인 이러한 파일을 만들고 업데이트할 수도 있습니다. VB 언어로 만든 간단한 Visual Studio 프로젝트[솔루션](/ko/programming/sln/)는 하나 이상의 이러한 파일로 구성될 수 있습니다. 컴파일에 포함하도록 표시된 파일은 프로젝트의 일부이며 컴파일러에 표시된 파일을 사용하도록 지시하는 [CSPROJ](/ko/programming/csproj/) 파일에 나열됩니다.

## VB 파일 형식 - 추가 정보

VB 파일은 편집을 위해 모든 텍스트 편집기에서 열 수 있는 텍스트 기반 파일 형식입니다. 그러나 적절한 구문 강조 표시와 함께 지원되는 IDE에서 열면 코드를 읽고 정렬하기 쉽습니다. 간단한 VB 파일에는 다음이 포함됩니다.

* 네임스페이스 선언 - 특정 네임스페이스에 의해 정의된 특정 기능을 참조하기 위해
* 변수 선언 - 특정 구현을 위한 클래스 수준 변수 선언
* 메소드 선언 - 특정 기능에 대한 메소드 선언 선언

## VB 파일 형식 예

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



