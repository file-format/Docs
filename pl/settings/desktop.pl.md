{
"data": "2023-05-31",
  "keywords": [
"plik pulpitu",
"co to jest plik pulpitu",
"co zawiera plik na pulpicie",
"przykładowy plik pulpitu",
"jak otworzyć plik pulpitu",
"jaki jest format pliku na komputer",
"plik",
"rozszerzenie pliku na pulpicie",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku DESKTOP - plik wejściowy pulpitu",
  "description":"Dowiedz się o formacie DESKTOP i interfejsach API, które umożliwiają tworzenie i otwieranie plików DESKTOP.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "31.05.2023"
}

## Co to jest plik DESKTOP?

Plik .desktop to plik konfiguracyjny używany w środowiskach graficznych systemu Linux do definiowania skrótów do aplikacji i programów uruchamiających. Dostarcza metadanych o aplikacji, takich jak jej nazwa, ikona, polecenie do wykonania i inne właściwości. Pliki te są zwykle używane do tworzenia skrótów w menu aplikacji, programach uruchamiających pulpit lub panelach w systemach opartych na systemie Linux.

## Co zawiera plik DESKTOP?

Plik .desktop ma określony format i zawiera kilka kluczowych pól:

- **[Wpis na pulpicie]:** To jest nagłówek głównej sekcji pliku .desktop.
- **Nazwa:** Określa nazwę aplikacji.
- **Komentarz:** Zawiera krótki opis lub komentarz dotyczący aplikacji.
- **Exec:** Definiuje polecenie do wykonania podczas uruchamiania aplikacji.
- **Ikona:** Określa ścieżkę do pliku ikony powiązanego z aplikacją.
- **Terminal:** Określa, czy aplikacja ma być uruchamiana w oknie terminala.
- **Typ:** Określa typ wpisu, np. "Aplikacja" lub "Link".
- **Kategorie:** Określa kategorie lub grupy, w ramach których aplikacja ma być wyświetlana w menu.
- **StartupNotify:** Określa, czy środowisko graficzne powinno wyświetlać powiadomienie o uruchomieniu aplikacji.
- **NoDisplay:** Określa, czy aplikacja ma być ukryta w menu.
- **Akcje:** Określa dodatkowe akcje, które można wykonać w aplikacji, takie jak otwarcie określonego pliku.

## Przykładowy plik DESKTOP

Oto przykład pliku .desktop fikcyjnego edytora tekstu o nazwie "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

W tym przykładzie plik .desktop definiuje aplikację "MyTextEditor" wraz z powiązanymi z nią właściwościami. Zawiera także dwie dodatkowe akcje: "Otwórz nowe okno" i "Otwórz istniejący plik", do których można uzyskać dostęp z menu kontekstowego programu uruchamiającego aplikacje.

Umieszczając plik .desktop w określonych katalogach, takich jak `/usr/share/applications` lub `~/.local/share/applications`, środowisko graficzne rozpozna go i odpowiednio wyświetli aplikację w menu lub umożliwi jej uruchomienie z pulpit.

## Jak otworzyć plik DESKTOP?

Kilka programów może otwierać i obsługiwać pliki .desktop. Programy te to zazwyczaj menedżery plików lub środowiska graficzne w systemach opartych na systemie Linux. Oto kilka przykładów:

- **Nautilus (Pliki):** Domyślny menedżer plików dla środowiska graficznego GNOME.
- **Nemo:** Menedżer plików dla środowiska komputerowego Cinnamon.
- **Dolphin:** Domyślny menedżer plików dla środowiska graficznego KDE Plasma.
- **Thunar:** Domyślny menedżer plików dla środowiska graficznego Xfce.
- **Edytor menu KDE:** Narzędzie specyficzne dla środowiska graficznego KDE Plasma, które pozwala przeglądać i edytować pliki .desktop.

Te menedżery plików i środowiska graficzne zapewniają graficzny interfejs do zarządzania plikami .desktop. Umożliwiają przeglądanie i edycję właściwości plików .desktop, tworzenie programów uruchamiających aplikacje oraz organizowanie skrótów w menu aplikacji lub na pulpicie.

Pliki .desktop są zwykłymi plikami tekstowymi, więc można je także otwierać i edytować za pomocą wybranego edytora tekstu. Wystarczy kliknąć prawym przyciskiem myszy plik .desktop i wybrać opcję "Otwórz za pomocą" lub "Otwórz za pomocą innej aplikacji", aby wybrać edytor tekstu z listy zainstalowanych programów.

## Jaki jest format pliku DESKTOP?

Format pliku .desktop ma określoną strukturę i format. Jest to zwykły plik tekstowy z zestawem par klucz-wartość zorganizowanych w sekcje. Oto przegląd formatu:

- **Nagłówki sekcji:** Każda sekcja zaczyna się od nagłówka ujętego w nawiasy kwadratowe ([]). Sekcja główna nosi zazwyczaj nazwę [Wpis na pulpicie] i zawiera główne metadane aplikacji lub programu uruchamiającego.
- **Pary klucz-wartość:** w każdej sekcji definiujesz właściwości za pomocą par klucz-wartość. Format to "Klucz=Wartość". Klucz identyfikuje właściwość, a wartość zapewnia odpowiednie dane.
- **Składnia właściwości:** Wartości właściwości mogą być różnych typów, w tym ciągi znaków, wartości logiczne, ścieżki plików lub listy. Format każdej wartości właściwości zależy od jej typu.
- **Komentarze:** Możesz dołączyć komentarze do pliku .desktop, używając symbolu "#". Wszystko, co następuje po znaku "#" w linii, jest uznawane za komentarz i ignorowane.

## Bibliografia
* [Pliki wejściowe pulpitu] (https://www.baeldung.com/linux/desktop-entry-files)

