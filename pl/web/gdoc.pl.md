{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik GDOC - skrót do Dokumentów Google",
  "description":"Dowiedz się, czym jest plik GDOC i interfejsy API, które mogą tworzyć i otwierać pliki GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Czym jest plik GDOC?

Plik GDOC to plik skrótu wskazujący plik znajdujący się na Dysku Google, usłudze przechowywania dokumentów w chmurze. Gdy klient Dysku Google jest zainstalowany na komputerze i tworzony jest w nim dokument, dysk tworzy dokument w internetowym magazynie w chmurze i zapisuje [URL](/pl/web/url/) tego dokumentu w pliku GDOC w lokalnym Google Folder na dysku. Po dwukrotnym kliknięciu tego pliku skrótu domyślna przeglądarka internetowa otwiera dokument z lokalizacji [URL](/pl/web/url/). Jeśli ten plik skrótu zostanie przeniesiony z tego folderu, łącze do dokumentu online zostanie zerwane.

## Format pliku GDOC — więcej informacji

Plik GDOC zawiera skrót do dokumentu online zapisanego w formacie pliku [JSON](/pl/web/json/). Przeglądarka otwierająca pliki GDOC odczytuje informacje o adresie URL i otwiera połączony dokument do wyświetlenia, pod warunkiem, że użytkownik jest zalogowany na to konto Google, na którym przechowywany jest dokument. Pliki GDOC nie zawierają treści dokumentu.

### Przykład pliku GDOC

Plik GDOC można otworzyć w edytorze tekstu, a jego zawartość wygląda następująco.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Jak widać, zawartość jest sformatowana w formacie JSON z adresem URL dokumentu i powiązanym identyfikatorem dokumentu.

## Bibliografia

* [Dokumenty Google nie otwierają plików gdoc ani docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=pl )

