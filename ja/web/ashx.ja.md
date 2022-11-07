{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "ファイル", "拡張子", "ファイル形式", "ASHX", "ASP.NET Web ハンドラ ファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX ファイル拡張子 - ASP.NET Web ハンドラ ファイル",
  "description" :"ASHX ファイルとは何か,および ASHX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## .ASHX オプション番号

ASHX ファイルは、このファイル内で参照されるページをユーザーに提供するために ASP.NET HTTP ハンドラーによって使用される Web ページです。 ASP.NET HTTP ハンドラーは受信要求を処理し、.ashx ファイルからページを参照して、コンパイルされたページをユーザーのブラウザーに送り返します。処理方法は ASPX ファイルの場合とほとんど同じですが、この場合、参照されたページ/ドキュメントが処理されて送り返されます。

## ASHX ファイル形式

.ashx ファイルはプレーン テキスト ファイル形式で保存され、要求に応じてユーザーのブラウザーに送り返される他のページまたはドキュメントへの参照が含まれています。これらは、Xamarin Studio、Microsoft Notepad、Notepad++ などの任意のテキスト エディターおよび開発者用 IDE で開くことができます。 ASHX ファイルは、次の場合に役立ちます。
* バイナリ ファイル
* 動的画像ビュー
* パフォーマンスが重要な Web ページ
* XML ファイル
* 最小限の Web ページ

## ASHX ファイルを動的にコンパイルする方法は?

次の手順を使用して、Microsoft Visual Studio を使用して ASHX ファイルを追加およびコンパイルできます。

* ジェネリック ハンドラーを追加 - Visual Studio で Handler1.ashx
* 自動作成された cs ファイルを削除します。
* ashx を再度開きます。
** CodeBehind="Handler1.ashx.cs" を削除
** 以下に c# コードを追加

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
### ASHX の例

次の ASHX コードは、インターネット ブラウザーで ASHX ファイルが呼び出されたときに、ユーザーの要求に応じて画像ファイルを返します。


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

## 参考文献

* [ASHX ファイルのコンパイル](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


