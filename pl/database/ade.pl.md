{
  "date" : "2021-08-29",
  "keywords" :["ade", "rozszerzenie", "plik", "format pliku", "Typ pliku bazy danych", "Format pliku bazy danych", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format pliku ADE i interfejsy API, które mogą tworzyć i otwierać pliki ADE.",
  "title" :"ADE - plik rozszerzenia projektu dostępu",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Czym jest plik ADE?

Plik z rozszerzeniem .ade to plik projektu Microsoft Access, który zawiera skompilowane dane wyjściowe informacji zawartych w pliku projektu Microsoft Access ADP. Informacje w pliku projektu programu Access, inne niż Visual Basic for Applications (VBA), są dostępne w postaci skompilowanej w plikach ADE. Dane są przechowywane w tych plikach w skompresowanym formacie, aby zmniejszyć rozmiar pliku i poprawić wydajność programu Access. Ponieważ ADE jest skompilowanym wynikiem pliku projektu programu Access, każdy kod źródłowy VBA, który jest częścią projektu, pozostaje chroniony, ponieważ nie pozwala, aby był częścią danych wyjściowych. Pliki ADE można otwierać w programie Microsoft Access 365.

## Format pliku ADE — więcej informacji

ADE to skompilowane pliki bazy danych Access, które są przechowywane na dysku jako pliki binarne. Wewnętrzna struktura plików tych plików nie jest znana.

Pliki ADE mogą powodować problemy z otwieraniem w zależności od wersji programu Microsoft Access, która została użyta do utworzenia tych plików. Bazy danych programu Access korzystające z 64-bitowej wersji programu Microsoft Access 2010 i skompilowane jako pliki MDE, [ACCDE](/pl/database/accde/) lub ADE muszą zostać ponownie skompilowane w dodatku Service Pack 1 (SP1) dla programu Microsoft Access 2021, aby działać poprawnie z programem Access 2010 SP1. Ten problem występuje, ponieważ dodatek SP1 dla programu Access 2010 używa nowszej wersji pliku VBE7.dll (wersja 7.00.1619).

## Bibliografia

* [Problem z plikami Access ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Jakich formatów plików programu Access użyć](https://support.microsoft.com/en-us/office/ Which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

