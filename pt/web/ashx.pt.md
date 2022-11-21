{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "arquivo", "extensão", "formato de arquivo", "ASHX", "Arquivo manipulador da Web ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extensão de arquivo ASHX - um arquivo ASP.NET Web Handler",
  "description" :"Saiba mais sobre o que é um arquivo ASHX e APIs que podem criar e abrir arquivos ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## O que é um arquivo ASHX?

Um arquivo ASHX é uma página da Web que é usada pelo ASP.NET HTTP Handler para servir ao usuário com as páginas referenciadas dentro desse arquivo. O ASP.NET HTTP Handler processa a solicitação de entrada, faz referência às páginas do arquivo .ashx e envia de volta a página compilada ao navegador do usuário. O método de processamento é muito semelhante ao dos arquivos ASPX com a diferença de que, neste caso, as páginas/documentos referenciados são processados e enviados de volta.

## Formato de arquivo ASHX

Os arquivos .ashx são salvos em formato de arquivo de texto simples e contêm referências a outras páginas ou documentos que são enviados de volta ao navegador do usuário mediante solicitação. Eles podem ser abertos em qualquer editor de texto e IDEs de desenvolvedor, como Xamarin Studio, Microsoft Notepad, Notepad++ e muitos outros. Os arquivos ASHX são úteis caso você tenha:
* Arquivos binários
* Visualizações de imagens dinâmicas
* Páginas da web com desempenho crítico
* Arquivos XML
* Páginas da web mínimas

## Como compilar dinamicamente um arquivo ASHX?

As etapas a seguir podem ser usadas para adicionar e compilar um arquivo ASHX usando o Microsoft Visual Studio.

* adicione um manipulador genérico - Handler1.ashx no visual studio
* exclua o arquivo cs que foi criado automaticamente.
* abra o ashx novamente,
** remova CodeBehind="Handler1.ashx.cs"
** adicione o código c# abaixo

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
### Exemplo ASHX

O código ASHX a seguir retorna o arquivo de imagem à solicitação do usuário quando o arquivo ASHX é chamado no navegador da Internet.


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

## Referências

* [Compilar arquivo ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


