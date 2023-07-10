{
  "date" : "2019-10-11",
  "keywords" :[ "ascx", "ascx soubor", "formát souboru ascx", "typ souboru ascx", "soubor", "typ", "co je soubor ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ASCX",
  "description" :"Zjistěte, co je soubor ASCX a rozhraní API, která mohou vytvářet a otevírat soubory ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor ASCX?

Soubor s příponou .ascx je uživatelský ovládací prvek, který se používá jako opakovaně použitelná komponenta na webových stránkách. Odkazuje se na něj na libovolném webu ASP přetažením z ovládacího pole na stránku. Uživatelské ovládací prvky ASCX jsou přidány do projektu jako centrální zdroj, což má za následek, že jakákoli změna uživatelského ovládání se projeví na celém webu. Na rozdíl od souborů ASMX, které definují mechanismus pro komunikaci v rámci 2 objektů přes internet, jsou soubory ASCX uživatelskými ovládacími prvky pro vkládání do stránek nebo webových stránek.

## Formát souboru ASCX

Soubory ASCX se zapisují ve formátu prostého textu a mohou používat kód za funkcí, jako jsou webové stránky, které končí příponou .ascx.cs. Značkovací kód uživatelských ovládacích prvků začíná direktivou @Control, jak je znázorněno v následujícím příkladu.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Tento webový uživatelský ovládací prvek lze znovu použít na mnoha stránkách, jako je zápatí stránky, záhlaví nebo nějaký druh navigace na webu. Webové uživatelské ovládací prvky mají vlastnosti, metody a události jako každý jiný ovládací prvek, díky kterému jsou užitečné při nastavování jejich vizuálního chování.

### Příklad registrace uživatelských ovládacích prvků ve web.config

Chcete-li používat ovládací prvek jednoho uživatele na mnoha stránkách, lze webový ovládací prvek zaregistrovat v souboru web.config. To umožňuje používat kontrolu nad celou webovou stránkou namísto samostatné registrace na každé stránce. Následující ukázkový kód definuje, jak zaregistrovat webový ovládací prvek v souboru web.config, aby se zobrazil jako zápatí na celém webu.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Reference

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [ASCX User Control](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

