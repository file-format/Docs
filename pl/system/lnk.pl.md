{
  "date" : "2021-07-15",
  "keywords" :["LNK", "rozszerzenie", "plik", "format", "system", "plik LNK", "link", "pliki LNK", "dokumenty LNK", "aplikacja", "programy" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Format pliku łącza",
  "description":"Poznaj format pliku LNK i interfejsy API, które mogą tworzyć i otwierać pliki LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Czym jest plik LNK? ##

Plik LNK, analogiczny do tożsamości w systemie Mac, jest alternatywą dla systemu Windows lub „łączem”, które służy jako połączenie z oryginalnym folderem dokumentu obrazu lub programem. Zawiera typ, pozycję i nazwę pliku miejsca docelowego skrótu, a także aplikację otwierającą dokument docelowy oraz dodatkowy klawisz skrótu.

W systemie Windows wyprostuj plik, folder lub program wykonywalny i wybierz opcję Utwórz skrót. Lokalizacja formatu pliku oraz katalog „Początek” to dwie podstawowe cechy plików LNK. Format pliku plików LNK jest maskowany, a zakrzywiona strzałka wskazuje, że są to skróty.

## Format pliku LNK ##

Formaty plików LNK zwykle mają tę samą ikonę, co ich pliki docelowe, ale z dodatkiem małej zakrzywionej strzałki, aby pokazać, że plik wskazuje inną lokalizację. Po dwukrotnym kliknięciu skrótu zachowuje się tak, jakby użytkownik dwukrotnie kliknął rzeczywisty plik.

Pliki LNK zawierające skróty do aplikacji mogą mieć właściwości wpływające na działanie programu. Aby zmienić atrybuty, kliknij plik skrótu prawym przyciskiem myszy i wybierz **Właściwości**, a następnie zmień pole Cel.

Zamiast być rozszerzeniami plików, pliki LNK są rozszerzeniami Eksploratora Windows. Jako rozszerzenie terminala dokumenty .lnk mogą być używane tylko w Eksploratorze Windows w celu zastąpienia pliku i mają inne cele w Eksploratorze Windows niż służą jako skrót do dokumentu lokalnego. Te pliki również zaczynają się na literę „L”.

Chociaż tworzone skróty prowadzą do określonych plików i katalogów, mogą przestać działać, jeśli miejsce docelowe zostanie zmienione na inną lokalizację. Eksplorator rozpocznie naprawę folderu skrótów, który wskazuje martwy cel po jego otwarciu.


## Specyfikacja techniczna ##

Tylko wtedy, gdy opcja przeglądania folderów „Ukryj rozszerzenia rozpoznawanych typów plików” jest odznaczona, system Windows nie wyświetla rozszerzenia dokumentu .lnk dla skrótów do dokumentów. Chociaż nie jest to zalecane, można włączyć wyświetlanie rozszerzenia pliku, usuwając właściwość „NeverShowExt” z elementu rejestru systemu Windows w pliku HKEY_CLASSES_ROOT\lnk.

Aby to zrobić, wykonaj następujące kroki:

* Otwórz „Edytor rejestracji”, wpisując „Regedit” w polu wyszukiwania paska zadań i wybierając program
* W aplikacji przejdź do lokalizacji pliku Computer\HKEY HKEY_CLASSES_ROOT\lnk
* Zrób kopię zapasową elementu, klikając go prawym przyciskiem myszy i wybierając opcję Eksportuj
* Wybierz i usuń atrybut „NeverShowExt”.
* Należy ponownie uruchomić system Windows


## Odniesienie ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
