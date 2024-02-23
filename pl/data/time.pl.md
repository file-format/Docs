{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Plik TIME - Co to jest plik .time? Czas utworzenia pliku w systemie Linux",
  "description" : "Dowiedz się o pliku TIME i dowiedz się, kiedy plik został utworzony w systemie Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-pl",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Co to jest plik TIME?

Format pliku TIME był używany przez system internetowy o nazwie LIGHT, który pomagał użytkownikom nagrywać, organizować i udostępniać swoje życie. Zasadniczo przechowywał zbiór postów i reprezentował folder na stronie życia użytkownika w systemie.

## Jak dowiedzieć się, kiedy plik został utworzony w systemie Linux

W systemie Linux możesz użyć polecenia `stat`, aby dowiedzieć się, kiedy plik został utworzony. Oto jak możesz to zrobić:

Otwórz terminal i wpisz następujące polecenie:

```
stat <file_path>
```

Zamień `<file_path> ` ze ścieżką do interesującego Cię pliku. Na przykład:

```
stat /path/to/your/file.txt
```

To polecenie wyświetli różne informacje o pliku, w tym czas jego utworzenia. Poszukaj linii zaczynającej się od Birth” lub File:”. Czas narodzin” wskazuje, kiedy plik został utworzony w systemie plików.

Oto przykład tego, jak mogą wyglądać dane wyjściowe:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

W tym przykładzie czas Urodzenia” wskazuje, kiedy plik został utworzony.

