{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "soubor asmx", "formát souboru asmx", "typ souboru asmx", "soubor", "typ", "co je soubor asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - ASP.NET Web Service File",
  "description" :"Zjistěte, co je soubor ASMX a rozhraní API, která mohou vytvářet a otevírat soubory ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Co je soubor ASMX?

Soubor s příponou .asmx je soubor webové služby ASP.NET, který poskytuje komunikaci mezi dvěma objekty přes internet pomocí protokolu SOAP (Simple Object Access Protocol). Je nasazena jako služba na webovém serveru se systémem Windows pro zpracování příchozího požadavku a vrácení odpovědi. Na rozdíl od souborů [ASPX](/cs/web/aspx/), které obsahují kód pro vizuální zobrazení webových stránek ASP.NET, soubory ASMX běží na serveru na pozadí a provádějí různé úkoly, jako je připojení k databázi, načítání dat a jejich vrácení do formát, ve kterém byla žádost podána. Ty se používají speciálně pro webové služby XML.

## Formát souboru ASMX

Soubory ASMX jsou ve formátu prostého textu a lze je otevřít nebo upravit v aplikacích, jako je Microsoft Visual Studio nebo textové editory. Je to proprietární formát souborů společnosti Microsoft a má dobře definovanou syntaxi pro vytváření webových služeb. Odpověď souboru ASMX ve formě SOAP XML má následující prvky.

* `Envelop` - Kořenový prvek, který identifikuje dokument XML jako zprávu SOAP.
* `Header` – Volitelný prvek, který obsahuje informace specifické pro aplikaci, jako jsou ověřovací data. Pokud je přítomen prvek Záhlaví, musí to být první podřízený prvek prvku Obálka.
* `Tělo` - Obsahuje zprávu SOAP určenou pro příjemce.
* `Fault` - Volitelný prvek, který se používá k označení chybových zpráv. Pokud je přítomen prvek Fault, musí to být podřízený prvek prvku Body.

Soubory ASMX lze psát v jazycích .NET, jako je [C#](/cs/programming/cs/), [Visual Basic](/cs/programming/vb/) nebo JScript.

## Jak se ASMX liší od ASPX a ASCX?

Soubory ASMX se liší od souborů ASPX a ASCX.

* ASPX, Active Server Pages, soubory jsou programovací soubory, které jsou generovány pomocí Microsoft ASP.NET framework běžícího na webových serverech. Ty jsou vykresleny ve webovém prohlížeči klienta, když uživatel požádá o přístup na takovou stránku.
* ASCX, Active Server User Control, definuje uživatelské ovládací prvky, které se používají k definování opakovaně použitelných ovládacích prvků na webových stránkách ASP.NET nebo na celém webu.

## Reference

* [Spotřeba služby ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX User Control](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

