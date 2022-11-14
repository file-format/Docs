{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DISCO 파일 - DISCO 디스커버리 문서 파일 형식",
  "description":"DISCO 파일이 무엇이며 DISCO 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## .DISCO 파일이란?

DISCO 파일은 웹 서비스를 게시하고 검색하는 데 사용되는 Microsoft 검색 파일 형식입니다. XML 파일 형식으로 저장되며 웹 서비스 검색 도구가 사용 가능한 [XML](/ko/web/xml/) 서비스를 설명하는 하나 이상의 관련 문서를 찾거나 검색할 수 있도록 합니다. DISCO 파일은 검색 문서, [XSD](https://docs.fileformat.com/programming/xsd/) 스키마 및 서비스 설명과 같은 정보를 저장합니다. XML 웹 서비스는 이 정보를 사용하여 주어진 URL에서 사용 가능한 XML 웹 서비스를 얻습니다.

## DISCO 파일 형식 - 추가 정보

DISCO 파일은 XML 파일 형식으로 저장됩니다. Microsoft Studio와 같은 Microsoft ASP.NET 개발 소프트웨어와 함께 제공되는 Microsoft Discovery Tool(DISCO.exe)은 DISCO 파일을 사용하여 특정 URL의 DiscoveryDocument에 나열된 XML 웹 서비스에 대한 세부 정보를 검색합니다. Microsoft는 .NET 프레임워크에서 검색 파일 읽기를 지원합니다.

## 참고문헌

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894?tab=Overview)
* [웹 서비스 검색](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [DiscoveryClient 클래스의 C# 예제](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

