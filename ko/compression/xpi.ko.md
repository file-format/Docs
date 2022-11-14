{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - 크로스 플랫폼 설치 프로그램 패키지 파일",
  "description":"XPI 파일을 만들고 열 수 있는 API와 XPI 파일 형식에 대해 알아보세요.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## .XPI 파일이란?

XPI 파일은 파일 크기를 줄이기 위해 압축된 설치 아카이브입니다. 플러그인 및 추가 기능 파일 설치를 위해 Mozilla 응용 프로그램에서 사용합니다. 여기에는 여러 데이터 파일과 함께 파일 루트에 설치 스크립트 또는 매니페스트가 포함됩니다. XPI 파일에는 사용자가 Firefox 브라우저, Thunderbird 또는 SeaMonkey의 일부가 되기 위해 설치할 수 있는 테마, 툴킷 또는 Firefox 플러그인이 포함될 수 있습니다.

## XPI 파일 형식 - 추가 정보

XPI 파일은 여러 파일을 단일 압축 파일로 결합하는 [ZIP](/ko/compression/zip/) 아카이브로 디스크에 저장됩니다. XPI 파일 내부의 파일에는 JS와 같은 설치 스크립트 파일과 [CSS](/ko/web/css/), [HTML](/ko/web/html/) 및 [JSON](/ko/web/json/)과 같은 웹 파일이 포함될 수 있습니다. ). 경우에 따라 애드온에서 아이콘으로 사용할 [PNG](/ko/image/png/) 이미지 파일도 포함될 수 있습니다.

### XPI 파일의 내용을 보는 방법은 무엇입니까?

XPI 파일은 실제로 다음 단계를 사용하여 내용을 볼 수 있는 ZIP 아카이브입니다.

* 파일 확장자를 XPI에서 ZIP으로 변경
* WinZip(Windows, Mac), 7-Zip(Windows) 또는 Apple Archive Utility(Mac)와 같은 표준 압축 해제 유틸리티를 사용하여 파일의 내용을 추출합니다.

### Firefox Android에 XPI 파일 설치

대부분의 사람들은 XPI 파일을 Android 장치의 Firefox에 설치할 수 있는지 알고 싶어 합니다. Android에서는 파일을 찾아 Firefox로 열어 XPI 파일에서 추가 기능을 설치할 수 있습니다.

## 참고문헌

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [XPI 파일 확장자를 어떻게 열 수 있나요?](https://support.mozilla.org/en-US/questions/1009049)

