{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik OAM - Format pliku widgetu Adobe Edge Animate",
  "description" :"Dowiedz się, czym jest plik OAM i interfejsach API, które umożliwiają tworzenie i otwieranie pliku OAM.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Czym jest plik OAM?

Plik .oam to animowany plik widgetu wyeksportowany z Adobe Edge Animate Widget. Animacje wyeksportowane jako plik widżetu OAM można wstawiać do innych aplikacji firmy Adobe, takich jak dokumenty InDesign ([plik INDD](/pl/page-description-language/indd/), Dreamweaver i Muse. Pliki OAM są jak pakiety wdrożeniowe, które można łatwo wstawiane do innych projektów Adobe w celu wykorzystania ich. Pliki OAM zawierają informacje o zasobach animacji, zachowaniach i kodzie ActionScript. Możesz utworzyć plik OAM, publikując projekt Adobe Animate [plik .AN](/pl/web/an/) .
Użytkownicy mogą tworzyć pliki OAM, publikując je z projektu Edge Animate (plik .AN).

## Format pliku OAM

Plik OAM jest zapisywany na dysku jako skompresowane archiwum [ZIP](/pl/compression/zip/). Oznacza to, że możesz zmienić nazwę rozszerzenia pliku na .zip i rozpakować go za pomocą dowolnego narzędzia do kompresji, takiego jak WinZIP lub WinRAR. Zmniejszony rozmiar pliku ułatwia przesyłanie i udostępnianie animacji innym użytkownikom za pośrednictwem Internetu.

### Struktura pliku OAM

Wewnętrzna struktura pliku .oam jest zastrzeżona i nie jest publicznie udokumentowana przez firmę Adobe. Wiadomo jednak, że pliki .oam zawierają zbiór plików i zasobów (takich jak grafika, dźwięk i kod ActionScript) spakowanych w jednym pliku. Zawartość pliku .oam może obejmować pliki [XML](/pl/web/xml/), pliki SWF i inne pliki zasobów. Dokładna struktura pliku .oam zależy od konkretnej wersji programu Adobe Animate użytej do jego utworzenia, a także od rodzaju animacji i zasobów zawartych w pliku.

Plik OAM zawiera następujące informacje.

`Zasoby:` Informacje o zasobach graficznych, audio i wideo użytych w animacji.

`Zachowania:` Opisy działań i interakcji zachodzących w animacji.

`Kod ActionScript:` Kod używany do kontrolowania zachowania i interaktywności animacji.

`Ustawienia publikowania:` Informacje o platformie i formacie, w jakim animacja zostanie opublikowana, np. HTML5 lub AIR.

`Metadane:` Dodatkowe informacje, takie jak autor animacji, data utworzenia i numer wersji.

## Jak otworzyć plik OAM?

Do otwierania plików OAM możesz używać następujących aplikacji.

* Adobe Edge Animate CC (wycofane)
*Adobe Animacja 2023
*Adobe InDesign 2023
*Adobe Dreamweaver 2021

## Bibliografia

* [Publikowanie OAM](https://helpx.adobe.com/animate/using/OAM-publishing.html)

