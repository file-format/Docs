{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","arsc 파일이란","arsc 파일을 여는 방법", "확장자", "파일", "arsc 파일","arsc 파일 형식", "arsc 파일 확장자" ,"arsc 파일 예"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android 패키지 리소스 테이블 파일",
  "description":"ARSC 파일 형식과 ARSC 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## .ARSC 파일이란?

ARSC 파일은 애플리케이션의 리소스 목록을 테이블 형식으로 포함하는 Android 리소스 테이블 파일입니다. 여기에는 리소스 이름, 속성 및 ID와 같은 정보가 포함됩니다. ARSC 파일은 이러한 Android 앱을 설치하는 데 사용되는 APK 패키지의 일부입니다. Android 애플리케이션의 이미지, 레이아웃, 스타일 및 문자열과 같은 모든 리소스는 APK 파일이 생성될 때 바이너리 파일로 변환됩니다. ARSC 파일은 또한 모든 프로그램의 컴파일된 리소스 및 해당 ID 목록을 포함하는 동일한 위치에 생성됩니다.

## ARSC 파일 형식

.arsc 확장 파일은 ANT(Eclipse) 또는 Gradle(AS)과 같은 컴파일러가 Android 애플리케이션 코드를 컴파일하여 [APK](/ko/compression/apk/) 파일을 생성한 후 생성되는 바이너리 파일입니다. WinZip과 같은 보관 유틸리티를 사용하여 APK 파일을 추출하여 해당 내용을 볼 수 있습니다. 이 파일은 컴파일된 Java 클래스 파일(예: classes.dex)입니다. 이 외에도 다음과 같은 메타 정보가 포함된 ARSC 파일이 포함되어 있습니다.

* XML 노드
* 속성
* 리소스 ID

APK 파일의 리소스는 리소스 ID로 참조되는 반면 속성은 런타임에 값으로 확인됩니다. Android aapt 도구는 빌드 시 파일에 정의된 모든 리소스를 수집하고 리소스 ID를 할당합니다. 컴파일된 리소스에 식별자가 할당된 후 R.java 파일은 resources.arsc뿐만 아니라 소스 코드에서 생성됩니다.

## 참고문헌

* [바이너리 리소스 테이블 구조](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

