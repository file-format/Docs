{
  "date" : "2019-10-11",
  "keywords" :["plik emf", "format pliku emf", "co to jest plik emf", "plik", "przykład emf", "rozszerzenie pliku emf", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF – rozszerzony format metaplików",
  "description":"Poznaj format pliku EMF i interfejsy API, które mogą tworzyć i otwierać pliki EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik EMF?

**Ulepszony format metaplików (EMF)** umożliwia przechowywanie obrazów graficznych niezależnie od urządzenia. Metapliki EMF składają się z rekordów o zmiennej długości w porządku chronologicznym, które mogą renderować zapisany obraz po przeanalizowaniu na dowolnym urządzeniu wyjściowym. Te rekordy o zmiennej długości mogą być definicjami zamkniętych obiektów, poleceniami do rysowania i właściwościami graficznymi, które mają kluczowe znaczenie dla dokładnego renderowania obrazu. Gdy urządzenie otwiera metaplik EMF przy użyciu własnego środowiska graficznego, proporcje, wymiary, kolory i inne właściwości graficzne oryginalnego obrazu pozostają takie same, niezależnie od platformy urządzenia otwierającego.

## Krótka historia ##

W 1990 roku firma Microsoft zaprojektowała plik obrazu w formacie Windows Metafile ([WMF](/pl/image/wmf/)) dla systemu Microsoft Windows. Windows Metafiles to 16-bitowy format, który może zawierać niektóre komponenty mapy bitowej. WMF może składać się z grafiki wektorowej i jest przeznaczony do przenoszenia między różnymi aplikacjami. W 1993 roku Win32/GDI ogłosiło Enhanced Metafile (EMF), nowszą wersję o zwiększonej elastyczności i skalowalności. EMF używany również jako polecenia języka graficznego do uruchamiania sterowników drukarki. Microsoft zaleca teraz rozszerzony format metaplików (EMF) zamiast formatu Windows (WMF). Wraz z wprowadzeniem systemu Windows XP wydano wersję Enhanced Metafile Format Plus (EMF+). Ta nowsza wersja znajduje swoją drogę poprzez serializację wywołań API GDI+, podobnie jak WMF/EMF rejestruje wywołania GDI. Istnieje skompresowana gzip wersja EMF znana jako EMZ.

## Format metapliku EMF ##

Poniżej przedstawiono podstawowe elementy ulepszonego formatu metaplików:

* EMR_HEADER (wersja, rozmiar, rozdzielczość obrazu przy tworzeniu)
* Tabela dla obiektów GDI
* Zarezerwowana paleta (opcjonalnie)
* Rekordy metaplików ułożone w strukturę tablicową (ustawienia właściwości, zdefiniowane obiekty, polecenia rysowania)
* Rekord EMR_EOF (ostatni rekord w metapliku EMF)

## Wersje EMF ##
* **Oryginał**: Oryginalna wersja określa zapis niezbędny do zachowania oryginalnego obrazu i zachowania jego niezależności od urządzenia. Ponadto obsługuje zapis zawierający obiekty graficzne oraz polecenia do rysowania.
* **Wersja 1**: Druga wersja EMF poprawiła elastyczność i niezależność od urządzeń, dodając zapis dla formatu pikseli i udostępniając polecenie OpenGL.
* **Wersja 2**: Trzecia wersja zwiększyła dokładność, dodając system metryczny do pomiaru odległości powierzchni urządzenia, dzięki czemu zapis jest bardziej skalowalny.

## Ulepszone rekordy metaplików ##

Rekordy metaplików są ułożone w postaci tablicy. Rekordy te mają strukturę ENHMETARECORD i zmienną długość. ENHMETARECORD określa dane, które definiują funkcje GDI do tworzenia obrazu przy użyciu rozszerzonego formatu metaplików. Struktura **ENHMETAHEADER** jest zawsze pierwszym rekordem w tym formacie. Ten nagłówek EMF zawiera następujące informacje.

Każdy rekord rozszerzonego metapliku ma na początku dwóch członków EMR (zapewnia podstawową strukturę). Pierwszy element rozpoznaje funkcję GDI (parametry są używane w rekordzie), która określa typ rekordu i jest znana jako iType. Drugi element nSize określa rozmiar każdego rekordu. Pozostałe parametry (jeśli występują) i dodatkowe dane ułożone bezpośrednio pod nSize. Bezpośrednio po nagłówku może znajdować się opcjonalny opis tekstowy. Nazwa obrazu i autor są zapisane w tym opisie tekstowym. Paleta, której obecność jest opcją, określa kolory używane w rozszerzonym tworzeniu metaplików. Pozostałe rekordy służą do określenia funkcji GDI, która jest niezbędna przy tworzeniu obrazu.

W każdym metapliku powinien znajdować się co najmniej jeden rekord EMF. Informacje o przechodzeniu z jednego rekordu do drugiego zależą od rekordów EMF, więc te rekordy muszą być ułożone obok siebie. W dowolnym rekordzie w metapliku, z wyjątkiem EOF_record, długość tego konkretnego rekordu definiuje przejście do następnego rekordu.

## Ulepszone tworzenie metaplików ##

Funkcja **CreateEnhMetaFile** służy do tworzenia rozszerzonego metapliku. Argumenty tej funkcji służą do wymiarowania i przechowywania obrazu na dysku/pamięci. Ponadto funkcja ta wymaga wymiaru urządzenia, w którym obraz pojawił się jako pierwszy (urządzenie referencyjne) oraz kontekstu urządzenia referencyjnego (DC). Tak więc argumenty do obsługi tego kontrolera domeny muszą być podane podczas wywoływania funkcji **CreateEnhMetaFile**. Składnia funkcji jest następująca:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** uchwyt do urządzenia referencyjnego.

**lptoFilename:** Wskaźnik do nazwy pliku.

**lprc:** Wskaźnik struktury owalnej określa wymiary obrazka w mm.

**lpDesc:** wskaźnik do ciągu dla tytułu obrazu i nazwy aplikacji, która utworzyła obraz.

## Rozszerzone operacje na metaplikach ##

Poniżej przedstawiono zadania, które można wykonać za pomocą uchwytu do rozszerzonego metapliku.

* Wyświetl i edytuj zapisane zdjęcie.
* Twórz ulepszone kopie metaplików.
* Pobierz kopię nagłówka EMF, opcjonalny opis i wersję binarną rozszerzonego metapliku
* Podsumuj kolory w palecie.

## Obiekty graficzne ##

W operacjach rysowania i malowania obiekty graficzne mogą być tworzone przez zapisy tworzenia obiektów i zapisywane do dalszego wykorzystania. Rekord `EMR_SELECTOBJECT` może pobrać te obiekty graficzne przy użyciu kontekstu urządzenia odtwarzającego. Pióra, palety, pędzle, przestrzenie kolorów, czcionki i obiekty podstawowe to niektóre typy obiektów wielokrotnego użytku.

## Kolejność bajtów ##

Format little-endian służy do przechowywania danych w rekordach metaplików.

## Wersjonowanie ##

Format pliku EMF został zmieniony dwukrotnie. Zmienione wersje to oryginał, rozszerzenie 1 i rozszerzenie 2. Wersje rozszerzone zawierają zapisy OpenGL i opcjonalny deskryptor wewnętrznego formatu pikseli. Dla wyświetlanych wymiarów dodano jednostkę miary w mililitrach.

## Bibliografia ##

* [Metapliki w rozszerzonym formacie | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Ulepszony format i specyfikacja metaplików](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

