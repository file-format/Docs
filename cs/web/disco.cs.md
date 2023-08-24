{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DISCO File - DISCO Discovery Document File Format",
  "description":"Zjistěte, co je soubor DISCO a rozhraní API, která mohou vytvářet a otevírat soubory DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Co je soubor DISCO?

Soubor DISCO je formát souboru Microsoft Discovery, který se používá pro publikování a zjišťování webových služeb. Je uložen ve formátu souboru XML a umožňuje nástrojům zjišťování webových služeb vyhledat nebo objevit jeden nebo více souvisejících dokumentů pro popis dostupných služeb [XML](/cs/web/xml/). V souboru DISCO jsou uloženy informace, jako jsou dokumenty zjišťování, schémata [XSD](/programming/xsd/) a popisy služeb. Webové služby XML používají tyto informace k přístupu k dostupným webovým službám XML na dané adrese URL.

## Formát souboru DISCO – Další informace

Soubory DISCO se ukládají ve formátu souboru XML. Nástroj Microsoft Discovery Tool (DISCO.exe), který je dodáván s vývojovým softwarem Microsoft ASP.NET, jako je Microsoft Studio, pomocí souborů DISCO zjišťuje podrobnosti o webových službách XML uvedených v DiscoveryDocument na konkrétní adrese URL. Společnost Microsoft poskytla podporu čtení souborů zjišťování v .NET frameworku.

## Reference

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Zjištění webových služeb](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [Příklad C# třídy DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

