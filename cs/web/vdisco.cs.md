{
  "date" : "2023-01-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDISCO File - DISCO Dynamic Discovery Document File Format",
  "description":"Další informace o tom, co je soubor VDISCO?",
  "linktitle" : "VDISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-01-29"
}

## Co je soubor VDISCO?

Soubor VDISCO je vyhledávací soubor používaný aplikací Microsoft Visual Studio ve svých webových službách. Poskytuje informace o dostupných webových službách, jako jsou jejich adresy URL, jmenné prostory a metody. Soubor VDISCO je podobný formátu souboru [DISCO](/cs/web/disco/), ale je generován za běhu. Je uložen v aplikaci webové služby a používá jej Visual Studio k dynamickému zjišťování a používání webových služeb v projektu. Soubory VDISCO se používají v kombinaci se souborem [.asmx](/cs/web/asmx/), který obsahuje skutečný kód webové služby.

Soubor VDISCO můžete otevřít v libovolném textovém editoru, jako je Microsoft Notepad, Github Atom a Apple TextEdit. Pro práci s ním lze také otevřít pomocí Microsoft Visual Studio 2012 a novějších.

## Formát souboru VDISCO

Soubor VDISCO je uložen a hostován ve formátu souboru [XML](/cs/web/xml/), což je univerzální formát pro skládání a publikování dat. Obsahuje URL služby, jmenné prostory a metody ve standardních XML značkách, kde každá značka obsahuje příslušnou hodnotu své informace.

## Reference

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Zjištění webových služeb](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Příklad C# třídy DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

