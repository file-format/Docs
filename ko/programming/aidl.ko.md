{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL 파일 - Android 인터페이스 정의 언어 파일",
  "description":"AIDL 파일을 생성하고 열 수 있는 예제와 API를 통해 AIDL 파일 형식이 무엇인지 알아보세요.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AIDL 파일이란?

AIDL(Android Interface Definition Language) 파일을 사용하면 Android 개발자가 서로 다른 앱 간에 통신을 설정할 수 있습니다. 프로그래밍 인터페이스를 기반으로 클라이언트와 서비스 모두 IPC(프로세스 간 통신)를 사용하여 통신하는 데 동의합니다. AIDL 파일에는 이러한 인터페이스를 정의하기 위한 [Java](/ko/programming/java/) 소스 코드와 앱 간의 통신을 위한 계약이 포함되어 있습니다.

Google Android Studio 또는 Microsoft 메모장 및 메모장++과 같은 텍스트 편집기를 사용하여 AIDL 파일을 열 수 있습니다.

## AIDL 파일 형식 - 추가 정보

AIDL은 앱 간의 통신을 위한 인터페이스를 포함하는 텍스트 파일입니다. Android OS는 한 프로세스가 다른 프로세스의 메모리에 액세스하는 것을 허용하지 않습니다. 이를 통해 프로세스는 기본 운영 체제에 대한 이해를 위해 개체를 기본 개체로 분할하고 개발자를 위한 통신 구조 프로세스를 설정합니다.

### AIDL은 어떤 데이터 유형을 지원합니까?

AIDL은 기본적으로 다음 데이터 유형을 지원합니다.

* Java 프로그래밍 언어의 모든 기본 유형(예: int, long, char, boolean 등)
* 끈
* 문자 시퀀스
* 목록
* 지도

## AIDL 파일 예

다음은 AIDL 파일의 예입니다.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## 참고문헌

* [안드로이드 인터페이스 정의 언어(AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

