{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "fichier", "extension", "format de fichier", "ASHX", "Fichier du gestionnaire Web ASP.NET" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extension de fichier ASHX - Un fichier de gestionnaire Web ASP.NET",
  "description" :"Découvrez ce qu'est un fichier ASHX et les API qui peuvent créer et ouvrir des fichiers ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Qu'est-ce qu'un fichier ASHX ?

Un fichier ASHX est une page Web utilisée par le gestionnaire HTTP ASP.NET pour servir l'utilisateur avec les pages référencées dans ce fichier. Le gestionnaire HTTP ASP.NET traite la demande entrante, référence les pages du fichier .ashx et renvoie la page compilée au navigateur de l'utilisateur. La méthode de traitement est essentiellement similaire à celle des fichiers ASPX avec la différence que dans ce cas, les pages/documents référencés sont traités et renvoyés.

## Format de fichier ASHX

Les fichiers .ashx sont enregistrés au format texte brut et contiennent des références à d'autres pages ou documents qui sont renvoyés au navigateur de l'utilisateur sur demande. Ceux-ci peuvent être ouverts dans n'importe quel éditeur de texte et IDE de développeur tels que Xamarin Studio, Microsoft Notepad, Notepad ++ et bien d'autres. Les fichiers ASHX sont utiles dans le cas où vous avez :
* Fichiers binaires
* Vues d'images dynamiques
* Pages Web critiques pour les performances
* Fichiers XML
* Pages Web minimales

## Comment compiler dynamiquement un fichier ASHX ?

Les étapes suivantes peuvent être utilisées pour ajouter et compiler un fichier ASHX à l'aide de Microsoft Visual Studio.

* ajouter un gestionnaire générique - Handler1.ashx dans visual studio
* supprimer le fichier cs qui a été créé automatiquement.
* rouvrir ashx,
** supprimer CodeBehind="Handler1.ashx.cs"
** ajouter le code c# ci-dessous

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
### Exemple ASHX

Le code ASHX suivant renvoie le fichier image à la demande de l'utilisateur lorsque le fichier ASHX est appelé dans le navigateur Internet.


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

## Références

* [Compiler le fichier ASHX] (https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


