{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor AXD - Formát souboru ASP.NET Web Handler",
  "description" :"Zjistěte, co je soubor AXD a rozhraní API, která mohou vytvářet a otevírat soubory AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Co je soubor AXD?

Soubor AXD je soubor nastavení webu, který se používá pro zpracování a načítání požadavků na vložené prostředky v ASP.NET. Obsahuje instrukce pro načtení vložených zdrojů, jako jsou obrázky, soubory JavaScript ([.JS](/cs/web/js/)) a soubory [.CSS](/cs/web/css/). Soubory AXD se používají pro vkládání zdrojů do stránek na straně klienta. To umožňuje klientským stránkám přistupovat k těmto zdrojům na serveru standardním způsobem.

## Formát souboru AXD

Soubory AXD jsou uloženy jako binární soubory na straně serveru. Odkazuje na soubor Web Handler v ASP.NET, což jsou komponenty, které generují odpovědi na konkrétní požadavky na webový server. Soubory AXD provádějí vlastní zpracování před generováním odpovědi na základě požadavků stránky na straně klienta. Ty se obvykle ukládají jako soubory **WebResource.axd**.

### Co je soubor WebResource.axd?

Většina projektů ASP.NET ukládá soubory AXD jako soubory WebResource.axd, které umožňují stránkám na straně klienta stahovat prostředky, které jsou vloženy do sestavení. Vaše aplikace může čelit pomalému výkonu v případě, že ji spustíte v režimu ladění, protože obslužná rutina WebResources.axd není uložena v mezipaměti.

## Reference

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

