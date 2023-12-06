{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER File - ASP.NET Master Page File Format",
  "description" :"Další informace o formátu souborů MASTER a rozhraních API pro vytváření a otevírání souborů MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Co je soubor MASTER?

Soubor MASTER je soubor šablony hlavní webové stránky vytvořený pomocí ASP.NET. Používá se jako výchozí bod pro vytváření více stránek, které mají stejné rozvržení a nastavení jako soubor MASTER. Soubor MASTER šablony obsahuje nastavení pro záhlaví, navigační nabídky, zápatí, písmo a informace o stylu. Použití souboru MASTER pomáhá rychle vytvořit více webových stránek.

Soubor MASTER můžete otevřít pomocí sady Microsoft Visual Studio 2022 a vyšší.

## Formát souboru MASTER – Další informace

Soubor MASTER je vytvořen a uložen ve formátu HTML a je podobný jakémukoli jinému souboru webové stránky. Je rozdělen na upravitelné a neupravitelné části. Editovatelné sekce jsou ty, které lze upravit tak, aby vyhovovaly požadavkům uživatele. Neupravitelné části jsou při otevření souboru MASTER v aplikaci Microsoft Visual Studio zašedlé.

Hlavní stránky se skládají ze dvou částí, tj. ze samotné stránky předlohy a jedné nebo více stránek s obsahem.

### HLAVNÍ stránka

Hlavní stránka má příponu .master a je vytvořena v ASP.NET. Má předdefinované rozložení, které se skládá ze statického textu, HTMLtagů a ovládacích prvků na straně serveru. V běžných stránkách .aspx se používá direktiva @ Page. V případě souborů .master je toto nahrazeno direktivou @ Master.

### Stránky s obsahem

Stránka s obsahem představuje obsah pro ovládací prvky zástupného symbolu vzorové stránky. Toto jsou stránky .aspx, které jsou ve skutečnosti kódem na pozadí hlavní stránky. Stránky obsahu jsou svázány pomocí direktivy @ Page zahrnutím atributu MasterPageFile odkazujícího na vzorovou stránku, která má být použita, jak je uvedeno níže.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Reference

* [Přehled hlavních stránek ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

