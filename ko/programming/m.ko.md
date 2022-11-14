{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab 소스 코드 파일",
  "description":"Matlab .m 소스 코드 파일과 MF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab 소스 코드 파일

## M(Matlab) 파일이란?

확장자가 .m인 파일은 분석, 알고리즘 개발 및 시뮬레이션 모델링에 사용되는 프로그래밍 및 수치 계산 플랫폼인 Matlab에서 사용하는 소스 코드 파일입니다. 다른 프로그래밍 파일 형식과 마찬가지로 M 파일에는 Matlab 명령을 실행하여 그래프를 플로팅하고 시뮬레이션 및 기타 수학 연산을 실행하는 소스 코드가 포함되어 있습니다. 단일 Matlab 시뮬레이션은 스크립트, 클래스, 함수 또는 선언에서 애플리케이션을 분류할 수 있는 여러 .m 파일에 걸쳐 있을 수 있습니다. Matlab M 파일은 모든 텍스트 편집기로 열 수 있습니다.

## Matlab M 파일 형식 - 추가 정보

Matlab .m 파일은 Matlab 프로그래밍 언어의 프로그래밍 코드가 포함된 텍스트 파일입니다. 이것은 모든 텍스트 편집기에서 열고 편집할 수 있으며 Matlab 소프트웨어에서 실행하기 위해 다시 저장할 수 있습니다. Matlab 자체에는 코드, 출력 및 서식이 지정된 텍스트의 조합인 스크립트를 만드는 데 사용되는 라이브 편집기가 포함되어 있습니다.

### Matlab 함수 파일

다른 프로그래밍 언어와 마찬가지로 특정 작업만 수행하는 함수의 정의만 포함하는 .m 파일을 만들 수 있습니다. 이러한 파일도 .m 확장자로 저장되며 해당 기능과 관련된 기능만 구현합니다.

### .M 파일 예

다음은 높이 h에서 물체를 떨어뜨리는 데 걸린 시간을 계산하는 Matlab 함수 파일 예제입니다.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Matlab 편집기 또는 다른 .m 파일에서 이 함수를 호출하려면 다음 코드를 사용할 수 있습니다.
```C++
TimeToGround(100)
```

## 참고문헌

* [Matlab - 지원되는 파일 형식](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Matlab 사용하기](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C 구현 파일

## M(Objective-C) 파일이란?

M 파일은 OS X 및 iOS용 소프트웨어 응용 프로그램을 작성하는 데 사용되는 프로그래밍 언어인 Objective-C 언어로 작성된 클래스의 소스 코드가 포함된 구현 파일이라고도 합니다. Objective-C는 이러한 플랫폼을 위해 Apple의 주요 API인 Cocoa 및 Cocoa Touch에서 사용하는 주요 프로그래밍 언어입니다. 이 언어로 개발된 단일 소프트웨어 응용 프로그램에는 프로그램 클래스의 구현을 포함하는 여러 .m 파일이 포함될 수 있습니다. Apple XCode, jEdit 및 기타 일반 텍스트 편집기를 사용하여 열 수 있습니다.

## Objective-C M 파일 형식 - 추가 정보

M 파일은 Objective-C의 프로그래밍 구문을 사용하여 일반 텍스트 형식으로 작성됩니다. 클래스의 모든 메서드는 이러한 구현 파일에 필요한 모든 코드로 정의되어야 합니다. 이러한 구현 M 파일은 요구 사항에 따라 하나 이상의 .h 헤더 파일을 가져올 수 있습니다. import 문은 컴파일러에게 이 구현 파일에 속한 헤더 파일을 찾을 위치를 알려줍니다. import 문은 다음과 같이 작성됩니다.

```C++
#import "network.h"
```

각 M 파일 구현은 `@implementation` 지시문으로 시작하고 그 뒤에 구현 클래스 파일 이름이 옵니다. 그런 다음 헤더 파일에 선언된 모든 메서드 구현이 이어집니다.

### M 파일 형식 예

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## 참고문헌
* [오브젝티브 C 소개](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C 가이드](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

