{
  "date" : "2019-12-12",
  "keywords" :["EPS", "plik", "rozszerzenie", "format pliku", "Układ strony", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików EPS i interfejsy API, które mogą tworzyć i otwierać pliki EPS.",
  "title" :"Format pliku EPS - Enkapsulowany plik PostScript",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik EPS?

Plik .eps to plik obrazu zapisywany na dysku w formacie Encapsulated Postscript. Może zawierać dowolną kombinację tekstu, grafiki i obrazów. Pliki EPS mogą również zawierać obraz podglądu mapy bitowej zamknięty w środku do wyświetlania przez aplikacje, które mogą otwierać takie pliki.

## Krótka historia formatu plików EPS

Szybkie spojrzenie na format pliku EPS z perspektywy historii ujawnia następujące informacje:

* Pierwsza wersja EPS została wydana przez firmę Adobe w latach 1985-1988
* Wersja 2.0 specyfikacji EPS została opublikowana w styczniu 1989 roku
* Specyfikacja wersji 3.0 EPS została opublikowana jako odrębny dokument w 1992 roku; to jest najnowsza opublikowana wersja.

EPS, w połączeniu z mechanizmem rozszerzenia Open Structuring Conventions opisanym w klauzuli 9 specyfikacji Adobe PostScript Language Document Structuring Conventions, stanowił podstawę wczesnych wersji formatu pliku Adobe Illustrator Artwork.

## Format pliku EPS

EPS jest zastrzeżonym, ale publicznie udokumentowanym formatem, a specyfikacje formatu plików EPS są publicznie dostępne w celach informacyjnych dla programistów. EPS jest formatem pliku zgodnym z [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Konwencją struktury dokumentów) i wszystkimi zasadami ustanowionymi przez DSC. DSC to specjalny format plików dla dokumentów PostScript firmy Adobe. Każda aplikacja, która twierdzi, że może odczytywać pliki EPS, powinna być zgodna z DSC.

Plik EPS składa się z dwóch głównych sekcji, jak wyjaśniono poniżej.

### Podgląd obrazu ###

Typowy plik EPS zawiera obraz podglądu w formacie przeznaczonym do wygodnego użycia w przepływie pracy obejmującym kilka systemów lub aplikacji. Celem podglądu jest uzyskanie obrazu w formacie, który może renderować większość aplikacji graficznych; podgląd ma zwykle niższą rozdzielczość, wymiary w pikselach i/lub głębię bitową. Plik podglądu może być w jednym z wielu formatów. Specyfikacja EPS_3 wymienia trzy formaty podglądu „specyficzne dla urządzenia”:

* dla Apple Macintosh, obraz PICT używany przez aplikację QuickDraw
* dla komputerów z systemem DOS bitmapa TIFF
* Metaplik systemu Windows.

PICT i Windows Metafile mogą zawierać zarówno dane bitmapowe, jak i grafikę wektorową. Ponadto specyfikacja definiuje bardzo prostą, niezależną od urządzenia reprezentację osadzonego obrazu podglądu z mapą bitową. Ta reprezentacja jest znana jako Encapsulated PostScript Interchange Format (EPSI).

Podgląd EPSI to mapa bitowa reprezentowana w postaci szesnastkowej ASCII, otoczona kilkoma komentarzami PostScript w celu identyfikacji i mająca być prosta i łatwa do przenoszenia. Aby rozróżnić pliki EPS z różnymi formatami podglądu, w specyfikacji EPS zalecono różne rozszerzenia plików DOS i typy plików Macintosh.

### Kod PostScript

Format pliku EPS musi zawierać co najmniej następujące elementy:

* komentarz nagłówka, %!PS-Adobe-3.0 EPSF-3.0
* i komentarz ramki ograniczającej, %%BoundingBox: llx lly urx ury, opisujący granice ilustracji. Te cztery argumenty odpowiadają lewym dolnym (llx, lly) i prawym górnym (urx, ury) rogom obwiedni.

Plik EPS nie może używać żadnego z następujących operatorów:

* urządzenie pasma,
* cleardictstack
* kopiuj stronę
* Usuń stronę
* serwer wyjściowy
* urządzenie ramki
* grestoreall
* initclip
* initgrafika
* macierz początkowa
* zrezygnować
* pasma renderowania
* ustaw globalnie
* ustaw urządzenie strony
* zestaw współdzielony
* rozpoczęcie pracy.

## Konwersja EPS do innych formatów plików

Pliki EPS można konwertować do standardowych formatów graficznych, takich jak [JPG](/pl/image/jpeg/), [PNG](/pl/image/png/), [TIFF](/pl/image/tiff/) i [PDF](/pl/pdf) /) korzystanie z różnych aplikacji np. Adobe Illustrator, Photoshop i PaintShop Pro.

Z powodu [luki w zabezpieczeniach](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) w plikach EPS, Office 2016, Office 2013, Office 2010 i Office 365 wyłączyły możliwość wstawiania plików EPS do dokumentów Office.

## Bibliografia

* [Encapsulated PostScript – Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

