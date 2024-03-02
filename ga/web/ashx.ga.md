{
  "date": "2019-10-11",
  "keywords": [
"fuinseog",
"comhad",
"síneadh",
"formáid comhaid",
"ASHX",
"Comhad Láimhseálaí Gréasáin ASP.NET"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Síneadh Comhad ASHX - Comhad Láimhseálaí Gréasáin ASP.NET",
  "description": "Foghlaim faoi cad is comhad ASHX agus APIs ann ar féidir comhaid ASHX a chruthú agus a oscailt.",
  "linktitle": "ASHX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ash-gax"
}
},
  "lastmod": "2021-06-10"
}

## Cad is comhad ASHX ann?

Is leathanach gréasáin é comhad ASHX a úsáideann Láimhseálaí HTTP ASP.NET chun na leathanaigh a bhfuil tagairt déanta dóibh laistigh den chomhad seo a sholáthar don úsáideoir. Próiseálann Láimhseálaí HTTP ASP.NET an t-iarratas isteach, déanann sé tagairt do na leathanaigh ón gcomhad .ashx, agus cuireann sé an leathanach tiomsaithe ar ais chuig brabhsálaí an úsáideora. Tá an modh próiseála cosúil den chuid is mó leis an modh próiseála i gcomhaid ASPX agus an difríocht sa chás seo, go ndéantar na leathanaigh/doiciméid tagartha a phróiseáil agus a sheoladh ar ais.

## Formáid Comhaid ASHX

Déantar na comhaid .ashx a shábháil i bhformáid gnáth-théacs agus tá tagairtí iontu do leathanaigh nó doiciméid eile a sheoltar ar ais chuig brabhsálaí an úsáideora arna iarraidh sin. Is féidir iad seo a oscailt in aon eagarthóir téacs agus IDEanna forbróra ar nós Xamarin Studio, Microsoft Notepad, Notepad ++, agus go leor eile. Tá na comhaid ASHX úsáideach i gcás go bhfuil:
 * Comhaid dhénártha
 * Radhairc íomhá dinimiciúil
 * Leathanaigh ghréasáin atá ríthábhachtach ó thaobh feidhmíochta de
 * Comhaid XML
 * Leathanaigh ghréasáin íosta

## Conas comhad ASHX a thiomsú go dinimiciúil?

Is féidir na céimeanna seo a leanas a úsáid chun comhad ASHX a chur leis agus a thiomsú ag baint úsáide as Microsoft Visual Studio.

 * cuir láimhseálaí Cineálach - Handler1.ashx i stiúideo amhairc
 * scrios an comhad cs a chruthaigh go huathoibríoch.
 * oscail ashx arís,
** bain CodeBehind=Handler1.ashx.cs
** cuir c# cód leis thíos

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
### ASHX Sampla

Tugann an cód ASHX seo a leanas an comhad íomhá ar ais chuig iarratas úsáideora nuair a ghlaoitear an comhad ASHX sa bhrabhsálaí idirlín.


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

## Tagairtí

 * [Tiomsaigh Comhad ASHX]( https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 

