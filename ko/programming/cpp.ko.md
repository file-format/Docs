{
  "date" : "2019-10-11",
  "keywords" :[ "C++", "파일", "확장자", "파일 형식", "C++", "프로그래밍 언어" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ 소스 코드 파일",
  "description":"CPP 파일 형식과 CPP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## C++ 파일이란?

CPP 파일 확장자를 가진 파일은 C++ 프로그래밍 언어로 작성된 응용 프로그램의 소스 코드 파일입니다. 단일 C++ 프로젝트에는 애플리케이션 소스 코드로 둘 이상의 CPP 파일이 포함될 수 있습니다. 이러한 프로젝트는 헤더(.h) 파일에 선언된 메서드의 모든 정의를 포함하므로 CPP 파일을 구현 파일이라고 하는 다양한 파일 형식으로 구성됩니다. C++ 프로젝트는 전체적으로 컴파일될 때 실행 가능한 응용 프로그램이 됩니다.

## CPP 파일 구조

CPP 파일 구조는 헤더 파일에 비해 단순합니다. 이러한 구현 파일의 주요 목적은 구현에서 인터페이스를 분리하는 것입니다. 그 결과 헤더 파일의 모든 멤버 함수와 CPP 파일 내부의 세부 정보가 선언됩니다. CPP 구현 파일은 응용 프로그램 작성을 위한 간단한 파일이나 클래스 구현으로 사용할 수 있습니다.

### 독립적인 구현

CPP 파일을 독립 응용 프로그램으로 사용할 때 헤더 파일에 메서드 선언 없이도 내부에 모든 구현을 포함할 수 있습니다. 이러한 구현은 선택적 사용자 입력을 인수로 사용하는 기본 메서드에 의해 애플리케이션 항목이 제어되는 구현 파일에 정의된 모든 메서드로 구성됩니다. 또한 파일에서 선언된 메서드에서 사용할 C++ 표준 라이브러리의 모든 라이브러리를 포함할 수 있습니다.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### 클래스 구현

객체 지향 프로그래밍(OOP)에서 CPP 파일은 클래스 정의로 사용됩니다. 이 경우 모든 클래스 데이터 멤버와 멤버 함수는 헤더 파일 내부에 선언됩니다. 각 헤더 파일은 표준 라이브러리 메서드에 대한 참조도 가질 수 있습니다. 클래스 정의 CPP 파일은 파일 시작 부분에 있는 include 문의 헤더 파일을 참조합니다. 대부분 소프트웨어 개발자는 클래스 구현 파일의 시작 부분에 파일의 실제 내용, 작성자 세부 정보 및 구현 날짜에 대한 정보를 제공하는 주석을 포함합니다. 이러한 경우 헤더 구현 파일은 동일한 이름을 가져야 합니다. 이러한 헤더 및 구현 파일의 예는 다음과 같습니다.

### 헤더 파일

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP 구현 파일

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## 참고문헌

* [클래스 구현 - 위키피디아 작성](https://en.wikipedia.org/wiki/Class_implementation_file)

