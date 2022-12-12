{
  "date" : "2019-10-11",
  "keywords" :["xaml","plik xaml", "format pliku xaml", "typ pliku xaml", "plik", "typ", "co to jest plik xaml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAML — język znaczników oparty na XML",
  "description":"Poznaj format pliku XAML i interfejsy API, które mogą tworzyć i otwierać pliki XAML.",
  "linktitle" : "XAML ",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik XAML?

XAML, Extensible Application Markup Language, pliki rozszerzeń opisują elementy interfejsu użytkownika dla aplikacji opartych na Windows Presentation Foundation (WPF). Chociaż jest językiem, nie wymaga programowania, ponieważ jest oparty na standardowym formacie **[XML](/pl/web/xml/)**, który jest łatwy w użyciu i zrozumiały. XAML (wymawiane jako „zammel”) został opracowany przez firmę Microsoft w celu tworzenia interfejsów użytkownika. Jego akronim pierwotnie oznaczał Extensible Avalon Markup Language, gdzie Avalon był kryptonimem WPF. Pliki XAML są czasami zapisywane również z rozszerzeniem XOML.

## Aplikacje XAML

XAML jest używany w technologiach .NET Framework 3.0 i .NET Framework 4.0, takich jak WPF, Silverlight, Windows Workflow Foundation (WF) i kilka innych. Elementy interfejsu użytkownika, powiązania danych, zdarzenia i inne funkcje są definiowane przez formularze XAML w WPF. Podobnie przepływy pracy w WF można definiować przy użyciu języka XAML. Jest łatwo przetwarzany przez narzędzia z tego powodu, że jest oparty na XML. Ponieważ jest to język deklaratywny i nie wymaga kompilacji, pojawia się wiele produktów opartych na aplikacjach opartych na XAML. Wszystko, co jest tworzone lub implementowane w XAML, można wyrazić przy użyciu bardziej tradycyjnego języka .NET, takiego jak C# lub Visual Basic .NET.

## Format pliku XAML

XAML jest całkowicie oparty na formacie XML. Wstępne specyfikacje [XAML Object Mapping](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) zostały opublikowane w 2006, a następnie kolejna [wersja](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) opublikowana w 2009. Te specyfikacje definiują dwa abstrakcyjne modele informacji:

* Model zestawu informacji schematu XAML
* Model zestawu informacji XAML

Zestaw informacji Xaml (w skrócie „Zestaw informacji Xaml”) definiuje strukturę informacji, które może reprezentować wystąpienie Xaml. Zestaw informacji o schemacie Xaml umożliwia zdefiniowanie określonych słowników Xaml. Ta specyfikacja definiuje również zestaw reguł służących do przekształcania dokumentu XML w zestaw informacji Xaml. XML jest powszechnym formatem dla Xaml. (Termin „dokument Xaml” odnosi się do dokumentu XML, który reprezentuje zestaw informacji Xaml.) Chociaż ta specyfikacja nie definiuje żadnych innych reprezentacji, można użyć dowolnej reprezentacji fizycznej, o ile może reprezentować informacje w zestawie informacji Xaml .

## Bibliografia

* [XAML — z Wikipedii](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [Specyfikacje formatu plików XAML](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)

