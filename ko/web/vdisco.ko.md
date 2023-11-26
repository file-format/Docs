{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO 파일 - DISCO 동적 검색 문서 파일 형식",
  "description":"VDISCO 파일이 무엇인지 알아보세요.",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## VDISCO 파일이란 무엇입니까?

VDISCO 파일은 웹 서비스에서 Microsoft Visual Studio가 사용하는 검색 파일입니다. URL, 네임스페이스, 메소드 등 사용 가능한 웹 서비스에 대한 정보를 제공합니다. VDISCO 파일은 [DISCO](/ko/web/disco/) 파일 형식과 유사하지만 런타임 시 생성됩니다. 이는 웹 서비스 애플리케이션에 저장되며 Visual Studio에서 프로젝트의 웹 서비스를 동적으로 검색하고 사용하는 데 사용됩니다. VDISCO 파일은 실제 웹 서비스 코드가 포함된 [.asmx](/ko/web/asmx/) 파일과 함께 사용됩니다.

Microsoft Notepad, Github Atom 및 Apple TextEdit과 같은 텍스트 편집기에서 VDISCO 파일을 열 수 있습니다. 또한 작업을 위해 Microsoft Visual Studio 2012 이상에서 열 수도 있습니다.

## VDISCO 파일 형식

VDISCO 파일은 데이터 구성 및 게시를 위한 범용 형식인 [XML](/ko/web/xml/) 파일 형식으로 저장되고 호스팅됩니다. 여기에는 각 태그에 해당 정보 값이 포함된 표준 XML 태그의 서비스 URL, 네임스페이스 및 메소드가 포함됩니다.

## 참고자료

* [디스코](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [웹 서비스 검색](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [DiscoveryClient 클래스의 C# 예](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

