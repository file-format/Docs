{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APX - Co to jest plik APPX?",
  "description":"Poznaj format pliku APPX i interfejsy API, które mogą tworzyć i otwierać pliki APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Czym jest plik APPX?

Plik APPX to dystrybuowalny format pliku pakietu, który jest używany do dystrybucji i instalacji aplikacji. Został wprowadzony wraz z systemem Windows 8 i został opublikowany w Microsoft Windows Store. Zawiera wszystkie pliki wymagane do zainstalowania aplikacji Windows. Obejmują one metadane, pliki i informacje o poświadczeniach. Bardziej nowoczesnym formatem pliku opakowania jest MSIX, który jest obecnie częściej używany niż APPX.

## Format pliku APPX — więcej informacji

Pliki APPX są zapisywane jako pliki skompresowane w formacie [ZIP](/pl/compression/zip/). Dzięki temu cały pakiet jest plikiem archiwum o zmniejszonym rozmiarze, który można łatwo przesłać do sklepu Microsoft Store.

## Jak wyświetlić pliki w pliku APPX?

Aby wyświetlić zawartość lub pliki w pliku APPX, należy wykonać następujące kroki.

1. Ponieważ pliki APPX są przechowywane jako skompresowane pliki ZIP, zmień nazwę pliku na rozszerzenie .zip
1. Użyj dowolnego narzędzia do dekompresji, takiego jak 7-Zip, WinZip lub WinRAR, aby wyodrębnić pliki zawarte w pliku APPX

## Jak utworzyć plik APPX?

Istnieją dwie metody tworzenia plików APPX.

1. Korzystanie z MakeApp.exe — [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) służy do tworzenia obu pakiety aplikacji (.msix lub .appx) i pliki pakietów aplikacji .msixbundle lub .appxbundle). Ponadto może wyodrębniać pliki z pakietu aplikacji. MakeApp.exe jest dostępny z Windows 10 SDK i może być używany z wiersza poleceń.
1. Korzystanie z programu Microsoft Visual Studio — programiści zwykle [tworzą pliki APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) przy użyciu programu Microsoft Visual Studio. Po zakończeniu opracowywania aplikacji i przygotowaniu aplikacji do opublikowania plik pakietu APPX można utworzyć, publikując go z poziomu programu Visual Studio.

## Bibliografia

* [Utwórz pakiet lub pakiet MSIX za pomocą MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Utwórz pliki APPX za pomocą Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

