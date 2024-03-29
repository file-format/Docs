{
"날짜": "2023-05-15",
  "keywords": [
"csx 파일",
"csx 파일이 무엇인가요?",
"csx 파일에는 무엇이 포함되어 있나요?",
"csx 파일의 형식은 무엇입니까",
"파일",
"csx 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "CSX 파일 형식 - Visual C# 스크립트",
  "description":"CSX 파일을 생성하고 열 수 있는 CSX 형식과 API에 대해 알아보세요.",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent" : "programming"
}
},
"lastmod": "2023-05-15"
}

## .CSX 파일이란?

Visual C# 스크립트(CSX라고도 함)는 Microsoft .NET 생태계의 Roslyn 스크립팅 엔진에서 사용되는 파일 형식입니다. CSX 파일에는 별도의 컴파일 단계 없이 직접 실행할 수 있는 C# 코드가 포함되어 있습니다.

CSX 형식은 Microsoft 에코시스템에만 적용되며 일반 프로그래밍에서 널리 사용되는 파일 형식은 아닙니다. CSX 파일은 빠른 프로토타이핑 또는 스크립팅 기능이 필요한 시나리오에서 자주 사용됩니다. 이를 통해 본격적인 컴파일된 애플리케이션을 만드는 것보다 더 가벼운 방식으로 C# 프로그램을 만들고 실행할 수 있습니다.

CSX 파일을 실행하려면 C# 코드 실행을 위한 대화형 환경을 제공하는 .NET Interactive Notebooks와 같은 도구를 사용할 수 있습니다. C# 확장이 포함된 Visual Studio Code 및 .NET Core SDK를 사용하여 CSX 파일 작업을 수행할 수도 있습니다.

## CSX 파일에는 무엇이 포함되어 있습니까?

CSX(C# 스크립트) 파일에는 직접 실행할 수 있는 C# 코드가 포함되어 있습니다. 여기에는 변수 선언, 함수, 클래스 및 기타 프로그래밍 구문과 같은 유효한 C# 코드가 포함될 수 있습니다.

다음은 CSX 파일에 포함될 수 있는 내용의 예입니다.

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX 파일에는 import 문, 외부 라이브러리 참조 및 기타 C# 언어 기능이 포함되어 코드 기능을 지원할 수도 있습니다. 코드는 컴파일할 필요 없이 즉시 해석되고 실행되므로 스크립팅 및 빠른 프로토타이핑 작업에 적합합니다.

## CSX 파일의 형식은 무엇입니까?

CSX(C# 스크립트) 형식은 간단한 텍스트 기반 형식을 따릅니다. 일반 C# 소스 코드 파일(.cs)과 구별하기 위해 일반적으로 파일 확장자는 .csx입니다.

CSX 파일은 C# 구문 강조를 지원하는 텍스트 편집기나 IDE(통합 개발 환경)를 사용하여 편집할 수 있습니다. CSX 파일이 준비되면 .NET Interactive Notebooks, .NET Core 명령줄 인터페이스(CLI) 또는 C# 스크립팅을 지원하는 IDE와 같은 도구를 사용하여 실행할 수 있습니다.

## 참고자료
* [C# programming with Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)
