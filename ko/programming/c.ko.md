{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","ac 파일이란","c 파일을 여는 방법", "확장자", "파일", "c 파일","c 파일 형식", "c 파일 확장자"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"C - C 언어 프로그래밍 파일",
  "description":"C 파일 형식과 C 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## C 파일이란?

c 파일 확장자로 저장된 파일은 C 프로그래밍 언어로 작성된 소스 코드 파일입니다. **C 파일**에는 애플리케이션 기능의 모든 구현이 소스 코드 형식으로 포함됩니다. 소스 코드의 선언은 [.h](/ko/programming/h/) 확장자로 저장되는 헤더 파일에 작성됩니다. C++는 C 언어의 현대적 형태이며 오늘날 대부분의 소프트웨어를 개발하는 데 사용됩니다.

## 약력

C 언어는 UNIX 운영 체제용으로 다양한 유틸리티를 만든 결과 탄생했습니다. 이 프로그래밍 언어를 만든 사람인 Denis Ritchie는 원래 1960년대와 1970년대 초에 작업을 시작했습니다.

## C 파일 형식

C 파일은 프로그래밍 언어 구문에 따라 일반 텍스트 파일 형식으로 작성됩니다. 일반적인 C 파일에는 다음이 포함됩니다.

* 헤더 파일을 가져오기 위한 파일 상단의 import 문
* 원하는 기능을 구현하는 하나 이상의 방법

### 헤더 가져오기

확장자가 .h인 헤더 파일에는 프로젝트에 다른 기능 파일을 포함하는 데 필요한 포함 문이 포함되어 있습니다. 또한 여기에는 구현 파일에 정의된 메서드 선언이 포함됩니다. 헤더 파일은 아래와 같이 include 문을 사용하여 포함됩니다.

```
#include <filename.h>
```

### 소스 코드 구현

기능 요구 사항의 실제 구현은 C 파일의 메소드로 코딩됩니다. C 파일의 각 메소드에는 리턴 유형, 메소드 이름이 있으며 일부 입력 매개변수가 있을 수 있습니다. 반환 유형이 void가 아니면 메서드가 일부 값을 반환할 수 있습니다.

### C 코드 예
다음은 ac 예제 프로그램입니다.

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **참조** ##

* [클래스 구현 - 위키피디아 작성](https://en.wikipedia.org/wiki/Class_implementation_file)

