{
  "date" : "2022-09-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik DISCO - Format pliku dokumentu DISCO Discovery",
  "description":"Dowiedz się, co to jest plik DISCO i interfejsy API, które mogą tworzyć i otwierać pliki DISCO.",
  "linktitle" : "DISCO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-17"
}

## Czym jest plik DISCO?

Plik DISCO to format pliku Microsoft Discovery, który jest używany do publikowania i odkrywania usług sieci Web. Jest przechowywany w formacie pliku XML i umożliwia narzędziom Web Services Discovery zlokalizowanie lub wykrycie jednego lub kilku powiązanych dokumentów opisujących dostępne usługi [XML](/pl/web/xml/). Plik DISCO przechowuje informacje, takie jak dokumenty wykrywania, schematy [XSD](https://docs.fileformat.com/programming/xsd/) i opisy usług. Usługi sieci Web XML wykorzystują te informacje, aby uzyskać dostęp do usług sieci Web XML dostępnych pod danym adresem URL.

## Format pliku DISCO — więcej informacji

Pliki DISCO są zapisywane w formacie pliku XML. Narzędzie Microsoft Discovery Tool (DISCO.exe), które jest dostarczane w pakiecie z oprogramowaniem programistycznym Microsoft ASP.NET, takim jak Microsoft Studio, wykorzystuje pliki DISCO do odkrywania szczegółowych informacji o usługach sieci Web XML wymienionych w dokumencie DiscoveryDocument pod określonym adresem URL. Firma Microsoft zapewniła obsługę odczytu plików wykrywania w środowisku .NET.

## Bibliografia

* [DISCO](https://appsource.microsoft.com/en-us/product/office/WA104381894)
* [Wykrywanie usług sieciowych](https://en.wikipedia.org/wiki/Web_Services_Discovery)
* [C# Przykład klasy DiscoveryClient](https://learn.microsoft.com/en-us/dotnet/api/system.web.services.discovery.discoveryclientprotocol?view=netframework-4.8)

