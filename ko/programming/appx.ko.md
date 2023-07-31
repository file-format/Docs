{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - APPX 파일이란?",
  "description":"APPX 파일 형식과 APPX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## .APPX 파일이란?

APPX 파일은 응용 프로그램의 배포 및 설치에 사용되는 배포 가능한 패키지 파일 형식입니다. Microsoft Windows Store에 게시하기 위해 Windows 8과 함께 도입되었습니다. 여기에는 Windows 응용 프로그램을 설치하는 데 필요한 모든 파일이 포함되어 있습니다. 여기에는 메타데이터, 파일 및 자격 증명 정보가 포함됩니다. 보다 현대적인 패키징 파일 형식은 현재 APPX와 비교하여 더 일반적으로 사용되는 MSIX입니다.

## APPX 파일 형식 - 추가 정보

APPX 파일은 [ZIP](/ko/compression/zip/) 파일 형식의 압축 파일로 저장됩니다. 이렇게 하면 전체 패키지를 Microsoft Store에 쉽게 업로드할 수 있는 축소된 파일 크기의 보관 파일로 만들 수 있습니다.

## APPX 파일의 파일을 보는 방법은 무엇입니까?

APPX 파일 내의 내용이나 파일을 보려면 다음 단계를 따라야 합니다.

1. APPX 파일은 압축된 ZIP 파일로 저장되므로 파일 이름을 .zip 확장자로 변경합니다.
1. 7-Zip, WinZip 또는 WinRAR와 같은 압축 해제 도구를 사용하여 APPX 파일에 포함된 파일의 압축을 풉니다.

## APPX 파일을 만드는 방법은?

APPX 파일을 만드는 데 사용할 수 있는 두 가지 방법이 있습니다.

1. MakeApp.exe 사용 - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)를 사용하여 둘 다 생성 앱 패키지(.msix 또는 .appx) 및 앱 패키지 번들 파일 .msixbundle 또는 .appxbundle). 또한 앱 패키지에서 파일을 추출할 수 있습니다. MakeApp.exe는 Windows 10 SDK에서 사용할 수 있으며 명령 프롬프트에서 사용할 수 있습니다.
1. Microsoft Visual Studio 사용 - 개발자는 일반적으로 Microsoft Visual Studio를 사용하여 [APPX 파일 생성](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)을 사용합니다. 애플리케이션 개발이 완료되고 앱을 게시할 준비가 되면 Visual Studio 내에서 앱을 게시하여 APPX 패키지 파일을 생성할 수 있습니다.

## 참고문헌

* [MakeAppx.exe로 MSIX 패키지 또는 번들 생성](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Microsoft Visual Studio를 사용하여 APPX 파일 만들기](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

