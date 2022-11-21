{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "dosya", "uzantı", "dosya formatı", "ASHX", "ASP.NET Web İşleyici Dosyası"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASHX Dosya Uzantısı - Bir ASP.NET Web İşleyici Dosyası",
  "description" :"ASHX dosyasının ne olduğu ve ASHX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## ASHX dosyası nedir?

Bir ASHX dosyası, ASP.NET HTTP İşleyicisi tarafından kullanıcıya bu dosyanın içinde başvurulan sayfaları sunmak için kullanılan bir web sayfasıdır. ASP.NET HTTP İşleyici gelen isteği işler, .ashx dosyasındaki sayfalara başvurur ve derlenen sayfayı kullanıcının tarayıcısına geri gönderir. İşleme yöntemi çoğunlukla ASPX dosyalarına benzer, ancak bu durumda başvurulan sayfalar/belgeler işlenir ve geri gönderilir.

## ASHX Dosya Biçimi

.ashx dosyaları düz metin dosyası biçiminde kaydedilir ve istek üzerine kullanıcının tarayıcısına geri gönderilen diğer sayfalara veya belgelere referanslar içerir. Bunlar herhangi bir metin düzenleyicide ve Xamarin Studio, Microsoft Notepad, Notepad++ ve çok daha fazlası gibi geliştirici IDE'lerinde açılabilir. ASHX dosyaları, aşağıdakilere sahip olduğunuzda kullanışlıdır:
* İkili dosyalar
* Dinamik görüntü görünümleri
* Performans açısından kritik web sayfaları
* XML dosyaları
* Minimum web sayfaları

## Bir ASHX dosyası dinamik olarak nasıl derlenir?

Aşağıdaki adımlar, Microsoft Visual Studio kullanılarak bir ASHX dosyası eklemek ve derlemek için kullanılabilir.

* görsel stüdyoda bir Genel işleyici - Handler1.ashx ekleyin
* otomatik oluşturulan cs dosyasını silin.
* ashx'i tekrar açın,
** CodeBehind="Handler1.ashx.cs" öğesini kaldırın
** aşağıya c# kodunu ekleyin

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
### ASHX Örneği

Aşağıdaki ASHX kodu, ASHX dosyası internet tarayıcısında çağrıldığında görüntü dosyasını kullanıcının isteğine döndürür.


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

## Referanslar

* [ASHX Dosyasını Derleyin](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


