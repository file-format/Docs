{
  "date" : "2019-10-11",
  "keywords" :[ "cshtml","cshtml 파일", "cshtml 파일 형식", "cshtml 파일 형식", "파일", "유형", "cshtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSHTML - ASP.NET Razor 웹페이지",
  "description":"CSHTML 파일 형식과 CSHTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CSHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-04-29"
}

## CSHTML 파일이란?

확장자가 .cshtml인 파일은 [C#](/ko/programming/cs/) HTML 파일로, Razor Markup 엔진이 사용자의 브라우저에 웹 페이지 파일을 렌더링하는 데 서버 측에서 사용합니다. 이 서버 측 코딩은 표준 ASP.NET 페이지와 유사하여 웹 페이지가 브라우저에 작성될 때 동적으로 웹 콘텐츠를 즉시 생성할 수 있습니다. 서버는 생성된 페이지를 브라우저로 보내기 전에 페이지 내부의 서버 측 코드를 실행합니다. 데이터베이스 액세스 및 복잡한 보기 렌더링과 같은 복잡한 작업. CSHTML 파일은 Microsoft Visual Studio를 사용하여 생성하고 프로그래밍할 수 있습니다.

## CSHTML 파일 형식

CSHTML 파일은 Razor 마크업 엔진에서 설명하는 구문을 따르는 텍스트 파일입니다. Razor는 C# 및 VB.NET을 모두 지원하며 기존 ASP 및 ASP.NET보다 배우고 사용하기 쉽습니다. w3schools에는 Razor의 [C# 및 VB.NET 구문](https://www.w3schools.com/asp/razor_syntax.asp) 코딩에 대한 간단하면서도 효과적인 가이드가 있습니다.

### CSHTML 예제

다음은 Razor용 CSHTML 파일에 사용된 C# 코드 예제입니다.

```
<!-- Single statement block -->
@{ var myMessage = "Hello World"; }

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@{
var greeting = "Welcome to our site!";
var weekDay = DateTime.Now.DayOfWeek;
var greetingMessage = greeting + " Here in Huston it is: " + weekDay;
}
<p>The greeting is: @greetingMessage</p>
```

Razor에 해당하는 VB.NET 코드는 다음과 같습니다.

```
<!-- Single statement block  -->
@Code dim myMessage = "Hello World" End Code

<!-- Inline expression or variable -->
<p>The value of myMessage is: @myMessage</p>

<!-- Multi-statement block -->
@Code
dim greeting = "Welcome to our site!"
dim weekDay = DateTime.Now.DayOfWeek
dim greetingMessage = greeting & " Here in Huston it is: " & weekDay
End Code

<p>The greeting is: @greetingMessage</p>
```

## 참고문헌

* [Razor 구문 참조 - Microsoft](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/razor?view=aspnetcore-5.0)

