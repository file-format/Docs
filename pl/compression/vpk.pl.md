{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik VPK — format pliku pakietu aplikacji PlayStation Vita",
  "description":"Poznaj format pliku VPK i interfejsy API, które mogą tworzyć i otwierać pliki VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Czym jest plik VPK?

Plik z rozszerzeniem .vpk to skompresowany plik pakietu archiwum, który służy do instalowania aplikacji innych firm na konsoli do gier Sony PlayStation Vita. Te pliki można zainstalować tylko na jailbreak Vita PlayStation firmy HENkaku, która umożliwiła PS Vita i PSTV korzystanie z dostosowanych treści tworzonych przez użytkowników. Plik archiwum VPK zawiera całą zawartość gry, w tym obrazy, takie jak pliki [PNG](/pl/image/png/), pliki ustawień, takie jak [.bin](/pl/disc-and-media/bin/) oraz dowolne konfiguracje w formacie pliku [XML](/pl/web/xml/).

## Format pliku VPK

Pliki VPK są zapisywane na dysku jako standardowe skompresowane archiwa [ZIP](/pl/compression/zip/). Mogą one zawierać wiele folderów i innych powiązanych plików dla aplikacji innych firm, które mają być zainstalowane na Vita Gaming Console. Aby wyświetlić zawartość pliku pakietu VPK, zmień jego rozszerzenie z .vpu na .zip i rozpakuj zawartość za pomocą standardowych narzędzi do dekompresji, takich jak WinZip lub WinRAR.

Valvesoftware zawiera szczegółowe informacje o [formacie pliku VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format), do których można się odnieść z perspektywy programisty.

## Jak zainstalować pliki VPK?

Pliki VPK można zainstalować z narzędzia wiersza poleceń VPK.exe. W systemie operacyjnym Windows pliki można umieszczać w pliku vpk.exe, który zwraca plik \*.vpk zawierający wszystkie spakowane pliki. Alternatywnie, narzędzia wiersza poleceń można użyć w następujący sposób.

### Utwórz VPK i dodaj pliki

```
vpk <dirname>
```

### Wypakuj pliki VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Przeglądarka VPK

* [Przeglądarka VRF VPK](https://github.com/SteamDatabase/ValveResourceFormat)

## Bibliografia

* [Format pliku VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Pliki VPK](https://developer.valvesoftware.com/wiki/VPK)

