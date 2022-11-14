{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax 파일", "asax 파일 형식", "asax 파일 형식", "파일", "유형", "asax 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET 서버 응용 프로그램 파일",
  "description" :"ASAX 파일을 만들고 열 수 있는 API와 ASAX 파일이 무엇인지 알아보세요.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## .ASAX 파일이란?

확장자가 .asax인 파일은 서버 측에 있는 ASP.NET 응용 프로그램에서 사용하는 파일입니다. 여기에는 ASP.NET 또는 HTTP 모듈에서 발생하는 응용 프로그램 수준 및 세션 수준 이벤트에 응답하기 위한 코드가 포함되어 있습니다. 여기에는 응용 프로그램이 시작되거나 종료될 때 특정 이벤트를 처리하는 것도 포함됩니다. ASAX 파일은 선택 사항이며 전역 수준에서 애플리케이션 수준 이벤트 및 오류를 처리하기 위해 단일 ASAX 파일만 웹 애플리케이션에 추가됩니다. ASPX 페이지와 달리 ASAX 파일에는 애플리케이션의 기능을 구현하는 코드가 포함되어 있지 않습니다.

## ASAX 파일 형식

ASAX 파일은 일반 텍스트 파일 형식으로 작성되며 사람이 읽을 수 있습니다. 가장 일반적으로 사용되는 ASAX 파일은 ASP.NET 응용 프로그램의 루트 디렉터리에 있는 Global.asax입니다. 웹 서버는 사용자가 이 파일의 코드를 다운로드하거나 볼 수 없도록 이 파일로 들어오는 호출을 거부하도록 구성되어 있습니다.

### Global.ASAX - ASAX 파일 형식의 예

단일 ASAX 파일은 애플리케이션 수준 이벤트를 처리하기 위해 작성된 여러 섹션으로 구성됩니다. 이들은 다음과 같습니다.

* **응용 프로그램 지시문** - 응용 프로그램 지시문은 Global.asax 파일을 처리할 때 ASP.NET 파서에서 사용할 선택적 응용 프로그램별 설정을 정의하는 데 사용되는 태그입니다. 이러한 지시문은 Global.asax 파일의 시작 부분에 있으며 다음과 같이 정의됩니다.

```
<%@ 지시문 속성=값 [속성=값 ... ]%>
```
* **코드 선언 블록** - 코드 선언 블록은 ASP.NET 애플리케이션 파일에 포함된 서버 코드 섹션을 정의하는 데 사용됩니다.<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **코드 렌더 블록** - 페이지가 렌더링될 때 실행되는 인라인 코드 또는 표현식을 정의합니다. 코드 렌더 블록의 두 가지 스타일에는 인라인 코드와 인라인 표현식이 있습니다. 전자는 자체 포함된 줄이나 코드 블록을 정의하는 데 사용되는 반면 측면은 Write 메서드를 호출하기 위한 바로 가기로 사용됩니다.

## 참고문헌

* [HTTP 핸들러 및 HTTP 모듈 개요](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax 구문](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

