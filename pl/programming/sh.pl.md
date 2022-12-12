{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Plik skryptu powłoki Bash",
  "description":"Poznaj format pliku SH i interfejsy API, które mogą tworzyć i otwierać pliki SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Czym jest plik SH?

Plik z rozszerzeniem .sh to plik poleceń języka skryptowego, który zawiera program komputerowy do uruchomienia przez powłokę Unix. Może zawierać szereg poleceń, które są uruchamiane sekwencyjnie w celu wykonywania operacji, takich jak przetwarzanie plików, wykonywanie programów i inne tego typu zadania. Są one wykonywane z interfejsu wiersza poleceń przez użytkownika lub wsadowo w celu wykonywania wielu operacji jednocześnie. Pliki skryptów można otwierać w edytorach tekstu, takich jak Notatnik, Notepad ++, Vim, Apple Terminal i innych podobnych aplikacjach w systemach Windows, MacOS i Linux OS.

## Format pliku SH

Pliki SH są zapisywane zwykłym tekstem zgodnie ze zdefiniowaną składnią. Te pliki skryptów obsługują:

* `Komentarze` - Komentarze zaczynają się od # i są ignorowane przez powłokę.
* `Skróty` - Można ich użyć do zmiany nazwy polecenia w celu szybkiego i łatwego wykonania.
* `Zadania wsadowe` - kilka poleceń może być wykonywanych automatycznie, które w innym przypadku musiałyby być wprowadzane ręcznie. Eliminuje to konieczność czekania, aż użytkownik uruchomi każdy etap sekwencji.
* `Uogólnienie` - Za pomocą prostych pętli osiąga się znacznie większe uogólnienie dla operacji takich jak konwersja obrazów z jednego formatu do drugiego.

## Przykład pliku SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Jak uruchomić plik SH?
Pliki SH zwykle działają w systemie Linux, nawet w systemie Windows musisz połączyć się z terminalem Linux za pomocą oprogramowania takiego jak Putty, aby uruchomić pliki sh. Poniżej przedstawiono kroki, aby uruchomić plik SH na terminalu Linux.

1. Otwórz terminal Linux i przejdź do katalogu, w którym znajduje się plik SH.
2. Używając polecenia `chmod`, ustaw uprawnienia do wykonywania swojego skryptu (jeśli nie zostały jeszcze ustawione).
3. Uruchom skrypt, korzystając z jednej z poniższych opcji
1. `./nazwa_pliku.sh`
2. `sh nazwa_pliku.sh`
3. `nazwa-skryptu-bash-tutaj.sh`

## Bibliografia

* [Bashscripting dla początkujących](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

