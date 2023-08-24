
{
  "date" : "2022-01-28",
  "keywords": [ ".aml file", "extension", "format","Microsoft Assistance Markup Language File", "how to open .aml file","aml file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik AML - plik języka znaczników pomocy Microsoft",
  "description":"Dowiedz się, co to jest plik AML i interfejsy API, które mogą tworzyć i otwierać pliki AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier":"programming-aml",
      "parent" : "programming"
}
},
  "lastmod" : "2022-01-28"
}

# AML — plik języka znaczników pomocy firmy Microsoft

## Czym jest plik AML?

Plik AML (Assistance Markup Language) to plik XML wygenerowany za pomocą Microsoft Assistance Markup Language (MAML). Został opracowany przez firmę Microsoft w celu zapewnienia pomocy online dla systemu operacyjnego Microsoft Windows. Wcześniej pomoc systemu Windows była dostępna w skompilowanym formacie pliku HTML [CHM](/pl/web/chm/). Pliki AML zapewniają ustrukturyzowany dokument, który umożliwia aplikacji tworzenie kodu źródłowego i wspieranie stron pomocy. Pozwala to na definiowanie dokumentów i ich elementów składowych na podstawie ich kontekstu. Pliki pomocy AML są publikowane online i można je skonfigurować tak, aby były aktualizowane z aktualizacji pakietów dostępnych online.

## Struktura pliku MML

Pliki AML generowane przy użyciu MAML są zapisywane jako pliki [XML](/pl/web/xml/), których można używać do wyrażania szerokiego zakresu aktywnych koncepcji. Może również zapewniać pomoc z przewodnikiem (kreator aktywnej zawartości), która sprawia, że plik pomocy jest interaktywny dla użytkownika za pomocą kreatora krok po kroku.

Plik AML wygenerowany przy użyciu MAML jest zgodny ze swoją strukturą tworzenia, którą można podzielić na segmenty, takie jak:

* Koncepcyjne
* Często zadawane pytania
* Słowniczek
* Procedura
* Odniesienie
* Zawartość wielokrotnego użytku
* Zadanie
* Rozwiązywanie problemów i
* Instruktaż

## Jak tworzyć pliki MAML?

Pliki MAML można tworzyć przy użyciu jednej z następujących metod:

* Korzystanie z Sandcastle - Wykorzystuje zestaw schematów i plików wykonywalnych programów do generowania pliku pomocy. To narzędzie zostało jednak wycofane.
* Korzystanie z DocProject — wtyczki Microsoft Visual Studio, którą można uruchomić z poziomu Microsoft Visual Studio w celu wygenerowania treści pomocy.

Pliki MAML można tworzyć za pomocą Sandcastle, zestawu schematów .XSL i plików wykonywalnych programów. Można je również tworzyć za pomocą DocProject, dodatku do narzędzia do tworzenia pomocy programu Microsoft Visual Studio.

## Bibliografia

* [Utwórz pomoc opartą na XML za pomocą PlatyPS](https://learn.microsoft.com/en-us/powershell/scripting/dev-cross-plat/create-help-using-platyps?view=powershell-7.2)
* [Język znaczników pomocy Microsoft](https://en.wikipedia.org/wiki/Microsoft_Assistance_Markup_Language)

# AML — plik językowy Arc Macro

## Co to jest plik ARC Macro AML?

Plik AML (ARC Macro Language) to plik skryptowy generowany za pomocą aplikacji ArcInfo Workstation GIS. Jest napisany w ARC Macro Language, który jest zastrzeżonym językiem algorytmicznym wysokiego poziomu do tworzenia aplikacji GIS w ArcInfo. AML został zaprojektowany przez ESRI w 1986 roku i służył do tworzenia aplikacji z poziomu wiersza poleceń systemu ARCINFO GIS. Będąc plikiem skryptowym, pliki AML mogą zawierać polecenia skryptowe do wykonywania szeregu zadań, takich jak tworzenie komponentów interfejsu użytkownika i manipulowanie danymi mapy.

## Format pliku AML — więcej informacji

AML, będąc plikami skryptowymi, zapisuje informacje na dysku jako zwykłe pliki tekstowe. Jest zgodny ze składnią AML opartą na języku powłoki CPL systemu operacyjnego PRIMOS. Język AML został zastąpiony strukturą geoprzetwarzania ESRI, która jest częścią pakietu ArcGIS i wykorzystuje ArcObjects do zapewniania wsparcia programistycznego za pośrednictwem VBA lub Python.

## Bibliografia

* [Język makr ARC](https://en.wikipedia.org/wiki/ARC_Macro_Language)
* [Korzystanie z AML z narzędziami skryptowymi](https://desktop.arcgis.com/en/arcmap/latest/analyze/creating-tools/using-amls-with-script-tools.htm)

