---
date: 2019-10-11
keywords: kt, .kt, kotlin 파일 형식, kotlin 파일 여는 방법, kotlin 파일 실행 방법, .kt 파일 형식, kt 파일, kotlin 파일 확장자, .kt 확장자, kotlin 대 Java
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT 파일 형식
linktitle: KT
description: "KT 파일을 생성하고 열 수 있는 KT 파일 형식과 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## .KT 파일이란? ##

Kotlin으로 작성된 소스 코드는 일반적으로 **Kotlin 파일 확장자**로 알려진 .kt 확장자로 저장됩니다. Kotlin은 [Java](/ko/programming/java/)와 완벽하게 상호 운용할 수 있도록 JetBrains에서 개발한 범용 크로스 플랫폼 프로그래밍 언어입니다. Kotlin 상표는 Kotlin 재단의 보호를 받습니다.

Kotlin은 2019년 5월 7일 Google에서 Android 앱 개발을 위한 기본 프로그래밍 언어로 발표했습니다. Android Studio 3.0은 2017년 10월 Android 앱 개발의 대안으로 Kotlin을 지원하기 시작했습니다.

## Kotlin KT 파일 형식의 간략한 역사##

Kotlin은 2011년 7월 JetBrains에서 JVM용 새 프로그래밍 언어로 공개되었습니다. JetBrains의 책임자인 Dmitry Jemerov는 Scala를 제외하고는 대부분의 언어에 원하는 기능이 없지만 Scala의 느린 컴파일이 단점이라고 말했습니다. Kotlin의 주요 목표 중 하나는 Java만큼 빠르게 컴파일하는 것이었습니다. Kotlin 프로젝트는 2012년 2월 Apache 2 라이선스에 따라 오픈 소스되었습니다.

Kotlin 버전 1.0은 2015년 2월 15일에 출시되었습니다. Android는 Google I/O 2017에서 Android에서 Kotlin에 대한 최고 수준의 지원을 발표했습니다. Kotlin 1.2는 2017년 11월 28일에 JVM과 JavaScript 플랫폼 간에 코드를 공유할 수 있는 기능으로 출시되었습니다. Kotlin 1.3은 비동기 프로그래밍을 지원하는 2018년 10월 29일에 출시되었습니다. Google은 2019년 5월 7일 Kotlin을 Android 앱 개발을 위한 기본 프로그래밍 언어로 발표했습니다. Kotlin 1.4는 Swift/Objective-C와의 상호 운용성을 지원하기 위해 약간의 변경 사항과 함께 2020년 8월에 출시되었습니다.

## 코틀린 구문 ##

Kotlin은 Java보다 낫도록 설계되었지만 Java 코드와 상호 운용 가능하므로 Java에서 Kotlin으로 점진적으로 마이그레이션할 수 있습니다.

* Kotlin에서 세미콜론은 선택 사항입니다. 새 줄은 명령문의 끝을 나타내기에 충분합니다.
* Kotlin은 *val* 키워드로 정의된 읽기 전용 변수와 *var* 키워드로 정의된 가변 변수의 두 가지 유형의 변수를 지원합니다.
* 수업은 기본적으로 비공개이며 최종 수업입니다. 클래스에서 파생시키려면 기본 클래스를 *open* 키워드로 선언해야 합니다.
* Kotlin은 절차적 프로그래밍도 지원합니다.
* Kotlin 프로그램의 진입점은 Java, C# 등과 유사한 "메인" 기능입니다.

### 구문 예 ###

다음은 Kotlin 구문의 예입니다.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

위의 코드에서 **fun** 키워드는 main이라는 함수를 정의합니다. 함수 내에서 읽기 전용 변수 'audience'는 **val** 키워드로 선언됩니다. **println** 메서드를 사용하면 "Hello World from Kotlin"이 콘솔에 인쇄됩니다. 대상 변수의 값은 **$** 기호가 있는 문자열에 삽입됩니다.

## 코틀린 대 자바
Kotlin은 많은 고급 기능을 제공하는 Android 앱을 작성하기 위한 공식 언어이지만 많은 전문 Java 개발자는 여전히 Kotlin으로 전환하는 데 관심을 보이지 않습니다. 그들은 Java만으로 모든 것을 할 수 있다고 생각합니다. 따라서 다음은 Java 개발자가 전환하도록 설득할 수 있는 두 기술 간의 비교입니다.

| 매개변수 | 자바 | 코틀린 |
|--------------------|-----------|---------------- -|
| 싱글톤 개체 | √ | √ |
| 와일드카드 유형 | √ | ㅇ |
| 편집 | 바이트코드 | 가상 머신 |
| 람다 식 | ㅇ | √ |
| 불변 배열 | ㅇ | √ |
| 비공개 필드 | √ | ㅇ |
| 스마트 캐스트 | ㅇ | √ |
| Null 안전 | ㅇ | √ |
| 정적 멤버 | √ | ㅇ |

## 참조 ##

- [Kotlin(프로그래밍 언어) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

