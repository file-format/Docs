
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS 파일 - Ada 사양 파일 형식",
  "description":"ADS 파일을 만들고 열 수 있는 예제와 API를 통해 ADS 파일 형식이 무엇인지 알아보세요.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .ADS 파일이란?

ADS 파일은 Ada 프로그래밍 프로젝트의 사양 파일입니다. Java의 경우 클래스, C++의 경우 헤더 및 구현 쌍과 유사합니다. Ada 패키지의 공개 및 비공개 사양은 .ads 파일에 저장됩니다. 대조적으로 .adb 파일에는 구현 또는 Ada 본문이 포함됩니다. [C++](/ko/programming/cpp/)와 마찬가지로 Ada는 OOP와 무관하게 사양과 구현을 분리합니다.

ADS 파일은 Microsoft 메모장, 메모장++ 및 Atom과 같은 모든 텍스트 편집기에서 열 수 있습니다.

## ADS 파일 형식

ADS 파일은 단순한 일반 텍스트 파일 형식이며 모든 텍스트 편집기로 열거나 편집할 수 있습니다. Ada 패키지는 계층 구조로 구성할 수 있습니다. 자식 유닛은 다음과 같이 선언할 수 있습니다.

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## 참고문헌

* [에이다 패키지](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

