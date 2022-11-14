{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "파일", "확장자", "파일 형식", "ASHX", "ASP.NET 웹 처리기 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX 파일 확장자 - ASP.NET 웹 처리기 파일",
  "description" :"ASHX 파일이 무엇이며 ASHX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASHX 파일이란?

ASHX 파일은 ASP.NET HTTP 처리기가 이 파일 내부에서 참조하는 페이지를 사용자에게 제공하는 데 사용하는 웹 페이지입니다. ASP.NET HTTP 처리기는 들어오는 요청을 처리하고 .ashx 파일의 페이지를 참조하며 컴파일된 페이지를 사용자의 브라우저로 다시 보냅니다. 처리 방법은 이 경우 참조된 페이지/문서가 처리되어 다시 전송된다는 점에서 ASPX 파일의 처리 방법과 대부분 유사합니다.

## ASHX 파일 형식

.ashx 파일은 일반 텍스트 파일 형식으로 저장되며 요청 시 사용자의 브라우저로 다시 전송되는 다른 페이지 또는 문서에 대한 참조를 포함합니다. Xamarin Studio, Microsoft 메모장, 메모장++ 등과 같은 모든 텍스트 편집기 및 개발자 IDE에서 열 수 있습니다. ASHX 파일은 다음과 같은 경우에 유용합니다.
* 바이너리 파일
* 동적 이미지 보기
* 성능이 중요한 웹 페이지
* XML 파일
* 최소한의 웹 페이지

## ASHX 파일을 동적으로 컴파일하는 방법은 무엇입니까?

다음 단계는 Microsoft Visual Studio를 사용하여 ASHX 파일을 추가하고 컴파일하는 데 사용할 수 있습니다.

* 일반 처리기 추가 - Visual Studio의 Handler1.ashx
* 자동 생성된 cs 파일을 삭제합니다.
* ashx를 다시 엽니다.
** CodeBehind="Handler1.ashx.cs" 제거
** 아래에 C# 코드 추가

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### ASHX 예

다음 ASHX 코드는 인터넷 브라우저에서 ASHX 파일을 호출할 때 사용자의 요청에 따라 이미지 파일을 반환합니다.


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## 참고문헌

* [ASHX 파일 컴파일](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


