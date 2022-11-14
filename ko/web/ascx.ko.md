{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","ascx 파일", "ascx 파일 형식", "ascx 파일 형식", "파일", "유형", "ascx 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASCX 파일 형식",
  "description" :"ASCX 파일이 무엇이며 ASCX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## .ASCX 파일이란?

확장자가 .ascx인 파일은 웹 페이지에서 재사용 가능한 구성 요소로 사용되는 사용자 컨트롤입니다. 컨트롤 상자에서 페이지로 끌어서 모든 ASP 웹 사이트에서 참조됩니다. ASCX 사용자 컨트롤이 프로젝트에 중앙 소스로 추가되어 사용자 컨트롤의 변경 사항이 전체 웹사이트에 반영됩니다. 인터넷을 통해 2개의 개체 내에서 통신하는 메커니즘을 정의하는 ASMX 파일과 달리 ASCX 파일은 페이지 또는 웹사이트에 포함하기 위한 사용자 컨트롤입니다.

## ASCX 파일 형식

ASCX 파일은 일반 텍스트 형식으로 작성되며 .ascx.cs로 끝나는 웹 페이지와 같은 코드 숨김 기능을 사용할 수 있습니다. 사용자 컨트롤의 마크업 코드는 다음 예제와 같이 @Control 지시문으로 시작합니다.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

이 웹 사용자 컨트롤은 페이지 바닥글, 머리글 또는 일종의 사이트 탐색과 같은 많은 페이지에서 재사용할 수 있습니다. 웹 사용자 컨트롤에는 시각적 동작을 설정하는 데 유용한 다른 컨트롤과 같은 속성, 메서드 및 이벤트가 있습니다.

### web.config에 사용자 컨트롤을 등록하는 예

여러 페이지에서 단일 사용자 컨트롤을 사용하기 위해 web.config에 웹 컨트롤을 등록할 수 있습니다. 이를 통해 각 페이지에 개별적으로 등록하는 대신 모든 웹사이트에 대한 제어를 사용할 수 있습니다. 다음 샘플 코드는 web.config에 웹 컨트롤을 등록하여 전체 웹 사이트에 바닥글로 표시하는 방법을 정의합니다.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## 참고문헌

* [ASCX 대 ASMX](https://forums.asp.net/t/1838934.aspx?How+to+work+with+ascx+files+)
* [ASCX 사용자 컨트롤](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

