{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","plik vdw", "format pliku vdw", "typ pliku vdw", "plik", "typ", "co to jest plik vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW — format pliku usługi graficznej programu Visio",
  "description":"Poznaj format pliku VDW i interfejsy API, które mogą tworzyć i otwierać pliki VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Czym jest plik VDW?

VDW to format pliku Visio Graphics Service, który określa strumienie i magazyny wymagane do renderowania rysunku internetowego. Rysunek internetowy to zbiór stron rysunku, kształtów, czcionek, obrazów, połączeń danych i informacji o aktualizacji diagramu, które można renderować jako rysunek wektorowy lub rastrowy. Pliki VDW można również otwierać w programie Microsoft Visio, ale są one zapisywane głównie do użytku w Internecie. Microsoft Visio oferuje możliwość konwertowania plików Visio na wiele różnych formatów plików, w tym [PNG](/pl/Image/PNG/), [BMP](/pl/Image/BMP/), [PDF](/pl/pdf/) i inne.

## **VDW** Format pliku

Specyfikacje techniczne formatu plików VDW są dostępne online przez [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) i mogą być używane przez programistów do tworzenia Aplikacje. Dokument techniczny opisuje dane zawarte w pliku złożonym, który zawiera magazyny i strumienie. Reprezentacja rysunku internetowego jest możliwa za pośrednictwem strumienia o nazwie VisioServerData, za pośrednictwem archiwum ZIP. Część ShapGraphic XML w archiwum opisuje elementy graficzne wyświetlane w rysunku internetowym i są wyrażone w Extensible Application Markup Language (XAML). Zbiór części XML w archiwum ZIP opisuje połączenie danych rysunku internetowego, informacje o jego kształcie i logikę aktualizacji diagramu. Te części są wyrażone jako XML. Część XML DataGraphic opisuje ponownie obliczone właściwości, które mają zostać ocenione po odświeżeniu danych w rysunku internetowym ze źródła danych. Dodatkowe elementy w archiwum ZIP zawierają informacje o czcionkach i obrazach użytych w rysunku internetowym.

|![Możliwa implementacja pliku](/pl/web/vdw.png "Możliwa implementacja pliku")

## Bibliografia

* [[MS-VGSFF]: format pliku usługi graficznej programu Visio (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

