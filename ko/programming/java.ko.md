---
date: 2019-10-11
keywords: java, .java, java 파일 형식, Java 파일을 여는 방법, Java 파일을 실행하는 방법, Java 파일, Java 샘플 코드
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: 자바 파일 형식
linktitle: Java
description: "Java 파일 형식과 Java 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## 자바 파일이란? ##
Java 소스 코드를 포함하고 .java 파일 확장자로 저장되는 파일을 Java 파일이라고 합니다. Java는 게임, 모바일, 웹 및 데스크톱 응용 프로그램 개발에 가장 널리 사용되는 기술 중 하나입니다. Java는 플랫폼 독립적이기 때문에 Windows, Mac, Linux, Raspberry Pi 등에서 완벽하게 작동합니다. Java는 C# 및 C++와 매우 유사하므로 이러한 언어 간에 전환하기가 더 쉽습니다.

## 간략한 역사 ##

Java 프로젝트는 1991년 6월 James Gosling, Mike Sheridan 및 Patrick Naughton에 의해 시작되었습니다. Java는 처음에 Oak로 이름이 지정되었습니다. 나중에 Green으로 이름이 바뀌었고 마침내 Java로 변경되었습니다. James Gosling은 C/C++와 유사한 구문으로 Java를 설계했습니다. Java의 첫 번째 공개 버전은 1996년 Sun Microsystems에 의해 출시되었습니다. Java가 빠르게 대중화되도록 만든 모든 대중적인 시스템에서 실행될 수 있습니다. 1998년 12월 Java 2 릴리스와 함께 다양한 유형의 플랫폼에 대한 여러 구성이 구축되었습니다. 버전은 다음과 같았습니다

- J2EE(Java EE): 엔터프라이즈 솔루션용
- J2ME(Java ME): 모바일 애플리케이션용
- J2SE(Java SE): 데스크탑 애플리케이션용

2006년 11월 19일 Sun은 JVM(Java Virtual Machine)을 무료 및 오픈 소스 소프트웨어로 출시했습니다. Oracle Corporation이 2009~2010년에 Sun Microsystems를 인수한 후 James Gosling은 2010년 4월 2일 Oracle에서 사임했습니다.

## 자바 코드 실행/실행 방법 ##

Java 코드를 실행하려면 먼저 컴파일해야 합니다. 이를 위해서는 Java SDK가 필요합니다. Java SDK는 Java 코드를 바이트코드 클래스 파일로 컴파일합니다. Eclipse 및 IntelliJ Idea와 같은 IDE에는 코드 완성 기능을 제공하고 Java 코드를 컴파일하고 실행하기 위한 사용하기 쉬운 인터페이스를 제공하여 Java 파일 작업을 더 쉽게 하는 IntelliJ Idea가 있습니다.

## 자바 파일 형식 ##

Java의 구문은 C 및 C++의 영향을 많이 받았지만 C++와 달리 Java는 거의 독점적으로 객체 지향 언어로 구축되었습니다. Java에서 모든 코드는 클래스 내부에 작성되고 모든 데이터 항목은 객체입니다. C++와 달리 Java는 연산자 오버로딩 또는 다중 상속을 지원하지 않습니다.

### 자바 샘플 코드 ###

다음은 Java 구문의 예입니다.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
위의 코드에서 **public** 키워드는 접근 한정자를 나타냅니다. 이 클래스는 클래스 계층 외부의 클래스에서 액세스할 수 있음을 나타냅니다. 접근 한정자는 **protected**(동일한 패키지에서 접근 가능) 또는 **private**(같은 클래스에서만 접근 가능)일 수도 있습니다. 메서드 앞의 **정적**은 클래스의 특정 인스턴스 없이 메서드를 호출할 수 있음을 나타냅니다. **void**는 메서드가 아무 것도 반환하지 않음을 나타냅니다. 문자열을 콘솔에 인쇄하려면. System.out.println 명령이 사용됩니다. 이 명령에서 *System* 클래스에는 *println* 메서드를 포함하는 *PrintStream* 클래스의 인스턴스인 정적 필드 *out*이 있습니다.

Java 파일의 파일 이름은 클래스 이름과 같아야 합니다. 따라서 예제 코드의 Java 파일 이름은 *ExampleApp.java*가 됩니다.

## 참조 ##

- [자바(프로그래밍 언어) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

