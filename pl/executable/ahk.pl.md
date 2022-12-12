{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku AHK i interfejsy API, które mogą tworzyć i otwierać pliki AHK.",
  "title" :"Format pliku AHK — plik skryptu AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Czym jest plik AHK?

Plik AHK to plik skryptu wygenerowany za pomocą aplikacji AutoHotkey, który służy do automatyzacji zadań w systemie Microsoft Windows. Zawiera instrukcje automatyzacji zadań za pomocą klawiszy skrótów, które można wykorzystać do wykonywania natychmiastowych akcji. Plik jest wykonywany przez AutoHotkey, a wszystkie akcje są wykonywane sekwencyjnie. Pliki AHK są wystarczająco wydajne, aby wykonywać złożone zadania za pomocą skrótów klawiszowych zdefiniowanych za pomocą skrótów klawiszowych. Pliki AHK można otwierać za pomocą edytorów tekstu, takich jak Microsoft Notepad i Notepad ++.

## Format pliku AHK

Pliki AHK są zapisywane na dysku jako zwykłe pliki tekstowe i zawierają linie kodu, które mogą być wykonywane przez AutoHotkey. AutoHotkey to darmowy język skryptowy typu open source, który umożliwia użytkownikom tworzenie prostych i złożonych skryptów w celu wykonywania czynności, takich jak wypełnianie formularzy, automatyczne klikanie, wykonywanie makr itp. Minimalny plik AHK może wykonać jedną akcję, a następnie wyjść .

Dostępne są narzędzia, których można użyć do konwersji plików AHK na pliki [Exe](/pl/executable/exe/).

### Przykład AHK

Poniższy przykład używa klawisza Win+Z do uruchomienia Notatnika Microsoft lub przeniesienia go na wierzch, jeśli jest już uruchomiony.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Jak utworzyć plik AHK?

Aby utworzyć plik AHK, można wykonać następujące kroki. Zakładają one, że AutoHotkey jest już zainstalowany na komputerze.

* Kliknij prawym przyciskiem myszy na pulpicie.
* Znajdź „Nowy” w menu.
* Kliknij „AutoHotkey Script” w menu „Nowy”.
* Nadaj skryptowi nową nazwę.
* Znajdź nowo utworzony plik na pulpicie i kliknij go prawym przyciskiem myszy.
* Kliknij „Edytuj skrypt”.
* Powinno pojawić się okno, prawdopodobnie Notatnik.
* Zapisz plik.

## Bibliografia

* [AutoHotkey](https://www.autohotkey.com/)
* [Plik wsadowy – autorstwa Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

