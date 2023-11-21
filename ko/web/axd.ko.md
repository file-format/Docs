{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD 파일 - ASP.NET 웹 처리기 파일 형식",
  "description" :"AXD 파일이 무엇인지, 그리고 AXD 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## .AXD 파일이란?

AXD 파일은 ASP.NET에서 포함된 리소스 요청을 처리하고 검색하는 데 사용되는 웹 설정 파일입니다. 이는 이미지, JavaScript([.JS](/ko/web/js/)) 파일 및 [.CSS](/ko/web/css/) 파일과 같은 포함된 리소스를 검색하기 위한 지침으로 구성됩니다. AXD 파일은 클라이언트 측 페이지에 리소스를 삽입하는 데 사용됩니다. 이를 통해 클라이언트 페이지는 표준 방식으로 서버의 이러한 리소스에 액세스할 수 있습니다.

## AXD 파일 형식

AXD 파일은 서버 측에 바이너리 파일로 저장됩니다. 이는 웹 서버에 대한 특정 요청에 대한 응답을 생성하는 구성 요소인 ASP.NET의 웹 처리기 파일을 나타냅니다. AXD 파일은 클라이언트 측 페이지 요청을 기반으로 응답을 생성하기 전에 사용자 정의 처리를 수행합니다. 이는 일반적으로 **WebResource.axd** 파일로 저장됩니다.

### WebResource.axd 파일이란 무엇인가요?

대부분의 ASP.NET 프로젝트는 AXD 파일을 클라이언트 측 페이지에서 어셈블리에 포함된 리소스를 다운로드할 수 있는 WebResource.axd 파일로 저장합니다. WebResources.axd 핸들러가 캐시되지 않기 때문에 디버그 모드에서 실행하는 경우 애플리케이션 성능이 저하될 수 있습니다.

## 참고자료

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

