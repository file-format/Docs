{
  "date" : "2019-10-11",
  "keywords" :[ ".swf", "SWF", "Apple swift", "파일", "확장자", "파일 형식", "apple swift 자습서", "프로그래밍 가이드"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SWIFT - Apple 소스 코드 파일",
  "description":"SWIFT 파일 형식과 SWIFT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SWIFT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## 스위프트 파일이란?

.swift 확장자를 가진 파일은 macOS, iOS, tvOS 및 그 이상을 위한 소프트웨어 응용 프로그램 및 앱을 작성하기 위해 Apple에서 도입한 SWIFT 프로그래밍 언어를 나타냅니다. SWIFT 이전에는 Objective-C가 애플리케이션 작성을 위한 주요 프로그래밍 언어였습니다. Mac, iPhone, iPad, Apple Watch 및 Apple TV용 앱을 만들기 위한 완전한 개발자 도구 세트인 Xcode와 함께 사용할 수 있습니다. SWIFT는 더 강력하고 상호작용적이며 표현력이 뛰어나며 성능 저하 없이 설계상 더 안전한 기능을 제공합니다. Apple Xcode 외에 모든 텍스트 편집기에서 편집을 위해 Swift 파일을 열 수 있습니다. Apple의 운영 체제, Linux, Windows 및 Android를 지원합니다.

## 약력

* 2010년 중반에 Apple의 다른 프로그래머의 기여로 Chris Lattner가 개발을 시작했습니다.
* SWIFT로 작성된 최초의 공식 앱은 2014년 6월 2일 Apple WorldWide Developer Conference(WWDC)에서 출시되었으며 언어의 베타 버전은 등록된 Apple 개발자에게 출시되었습니다.
* Swift 1.0은 2014년 9월 9일 iOS의 Xcode와 함께 출시되었습니다.
* Swift 1.1은 2014년 10월 22일 Xcode 6.1 출시와 함께 출시되었습니다.
* Swift 1.2는 Xcode 6.3과 함께 2015년 4월 8일에 출시되었습니다.
* Swift 2.0은 WWDC 2015에서 발표되었으며 2015년 9월 21일 App Store에서 앱을 퍼블리싱할 수 있게 되었습니다.
* Swift 3.0은 2016년 9월 13일에 출시되었습니다.
* Swift 4.0은 2017년 9월 19일에 출시되었습니다.
* Swift 4.1은 2018년 3월 29일에 출시되었습니다.
* Swift 언어는 Apache 2.0 라이선스에 따라 지원 라이브러리, 디버거 및 패키지 관리자와 함께 2015년 12월 3일에 오픈 소스되었습니다. 프로젝트는 [Swift.org](https://swift.org/)에서 호스팅되었으며 소스 코드는 [GitHub](https://github.com/apple/swift)에서 호스팅됩니다.
* WWDC 2019에서 Apple은 모든 Apple 플랫폼에서 UI 구조 설계를 위한 SwiftUI 프레임워크를 발표했습니다.

## Swift 파일 형식 - 추가 정보

Swift 파일은 모든 텍스트 편집기로 열 수 있는 일반 텍스트 파일입니다. 신속한 파일을 열고 편집하는 데 사용되는 기본 텍스트 편집기는 Apple의 Xcode입니다. Swift의 많은 부분이 C 및 Objective-C를 사용하여 개발하는 애플리케이션에 익숙합니다. Swift 문서는 Swift를 사용하여 코드를 작성하기 위한 자세한 [애플리케이션 개발 가이드](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/)를 제공합니다.

## 스위프트 언어 기능

Swift는 다음과 같은 특징에 따라 다른 프로그램 언어와 구별됩니다.

`Modern` - 명명된 매개변수가 깔끔한 구문으로 표현되어 Swift의 API를 훨씬 더 쉽게 읽고 유지 관리할 수 있습니다. 더 좋은 점은 세미콜론을 입력할 필요조차 없다는 것입니다.

'안전' - 변수는 항상 사용하기 전에 초기화되고, 배열과 정수는 오버플로가 있는지 확인하고, 메모리는 자동으로 관리되며, 메모리에 대한 독점적 액세스는 많은 프로그래밍 실수로부터 보호합니다.

'빠르고 강력한' - 믿을 수 없을 정도로 고성능 LLVM 컴파일러 기술을 사용하여 Swift 코드는 최신 하드웨어를 최대한 활용하는 최적화된 네이티브 코드로 변환됩니다.

`소스 및 바이너리 호환성` - 이전 버전의 Swift로 개발된 애플리케이션은 새 릴리스와 호환되며 소스 코드를 다시 컴파일할 필요가 없습니다. Swift 5 출시와 함께 Swift 라이브러리는 앞으로 모든 OS 릴리스에 포함됩니다. 이렇게 하면 현재 및 향후 OS 릴리스를 대상으로 하는 앱에 Swift 라이브러리가 포함되지 않습니다.

'오픈 소스' - Swift는 Swift 커뮤니티 회원의 수백 가지 기여가 있는 오픈 소스입니다. 모든 사람이 공개적으로 사용할 수 있는 강력한 버그 추적기, 포럼 및 정기 개발 빌드가 지원합니다.

## 참고문헌
* [Swift - GitHub](https://github.com/apple/swift)
* [스위프트 - 위키피디아](https://en.wikipedia.org/wiki/Swift_(programming_language))

