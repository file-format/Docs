{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - MSIX 파일이란 무엇입니까?",
  "description":"MSIX 파일을 만들고 열 수 있는 API와 MSIX 파일에 대해 알아보세요.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## .MSIX 파일이란?

MSIX 파일은 Windows 10에서 응용 프로그램을 만들고 배포하는 데 사용되는 Windows 앱 패키징 형식입니다. 이는 [APPX](/ko/programming/appx/) 및 마지막으로 단계적으로 제거될 MSI와 비교하여 최신 패키지 파일 형식입니다. 이 새로운 파일 형식으로. Win32, WPF 및 Windows Forms 앱 배포에 사용할 수 있습니다. MSIX 파일은 안정적이며 대상 네트워크 및 디스크 공간을 최적화합니다. 개발자는 이를 사용하여 Microsoft Store(이전에는 Windows Store로 알려짐)를 통해 최종 사용자에게 프로그램을 배포합니다.

## MSIX 파일 형식 - 추가 정보

MSIX 파일은 [ZIP](/ko/compression/zip/) 압축되며 모든 파일은 패키지된 파일 내에 포함됩니다. MSIX 파일에는 앱 관련 파일 외에도 앱 설치와 관련된 정보가 포함된 [.xml](/ko/web/xml/) 구성 파일이 포함되어 있습니다.

## MSIX 패키지 내부에는 무엇이 있습니까?

MSIX 패키지는 다음 파일로 구성됩니다.

* `AppxBlockMap.xml` - 패키지 블록 맵 파일로 알려진 이 파일은 패키지에 저장된 각 데이터 블록에 대한 인덱스 및 암호화 해시가 있는 앱 파일 목록을 포함하는 XML 문서입니다.
* `AppxManifest.xml` - MSIX 앱의 배포, 표시 및 업데이트에 필요한 정보가 포함된 XML 문서입니다. 이 정보에는 패키지 ID, 패키지 종속성, 필수 기능, 시각적 요소 및 확장성 포인트가 포함됩니다.
* `AppxSignature.p7x` - 패키지 서명 시 생성되는 파일. 모든 MSIX 패키지는 설치하기 전에 서명해야 합니다. AppxBlockmap.xml을 사용하면 플랫폼에서 패키지를 설치하고 유효성을 검사할 수 있습니다.

## 참고문헌

* [MSIX 개요](https://docs.microsoft.com/en-us/windows/msix/overview)
* [Microsoft Visual Studio를 사용하여 APPX 파일 만들기](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

