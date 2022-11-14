---
date: 2019-10-11
keywords: dart, .dart, dart 파일 형식, dart 파일, dart 파일 실행 방법, .dart 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: 다트 파일 형식
linktitle: Dart
description: "Dart 파일 형식과 Dart 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-18
---

## 다트 파일이란? ##

Dart 파일에는 Google에서 개발한 클라이언트 최적화 프로그래밍 언어인 Dart 프로그래밍 언어의 소스 코드가 포함되어 있습니다. 이 언어는 모바일, 데스크톱, 웹, Iot(사물 인터넷) 등의 앱을 빌드하는 데 사용됩니다. Dart는 객체 지향 언어입니다. C와 유사한 구문을 사용합니다. Dart는 JavaScript 또는 기본 코드로 컴파일할 수 있습니다. 자바스크립트 파일을 실행하는 것처럼 Dart 파일을 유명 웹 브라우저에서 실행할 수 있습니다. Dart SDK와 함께 제공되는 Dart 가상 머신이라는 명령줄 도구를 사용하여 Dart 파일을 컴파일하고 실행할 수도 있습니다.

## 간략한 역사 ##

Dart 프로젝트는 Lars Bak과 Kasper Lund에 의해 설립되었으며 첫 번째 버전은 2013년 11월 14일에 릴리스되었습니다. 저는 초기 Dart는 Google Chrome에 Dart VM을 포함하려는 계획으로 인해 웹 단편화에 대한 비판을 받았습니다. 이러한 계획은 중단되었고 Dart는 2015년 버전 1.9 릴리스와 함께 JavaScript로 컴파일하는 데 집중했습니다.

Dart 2.0은 2018년 8월에 릴리스되어 Dart 코드를 네이티브 Linux, Windows, macOS 플랫폼으로 컴파일하는 dart2native 확장이 도입되었습니다. 이 확장은 해당 플랫폼에서 Dart 앱을 실행하는 데 Dart SDK가 필요하지 않은 자체 포함 실행 파일을 활성화했습니다. 이 확장은 Flutter와도 통합되어 플랫폼 간 앱을 만들 수 있습니다.

ECMA는 2014년 7월 초판, 2014년 12월 초판으로 Dart를 표준화했습니다.


## Dart 코드 실행/실행 방법 ##

Dart 코드는 다음과 같은 방식으로 실행할 수 있습니다.

- **자바스크립트로 컴파일**:</br> Dart 코드는 dart2js 컴파일러를 사용하여 JavaScript로 컴파일됩니다. 컴파일된 JavaScript 코드는 모든 주요 웹 브라우저와 호환됩니다.
- **독립 실행형**:</br> Dart SDK(소프트웨어 개발 키트)는 Dart 코드를 명령줄 인터페이스에서 실행할 수 있는 독립 실행형 Dart VM과 함께 제공됩니다. Dart는 사용자가 완전한 기능의 앱을 작성할 수 있도록 하는 완전한 표준 라이브러리와 함께 제공됩니다.
- **AOT(Ahead-of-Time) 컴파일됨**:</br> Dart 코드는 Flutter로 모바일 앱을 빌드할 수 있도록 하는 기계 코드로 AOT 컴파일될 수 있습니다.
- **토종의**:</br> dart2native 컴파일러를 사용하면 Dart 코드를 Windows, Linux 및 macOS에서 실행할 수 있는 자체 포함 실행 파일로 컴파일할 수 있습니다.

## 다트 파일 형식 ##

Dart는 인터페이스, 믹스인, 추상 클래스, 구체화된 제네릭 및 유형 인터페이스를 지원하는 C 스타일 객체 지향 언어입니다.

### 구문 ###

다음은 Dart 구문의 몇 가지 예입니다.

#### 콘솔로 인쇄 ####

```dart
// print "Hello World" to console
main() {
  print("Hello, World!");
}
```

#### 루프와 배열 ####

```dart
// loops and arrays
var names = {
  'John',
  'James',
  'Rose',
};
main() {
  for (var name in names) {
    print(name);
  }
}
```

#### 기능 ####

```dart
// functions
int double(int x) {
  return x * 2;
}
main() {
  print("double of 10 is ${double(10)}");
}
```

#### 클래스 ####

```dart
// classes
abstract class Person {
  detail();
}

class Student implements Person {
  String firstName = "Jack";
  String lastName = "Wick";
  detail() => print("Student: $firstName $lastName");
}

main() {
  // The 'new' keyword is optional.
  Student student = Student();
  student.detail();
}
```

#### 믹스인 ####

믹스인은 상속 없이 메소드/변수를 빌릴 수 있는 일반 클래스입니다. 이것은 *"with"* 키워드를 사용하여 수행됩니다.

```dart
class B {  
  method(){
     ....
  }
}

class A with B {
  ....
     ......
}
void main() {
  A a = A();
  a.method();  //We are able to access the method of B class without inheriting from it.
}
```

## 참조 ##

- [Dart(프로그래밍 언어) - Wikipedia](https://en.wikipedia.org/wiki/Dart_(programming_language))
- [다트](https://dart.dev/)

