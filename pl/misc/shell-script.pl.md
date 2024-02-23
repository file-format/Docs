{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Skrypt powłoki — jak go uruchomić w systemie Ubuntu i Linux",
  "description":"Dowiedz się, czym jest skrypt powłoki i jak go uruchomić w systemach Ubuntu i Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-pl",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Co to jest skrypt powłoki?

Skrypty powłoki polegają na pisaniu serii poleceń w zwykłym pliku tekstowym, często nazywanym **skryptem powłoki**. Skrypty te są wykonywane przez powłokę, która jest interpreterem wiersza poleceń. Do najpopularniejszych muszli należą

1. Bash (Bourne Again SHELL)
2. Zsh (powłoka Z)
3. Ryba.

Skrypty powłoki mogą obejmować zarówno proste, jednowierszowe, jak i złożone programy i służą do wykonywania szerokiej gamy zadań, takich jak manipulowanie plikami, administrowanie systemem i automatyzacja powtarzalnych zadań.

## Korzyści ze skryptów powłoki:

1.  **Automatyzacja:** skrypty powłoki pozwalają użytkownikom automatyzować powtarzalne zadania, oszczędzając czas i zmniejszając ryzyko błędu ludzkiego.
    
2.  **Dostosowywanie:** Użytkownicy mogą tworzyć skrypty dostosowane do ich konkretnych potrzeb, zapewniając wysoki stopień dostosowania.
    
3.  **Przetwarzanie wsadowe:** Skrypty powłoki doskonale nadają się do obsługi zadań przetwarzania wsadowego, w których należy wykonać wiele poleceń po kolei.
    
4.  **Administracja systemem:** Skrypty powłoki są powszechnie używane do zadań administracyjnych systemu, takich jak tworzenie kopii zapasowych, rotacja dzienników i instalacja oprogramowania.

## Pisanie prostego skryptu powłoki:

Stwórzmy podstawowy skrypt powłoki, który wypisuje wiadomość powitalną. Otwórz edytor tekstu i utwórz plik o nazwie `greeting.sh`. Dodaj następujące linie:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Zapisz plik i uczyń go wykonywalnym, uruchamiając następujące polecenie w terminalu:

```
chmod +x greeting.sh
```

Teraz możesz wykonać skrypt:

```
./greeting.sh
```

Dane wyjściowe powinny być następujące:

```
Hello, welcome to the world of shell scripting!
```

## Uruchamianie skryptów powłoki w systemach Ubuntu i Linux:

Teraz omówimy **jak uruchomić plik .sh w Ubuntu i Linux**.

1.  **Uczyń skrypt wykonywalnym:** Przed uruchomieniem skryptu powłoki upewnij się, że jest on wykonywalny. Użyj polecenia `chmod`, jak pokazano wcześniej.
    
2.  **Przejdź do katalogu skryptów:** Otwórz terminal i użyj polecenia `cd`, aby przejść do katalogu zawierającego skrypt powłoki.
    
3.  **Uruchom skrypt:** Wykonaj skrypt, wpisując `./nazwaskryptu.sh` w terminalu, zastępując nazwaskryptu” rzeczywistą nazwą skryptu.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Korzystanie z polecenia Bash:** Jeśli skrypt zaczyna się od `#!/bin/bash` (znanego jako **shebang**), możesz go także uruchomić za pomocą polecenia `bash`.

```
bash greeting.sh
```

## Co oznacza $@ w skrypcie powłoki?

W skrypcie powłoki `$@` reprezentuje wszystkie argumenty wiersza poleceń przekazane do skryptu. Jest często używany do odwoływania się do listy argumentów jako oddzielnych jednostek. Używany w cudzysłowie, np. `$@`, zachowuje indywidualne argumenty, uwzględniając spacje i znaki specjalne.

Oto krótkie wyjaśnienie:

- `$@`: Reprezentuje wszystkie parametry pozycyjne (argumenty) przekazane do skryptu lub funkcji. Każdy argument jest traktowany jako osobne słowo.
    
- `$@`: W przypadku podwójnego cudzysłowu zachowuje separację argumentów, dopuszczając spacje lub znaki specjalne w poszczególnych argumentach.
    

Oto prosty przykład ilustrujący:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Po uruchomieniu tego skryptu z argumentami, na przykład:

```
bash example.sh arg1 "argument 2" arg3
```

Wygenerowałoby to:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Jak widać, `$@` reprezentuje wszystkie argumenty, a `$@` zachowuje poszczególne argumenty, nawet jeśli zawierają spacje.

