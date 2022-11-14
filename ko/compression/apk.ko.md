{
  "date" : "2019-10-11",
  "keywords" :[ "apk 파일", "apk 파일 형식", "apk 파일이란", "파일", "apk 예제", "apk 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - APK 파일이란 무엇입니까?",
  "description":"APK 파일을 생성하고 열 수 있는 API와 APK 파일이 무엇인지 알아보세요.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## APK 파일이란?

확장자가 .apk인 파일은 Android 기기에 앱(애플리케이션)을 설치하는 데 사용되는 Google Android 앱 파일입니다. 공식 IDE Google Android Studio를 사용하여 실행 파일로 생성되며 Google Play 스토어에 업로드되어 최종 사용자가 다운로드하여 설치할 수 있습니다. Google Play 스토어에 게시하기 전에 APK 파일을 생성하여 수동 설치에 사용할 수 있습니다. 이렇게 하면 생성된 APK 패키지 파일의 기능과 동작을 테스트하는 데 도움이 됩니다. 따라서 APK 파일이 신뢰할 수 있는 출처에서 제공되고 악성코드가 포함되어 있지 않은지 확인해야 합니다.

## APK 파일 형식

APK 파일은 모든 ZIP 파일 열기 소프트웨어로 열 수 있는 [ZIP](/ko/compression/zip/) 파일 형식으로 압축되어 패키징됩니다. 이러한 파일의 .apk 확장자는 .zip으로 이름을 바꾸고 ZIP 응용 프로그램에서 파일을 열거나 내용을 추출할 수 있습니다.

## APK 패키지 콘텐츠

단일 APK 파일에는 설치 및 실행에 필요한 모든 파일이 포함되어 있습니다. ZIP 응용 프로그램으로 압축을 푼 APK 파일에는 다음 파일과 폴더가 포함되어 있습니다.

* `META-INF/`: 아카이브의 매니페스트 파일, 서명 및 리소스 목록이 포함된 디렉토리
* `lib/`: armeabi-v7a, x86, arm64-v8a 등과 같은 특정 플랫폼과 관련된 컴파일된 코드가 포함된 디렉터리입니다.
* `res/`: 이미지와 같은 컴파일되지 않은 리소스를 포함하는 디렉토리
* `assets/`: AssetManager에서 검색할 수 있는 애플리케이션 자산을 포함하는 디렉토리.
* `androidManifest.xml`: APK 파일의 이름, 버전 정보 및 내용을 포함합니다.
* `classes.dex`: Dalvik 가상 머신 및 Android 런타임에서 실행할 수 있는 컴파일된 Java 클래스입니다.
* `resources.arsc`: 문자열과 같은 컴파일된 리소스 파일

## Android 기기에 APK 파일을 설치하는 방법은 무엇입니까?

Android 기기에 APK 파일을 설치하려면 다음 단계를 사용할 수 있습니다.

1. 웹 브라우저를 사용하여 APK 다운로드
2. 탭하세요. 그러면 기기의 상단 표시줄에서 다운로드되는 것을 볼 수 있습니다.
3. 다운로드가 완료되면 다운로드를 열고 APK 파일을 탭한 다음 메시지가 표시되면 예를 탭합니다.

다음 단계에 따라 기기에 앱 설치가 시작됩니다.

## 참고문헌

* [APK 파일 형식](https://en.wikipedia.org/wiki/Android_application_package)

