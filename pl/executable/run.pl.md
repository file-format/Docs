{
  "date" : "2023-01-31",
  "keywords" :["plik uruchamiający", "co to jest plik uruchamiający", "plik", "jak otworzyć plik uruchamiający", "rozszerzenie pliku uruchamiającego", "rozszerzenie"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się więcej o formacie pliku RUN i interfejsach API, które umożliwiają tworzenie i otwieranie plików RUN.",
  "title" :"Format pliku RUN - plik wykonywalny systemu Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Czym jest plik RUN?

Format pliku .run jest powszechnie używany do dystrybucji instalatorów oprogramowania lub aplikacji w środowisku Linux. Aby zainstalować oprogramowanie, musisz uczynić plik wykonywalnym, co można zrobić za pomocą następującego polecenia:

```bash
chmod +x file_name.run 
```

Następnie możesz uruchomić plik za pomocą następującego polecenia:

```bash
./file_name.run 
```

Proces instalacji może się różnić w zależności od konkretnego pliku i programu, który próbujesz zainstalować.

Format pliku .run to rodzaj skryptu powłoki używanego do dystrybucji instalatorów oprogramowania lub aplikacji w środowisku Linux. Jest to samodzielny pakiet zawierający wszystko, co potrzebne do zainstalowania oprogramowania, w tym pliki binarne, biblioteki i pliki konfiguracyjne.

Należy pamiętać, że pliki .run mogą również zawierać złośliwy kod, dlatego zawsze dobrze jest sprawdzić źródło pliku i przeskanować go w poszukiwaniu wirusów przed uruchomieniem.

Ponadto niektóre pliki .run mogą wymagać uprawnień roota do uruchomienia i instalacji, dlatego może być konieczne użycie polecenia "sudo", aby uruchomić plik z podwyższonymi uprawnieniami:

```bash
sudo ./filename.run
```

## Jak otworzyć plik RUN?

Aby otworzyć plik .run, musisz uczynić go wykonywalnym, co można zrobić za pomocą polecenia "chmod":

```bash
chmod +x filename.run 
```

Gdy plik stanie się wykonywalny, możesz go uruchomić, wpisując:

```bash
./filename.run
```

Uruchomienie pliku .run to nie to samo, co otwarcie go w edytorze tekstu. Uruchomienie pliku .run spowoduje wykonanie zawartych w nim instrukcji, od instalacji programu po uruchomienie skryptu. Aby wyświetlić zawartość pliku .run, musisz otworzyć go w edytorze tekstu, takim jak nano lub vim:

```
nano filename.run
```
Lub
```
vim filename.run
```

## Bibliografia
* [Jak uruchomić pliki .bin i .run w Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


