{
  "date" : "2021-06-30",
  "keywords" :[ "plik mst", "format pliku mst", "co to jest plik mst", "plik", "przykład mst", "rozszerzenie pliku mst", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku MST i interfejsy API, które mogą tworzyć i otwierać pliki MST.",
  "title" :"MST - Plik pakietu Instalatora Windows",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Czym jest plik MST?
Pliki z rozszerzeniem .mst służą do przekształcania zawartości pakietu MSI. Są one powszechnie używane przez administratorów systemu w celu zastosowania ustawień niestandardowych do istniejącego pliku MSI. Pliki MST są używane razem z oryginalnym pakietem MSI w ich systemach dystrybucji oprogramowania, takich jak zasady grupy. Pliki MST są zwykle używane w opracowywaniu i testowaniu oprogramowania do konfigurowania ich będących w fazie rozwoju wersji oprogramowania.

## Format pliku MST
Plik MST lub plik Transform służy do zbierania opcji instalacji programów korzystających z Instalatora systemu Microsoft Windows w pliku. Pliki te są powszechnie używane w wierszu polecenia Instalatora (MSIEXEC.EXE) lub w zasadach grupy dotyczących instalacji oprogramowania; w domenie Microsoft Active Directory. Pliki MST mogą być również używane z opakowanymi wykonywalnymi instalatorami. Ogólny przypadek polega na tym, że ktoś chce przekazać parametry wiersza poleceń do opakowanego instalatora. Aby to zrobić, potrzebujesz pliku MST, który dodaje właściwość WRAPPED_ARGUMENTS do tabeli właściwości. Tych plików nie można tworzyć ani edytować za pomocą ogólnych edytorów. W tym celu dostępne są specjalne narzędzia.

### Jak korzystać z plików MST?
Pliki MST można generować za pomocą różnych narzędzi, a Ocra jest zwykle używana do generowania plików MST. Następnie ustawienia można dostosować do potrzeb i zapisać je w określonej lokalizacji. Następnie pliki MST mogą być używane w połączeniu z plikami MSI. Jeśli chcesz przetestować te pliki; użyj następującej składni w wierszu poleceń

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Właściwość PRZEKSZTAŁCA

Możesz także użyć właściwości **TRANSFORMS** instalatora Windows, która w rzeczywistości jest listą przekształceń, które instalator stosuje podczas instalacji pakietu. Instalator wykonuje transformacje w tej samej kolejności, w jakiej są wymienione we właściwości TRANSFORM. Transformacje można określić za pomocą nazwy pliku z rozszerzeniem .mst lub pełnej ścieżki. Aby określić więcej niż jedną transformację, oddziel nazwy plików lub średniki, jak w poniższym przykładzie.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Bibliografia

* [Pliki transformacji MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [Właściwość TRANSFORMS](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


