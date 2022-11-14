{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","aspx 파일", "aspx 파일 형식", "aspx 파일 형식", "파일", "유형", "aspx 파일이란"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX 파일 형식",
  "description" :"ASPX 파일을 만들고 열 수 있는 API 및 ASPX 파일이 무엇인지 알아보기 위한 파일 형식 가이드",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ASPX 파일이란?

확장자가 .aspx인 파일은 웹 서버에서 실행되는 Microsoft ASP.NET 프레임워크를 사용하여 생성된 웹 페이지입니다. ASPX는 Active Server Pages Extended의 약자이며 이러한 페이지는 URL에 액세스할 때 사용자 측의 웹 브라우저에 표시됩니다. 서버단에서도 생성되지만 .NET 프레임워크를 사용하지 않는 [ASP](/ko/web/asp/) 기술의 후계자입니다. ASP.NET 페이지에는 웹 브라우저에서 사용자에게 표시하기 위해 웹 서버에 의해 HTML로 변환되는 [C#](/ko/programming/cs/) 또는 [VB.NET](/ko/programming/vb/) 스크립트가 포함될 수 있습니다. ASPX 페이지는 .NET Web Forms라고도 합니다. Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ 및 모든 텍스트 편집기와 같은 응용 프로그램을 사용하여 열고 만들 수 있습니다.

## ASPX 파일 형식

ASP.NET 웹 양식은 웹 응용 프로그램과의 상호 작용을 위한 이벤트 기반 모델을 기반으로 합니다. 최종 사용자인 브라우저는 웹 양식을 서버에 제출하고 서버는 응답으로 전체 마크업 페이지 또는 HTML 페이지를 반환합니다. ASP.NET 구성 요소 모델은 ASPX 페이지에 대한 개체 모델을 제공합니다. 이 모델은 다음을 설명합니다.

* \와 같은 거의 모든 HTML 요소 또는 태그의 서버 측 대응<form> 그리고 \<input> .
* 복잡한 사용자 인터페이스 개발에 도움이 되는 서버 제어. 예를 들어 Calendar 컨트롤이나 Gridview 컨트롤이 있습니다.

ASPX 파일은 이러한 페이지를 구성하기 위해 ASP.NET **코드 숨김 모델**을 사용합니다.

### 인라인 코드

ASPX 페이지에 인라인으로 포함되고 사용자 구현을 위한 모든 기능을 제공하는 샘플 코드입니다. 다음 [C#](/ko/programming/cs/) 코드는 인라인 코드가 포함된 샘플 ASP.NET 페이지를 나타냅니다.

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### 코드 숨김

프리젠테이션 로직에서 HTML을 깔끔하게 분리하기 위해 코드를 작성하고 별도의 클래스 파일에 저장할 수 있습니다. 이것은 프레젠테이션 계층을 실행 코드와 독립적으로 만듭니다. 다음은 사용자에게 표시하기 위한 코드 숨김입니다.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

프레젠테이션 계층에 대한 실제 로직의 C# 구현은 다음과 같습니다.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## 참고문헌

* [ASP.NET 웹앱 - 마이크로소프트](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

