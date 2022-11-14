{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC 파일 확장자 - INC 파일이란?",
  "description":"INC 파일을 생성하고 열 수 있는 INC Include 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## .INC 파일이란?

INC 파일은 헤더 정보를 참조하기 위해 소프트웨어 프로그램의 소스 코드에서 사용하는 포함 파일입니다. [.h 파일 형식](/ko/programming/h/)과 유사하며 C++와 같은 소스 코드 파일에서 재사용할 수 있는 선언, 함수, 헤더 또는 매크로를 포함합니다. INC 파일은 C, [C++](/ko/programming/cpp/), Pascal, [PHP](/ko/programming/php/) 및 [Java](/ko/programming/java/)와 같은 다양한 프로그래밍 언어에서 사용됩니다. Microsoft 메모장, 메모장++ 및 TextEdit와 같은 텍스트 편집기를 사용하여 INC 파일을 열 수 있습니다.

## INC 파일 형식 - 추가 정보

INC 파일은 선언 구문에 따라 포함된 모든 선언과 함께 일반 텍스트 파일로 저장됩니다. 하나의 INC 파일은 다른 INC 파일도 참조할 수 있습니다. INC 파일이 생성되면 프로젝트의 일부가 되고 C++와 같은 소스 파일에서 참조할 수 있습니다. 중복을 피하기 위해 여러 소스 파일에서 참조할 수 있습니다.

## INC 파일 내용

INC 파일에는 다음 정보가 포함될 수 있습니다.

**`변수`** - 객체 지향 프로그래밍(OOP)의 경우 클래스 헤더 파일에는 구현 소스 코드 파일에서 액세스할 수 있는 모든 클래스 수준 변수의 정의가 포함됩니다.

**`메소드 선언`** - 모든 메서드 선언은 여러 구현 파일에서 액세스할 수 있도록 .h 헤더 파일에 포함됩니다.

**`비인라인 함수 정의`** - 헤더 파일에는 인라인이 아닌 메서드의 정의도 포함될 수 있습니다.

## PHP에서 INC 파일 사용의 단점

PHP는 서버에서 실행되고 호출 웹페이지에 결과를 반환하는 서버측 스크립트입니다. PHP 파일이 INC 파일을 참조하고 서버가 .inc 파일을 구문 분석하도록 구성되지 않은 경우(매우 일반적임), 사용자는 URL 디렉토리를 방문하여 .inc 파일에서 php 소스 코드를 볼 수 있습니다. 따라서 PHP에서 INC 파일을 포함 파일로 사용할 때 주의해야 합니다.

## 참고문헌

* [PHP에서 INC 사용](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

