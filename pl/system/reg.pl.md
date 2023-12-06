{
"data": "2023-03-07",
  "keywords": [
"plik rej",
"co to jest plik reg",
"plik",
"rozszerzenie pliku reg",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku REG - plik rejestru systemu Windows",
  "description":"Dowiedz się o formacie REG i interfejsach API, które umożliwiają tworzenie i otwieranie plików REG.",
"tytuł linku": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Czym jest plik REG?

Plik REG to format pliku używany do importowania lub eksportowania danych rejestru systemu Windows. Rejestr systemu Windows to hierarchiczna baza danych przechowująca ustawienia konfiguracyjne i opcje systemu operacyjnego Windows oraz zainstalowanych aplikacji. Rejestr zawiera takie informacje, jak preferencje użytkownika, ustawienia aplikacji, dane konfiguracyjne sprzętu i oprogramowania i inne.

Plik REG ma zazwyczaj rozszerzenie ".reg" i jest zwykłym plikiem tekstowym zawierającym serię wpisów rejestru i wartości w określonym formacie. Format składa się z sekcji nagłówka identyfikującej plik jako plik rejestru, po której następuje seria par kluczy i wartości reprezentujących wpisy rejestru.

## Format pliku REG — więcej informacji

Oto przykład formatu pliku reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Pierwsza linia pliku określa wersję edytora rejestru. Poniższe wiersze zawierają wpisy rejestru w formacie ścieżki klucza, po których następuje nazwa wartości i dane wartości. W tym przykładzie plik reg zawiera dwa wpisy: jeden, który dodaje program o nazwie "Example.exe" do listy startowej systemu Windows, a drugi ustawia wartość "Ukryty" w zaawansowanych ustawieniach Eksploratora Windows na "true".

Pliki Reg można tworzyć i edytować za pomocą edytora tekstu, takiego jak Notatnik. Są one często używane do celów tworzenia kopii zapasowych i przywracania, a także do konfigurowania wielu komputerów z tymi samymi ustawieniami rejestru.

## Importuj lub eksportuj rejestr systemu Windows

Plik REG to typ pliku używany do importowania lub eksportowania danych z rejestru systemu Windows. Rejestr systemu Windows to hierarchiczna baza danych przechowująca ustawienia konfiguracyjne i opcje systemu operacyjnego Windows oraz zainstalowanych aplikacji. Rejestr zawiera takie informacje, jak preferencje użytkownika, ustawienia aplikacji, dane konfiguracyjne sprzętu i oprogramowania i inne.

Plików Reg można używać do tworzenia lub modyfikowania wpisów rejestru i często są używane do celów tworzenia kopii zapasowych i przywracania, a także do konfigurowania wielu komputerów z tymi samymi ustawieniami rejestru. Oto jak użyć pliku reg, aby dodać nowy wpis rejestru do rejestru systemu Windows:

1. Utwórz nowy plik tekstowy za pomocą edytora tekstu, takiego jak Notatnik.
2. Wpisz wpis rejestru w odpowiednim formacie. Format składa się z sekcji nagłówka identyfikującej plik jako plik rejestru, po której następuje seria par kluczy i wartości reprezentujących wpisy rejestru. Oto przykład:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Spowoduje to utworzenie nowego klucza o nazwie "Przykład" w kluczu "Oprogramowanie" w gałęzi rejestru bieżącego użytkownika i ustawienie wartości "Ustawienie1" na "Wartość1".

3. Zapisz plik z rozszerzeniem .reg.
4. Kliknij dwukrotnie plik .reg, aby dodać nowy wpis rejestru do rejestru systemu Windows.

Zostaniesz poproszony o potwierdzenie chęci dodania wpisu do rejestru. Po potwierdzeniu nowy wpis zostanie dodany do rejestru i będzie można go zweryfikować za pomocą narzędzia Edytor rejestru.

## Bibliografia
* [Rejestr systemu Windows](https://en.wikipedia.org/wiki/Windows_Registry)

