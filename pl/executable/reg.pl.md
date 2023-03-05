{
  "date" : "2021-08-02",
  "keywords" :["plik reg", "format pliku reg", "co to jest plik reg", "plik", "przykład reg", "rozszerzenie pliku reg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku REG i interfejsach API, które mogą tworzyć i otwierać pliki REG.",
  "title" :"REG - Plik Rejestru Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Czym jest plik REG?
Plik REG to po prostu plik tekstowy z rozszerzeniem .reg. Pliki te są zwykle tworzone przez wyeksportowanie typowych kluczy z Rejestru. Pliki te można również wykorzystać jako kopię zapasową rejestru (szczególnie ten krok jest ważny przed wprowadzeniem zmian!). Możesz zobaczyć, że niektóre udostępniły je jako pliki do pobrania w tych samych witrynach, które pokazują, jak wykonać hackowanie rejestru. Plik REG jest przydatny do ręcznego wprowadzania zmian w Rejestrze i eksportowania tych zmian. Po prostu trochę wyczyść plik, a następnie udostępnij go innym.

## Format pliku REG
Format pliku REG został zaprojektowany do eksportowania i importowania części rejestru systemu Windows przy użyciu składni opartej na INI. Rejestr systemu Windows to relacyjna lub hierarchiczna baza danych, która przechowuje ustawienia niskiego poziomu systemu operacyjnego Microsoft Windows i innych aplikacji korzystających z rejestru systemu Windows. Alternatywnie, możemy powiedzieć, rejestr lub rejestr systemu Windows składa się z informacji, opcji, ustawień i innych wartości dla programów i sprzętu zainstalowanego we wszystkich wersjach systemów operacyjnych Microsoft Windows.
### Składnia pliku REG
Oto kilka kluczowych elementów składni pliku REG:
- **RegistryEditorVersion**: Np. „Edytor rejestru systemu Windows w wersji 5.00” dla systemów Windows 2000, Windows XP i Windows Server 2003.
- **Pusta linia**: identyfikuje początek nowej ścieżki rejestru.
- **RegistryPathx**: Ścieżka podklucza zawierającego pierwszą importowaną wartość.
- **DataItemNamex**: Nazwa elementu danych, który chcesz zaimportować.
- **DataTypex**: Typ danych dla wartości rejestru.

Klucze są przechowywane w plikach .reg przy użyciu następującej składni:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Możesz edytować domyślną wartość klucza, używając „@” zamiast „Nazwa wartości”:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Przykład
Oto przykład pliku REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Bibliografia

* [Rejestr systemu Windows — według Wikipedii](https://en.wikipedia.org/wiki/Windows_Registry)
* [Jak dodawać, modyfikować lub usuwać podklucze i wartości rejestru za pomocą pliku .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
