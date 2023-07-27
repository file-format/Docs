{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","asmx 파일", "asmx 파일 형식", "asmx 파일 형식", "파일", "유형", "asmx 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET 웹 서비스 파일",
  "description" :"ASMX 파일이 무엇이며 ASMX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASMX 파일이란?

확장자가 .asmx인 파일은 SOAP(Simple Object Access Protocol)를 사용하여 인터넷을 통해 두 개체 간의 통신을 제공하는 ASP.NET 웹 서비스 파일입니다. 들어오는 요청을 처리하고 응답을 반환하기 위해 Windows 기반 웹 서버에 서비스로 배포됩니다. ASP.NET 웹 페이지의 시각적 표시를 위한 코드가 포함된 [ASPX](/ko/web/aspx/) 파일과 달리 ASMX 파일은 백그라운드에서 서버에서 실행되며 데이터베이스 연결, 데이터 검색 및 반환과 같은 다양한 작업을 수행합니다. 요청이 이루어진 형식입니다. 이들은 특히 XML 웹 서비스에 사용됩니다.

## ASMX 파일 형식

ASMX 파일은 일반 텍스트 형식이며 Microsoft Visual Studio 또는 텍스트 편집기와 같은 응용 프로그램에서 열거나 편집할 수 있습니다. Microsoft의 독점 파일 형식이며 웹 서비스 생성을 위한 잘 정의된 구문을 가지고 있습니다. SOAP XML 형식의 ASMX 파일에 의한 응답에는 다음 요소가 있습니다.

* `Envelop` - XML 문서를 SOAP 메시지로 식별하는 루트 요소입니다.
* '헤더' - 인증 데이터와 같은 애플리케이션별 정보를 포함하는 선택적 요소입니다. Header 요소가 있는 경우 Envelope 요소의 첫 번째 자식 요소여야 합니다.
* '본문' - 수신자를 위한 SOAP 메시지를 포함합니다.
* `Fault` - 오류 메시지를 나타내는 데 사용되는 선택적 요소입니다. Fault 요소가 있는 경우 Body 요소의 자식 요소여야 합니다.

ASMX 파일은 [C#](/ko/programming/cs/), [Visual Basic](/ko/programming/vb/) 또는 JScript와 같은 .NET 언어로 작성할 수 있습니다.

## ASMX는 ASPX 및 ASCX와 어떻게 다릅니까?

ASMX 파일은 ASPX 및 ASCX 파일과 다릅니다.

* ASPX, Active Server Pages, 파일은 웹 서버에서 실행되는 Microsoft ASP.NET 프레임워크를 사용하여 생성된 프로그래밍 파일입니다. 사용자가 이러한 페이지에 액세스하도록 요청할 때 클라이언트의 웹 브라우저에서 렌더링됩니다.
* ASCX(Active Server User Control)는 ASP.NET 웹 페이지 또는 전체 웹 사이트에서 재사용 가능한 컨트롤을 정의하는 데 사용되는 사용자 컨트롤을 정의합니다.

## 참고문헌

* [ASMX 서비스 사용](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX 사용자 컨트롤](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

