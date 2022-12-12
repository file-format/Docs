{
  "date" : "2021-08-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3DM",
  "description":"Poznaj format plików 3DM i interfejsy API, które mogą otwierać i tworzyć pliki 3DM.",
  "linktitle" : "3DM",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-08-13"
}

## Czym jest plik 3DM?

Plik z rozszerzeniem .3dm to format pliku typu open source, który jest używany w oprogramowaniu do grafiki 3D. Zawiera modele 3D wraz z ich zależnymi elementami, takimi jak informacje o powierzchni, punktach i krzywych. Format pliku 3DM został opracowany przez inicjatywę [openNURBS](https://github.com/mcneel/opennurbs) w celu dokładnego przenoszenia geometrii 3D między aplikacjami. Pliki 3DM można otwierać i konwertować za pomocą aplikacji takich jak Rhinoceros, SAP VEViewer, Moment of Inspiration i Right Hemisphere Deep View.

## Format pliku 3DM

[openNURBS](https://github.com/mcneel/opennurbs), zestaw narzędzi typu open source, zawiera specyfikacje formatu plików 3DM, dokumentację, biblioteki kodu źródłowego C++ oraz zestawy .NET 2.0 do odczytu i zapisu formatu pliku.

### Przykładowe pliki 3DM

Niektóre przykładowe pliki 3DM można pobrać z sekcji openNURBS [examples](https://github.com/mcneel/opennurbs/tree/7.x/example_files). Można je załadować i wyświetlić za pomocą zestawu narzędzi openNURBS.

## Jak odczytywać lub zapisywać pliki 3DM?

Biblioteki [openNURBS](https://github.com/mcneel/opennurbs) umożliwiają każdemu odczytywanie i zapisywanie plików w formacie 3DM bez konieczności używania Rhino. Zapewnia kod źródłowy C++ dla biblioteki, która odczytuje i zapisuje modele 3D przy użyciu formatu pliku openNURBS. Ten zestaw narzędzi zawiera również narzędzia do oceny NURBS oraz podstawowe narzędzia do manipulacji widokami geometrycznymi i 3D, a także zawiera kod źródłowy kilku przykładowych programów. Fora wsparcia [Rhinoceros](https://discourse.mcneel.com/c/opennurbs/6) to bogate treści i miejsce dyskusji, w którym można dzielić się problemami napotykanymi przez społeczność 3DM i uzyskiwać rozwiązania.

## Bibliografia ##

* [Nosorożec](https://www.rhino3d.com/download/openNURBS)
* [Nosorożec - Wikipedia](https://en.wikipedia.org/wiki/Rhinoceros_3D)
* [openNURBS na GitHub](https://github.com/mcneel/opennurbs)

