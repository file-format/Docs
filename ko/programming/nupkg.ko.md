{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG 파일 - NuGet 패키지 파일",
  "description":"NUPKG 파일 형식과 NUPKG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## .NUPKG 파일이란?

NUPKG 파일은 .NET 프로젝트에서 사용할 패키지를 만들기 위해 NuGet 소프트웨어에서 사용할 소스 코드가 포함된 패키지 파일입니다. NuGet 패키지 관리자 구성 요소는 리포지토리를 호스팅하는 온라인 패키지에서 패키지를 가져오기 위해 Microsoft Visual Studio의 일부로 설치됩니다. NUPKG 파일은 개발자가 개발 패키지를 수동으로 다운로드하여 설치하는 대신 NuGet 패키지 관리자를 사용하여 [Nuget.org](https://nuget.org)에서 최신 패키지를 가져오는 데 도움이 됩니다. NUPKG 파일은 NUSPEC 파일에서 빌드되며 가져올 때 사용자 시스템에 패키지를 설치합니다.

## NUPKG 파일 형식

NUPKG 파일은 내부에 패키지 라이브러리를 포함하는 [ZIP](/ko/compression/zip/) 아카이브입니다. 다운로드하면 .zip으로 이름을 바꾸고 WinZIP, 7-Zip 및 Apple Archive Utility와 같은 표준 zip 유틸리티로 압축을 풀 수 있습니다.

## 참조

* [Nuget.org](https://nuget.org)
* [빠른 시작: Visual Studio에서 패키지 설치 및 사용(Windows만 해당)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- 사진관)
* [Nuget 패키지 생성 및 게시 방법](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

