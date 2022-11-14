{
  "date" : "2021-01-21",
  "keywords" :[ "otp 파일", "otp 파일 형식", "otp 파일이란", "파일", "otp 예제", "otp 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument 프레젠테이션 템플릿",
  "description":"OTP 파일 형식과 OTP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## .OTP 파일이란?

확장자가 .otp인 파일은 OASIS OpenDocument 표준 형식의 응용 프로그램에서 만든 프레젠테이션 템플릿 파일을 나타냅니다. 이러한 파일의 내용에는 텍스트, 이미지, 모양, 멀티미디어 콘텐츠, 전환 효과 및 기타 슬라이드 요소가 포함된 슬라이드 형식의 프레젠테이션 정보가 포함됩니다. 이러한 템플릿 파일은 템플릿 자체에 저장된 스타일 정보를 기반으로 신속하게 새 프레젠테이션을 만드는 데 사용됩니다. OTP 파일은 OpenOffice 제품군과 함께 제공되는 Impress 및 Microsoft PowerPoint와 같은 여러 응용 프로그램을 사용하여 만들고 저장할 수 있습니다. OTP 파일 형식은 Microsoft PowerPoint 템플릿 파일 [.pot](/ko/presentation/pot/) 및 [.potx](/ko/presentation/potx/)와 유사합니다.

## OTP 파일 형식

OTP 파일 형식은 [ZIP](/ko/compression/zip/) 형식의 단일 압축 패키지에 여러 하위 문서 모음과 단일 XML 문서로 문서 표현을 지원하는 OpenDocument 표준을 기반으로 합니다. 파일의 내용은 함께 패키지된 여러 xml 파일로 배포됩니다. 이러한 여러 개의 [XML](/ko/web/xml/) 파일에는 아래와 같이 문서의 스타일, 내용, 메타 정보 및 설정에 대한 정보가 포함되어 있습니다.

* `content.xml` – 문서 콘텐츠 및 콘텐츠에 사용되는 자동 스타일.
* `styles.xml` – 문서 내용에 사용되는 스타일 및 스타일 자체에 사용되는 자동 스타일.
* `meta.xml` – 작성자 또는 마지막 저장 작업 시간과 같은 문서 메타 정보입니다.
* `settings.xml` – 창 크기 또는 프린터 정보와 같은 응용 프로그램별 설정입니다.

## 참고문헌

* [OpenDocument - 위키피디아 작성](https://en.wikipedia.org/wiki/OpenDocument)

