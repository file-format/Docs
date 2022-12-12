{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - skompilowany skrypt zasobów C++",
  "description":"Poznaj format pliku RES z przykładem RES i interfejsami API, które mogą tworzyć i otwierać pliki RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Czym jest plik RES?
Plik z sufiksem lub rozszerzeniem .res może należeć do wielu kategorii formatów plików. Tutaj omawiamy format pliku RES, który jest skompilowanym skryptem zasobów C++; plik binarny utworzony przez Microsoft Resource Compiler (rc), który zawiera dane zasobów; na podstawie zawartości pliku definicji zasobów; związane z jego nadrzędnym projektem oprogramowania. Plik .res jest zwykle ponownie formatowany do pliku obiektu zasobów w celu połączenia go z plikiem wykonywalnym aplikacji.

## Format pliku OZE
Format pliku RES należy do Microsoft Resource Compiler (rc). Kompilator zasobów to narzędzie, które kompiluje zasoby, takie jak kursory, ikony, menu i okna dialogowe używane przez aplikację. Pliki zasobów zwykle mają rozszerzenie .res; zawiera zasoby, takie jak kursory, obrazy i informacje o wersji. Plik RES może być 16- lub 32-bitowym plikiem zasobów.
## Struktura plików zasobów
Plik zasobów zawiera serię różnych wpisów zasobów. Każdy wpis zawiera nagłówek zasobu i odpowiednie dane. Nagłówek zasobu jest zwykle wyrównany do DWORD w pliku i zawiera następujące informacje:

- **DWORD** do określenia rozmiaru nagłówka zasobu
- **DWORD** do określenia rozmiaru danych zasobu
— Typ zasobu
— Nazwa zasobu
- Dodatkowe informacje o zasobach

Struktura nagłówka zasobu określa format pliku RES. Dane dla zasobu następują po nagłówku zasobu. Niektóre zasoby dodają również wzorzec nagłówka grupy specyficzny dla zasobu, aby zapewnić informacje o grupie zasobów. Poniżej przedstawiono niektóre typy wpisów zasobów i ich opis:

### Zasoby tabeli akceleratora
Tabela akceleratora to pozycja zasobu w pliku RES bez nagłówka grupy. Wzorzec **ACCELTABLEENTRY** definiuje każdy wpis w tabeli akceleratora. Plik RES może zawierać wiele tabel akceleratorów.

### Zasoby dotyczące kursorów i ikon
Chociaż system traktuje każdą ikonę i kursor jako pojedynczy plik, ale są one przechowywane w plikach RES jako grupa zasobów ikon lub grupa zasobów kursorów. Formaty plików zasobów ikon i kursorów są takie same. Nagłówek grupy zasobów następuje po wszystkich składnikach poszczególnych ikon lub grup kursorów w pliku res.

### Zasoby okna dialogowego
Okno dialogowe jest również realizowane jako wpis zasobu w pliku RES. Zawiera jeden wzorzec nagłówka okna dialogowego **DLGTEMPLATE** i jeden wzorzec **DLGITEMPLATE** dla każdego określonego elementu sterującego w oknie dialogowym. Wzorce **DLGTEMPLATEEX** i **DLGITEMTEMPLATEEX** wyjaśniają format zasobów rozszerzonego okna dialogowego.

### Zasoby czcionek
Zasób menu zawiera wzorzec **MENUHEADER**, po którym następuje jeden lub więcej wzorców **NORMALMENUITEM** lub **POPUPMENUITEM**, po jednym dla każdego elementu menu w szablonie menu. Wzorce **MENUEX_TEMPLATE_HEADER** i **MENUEX_TEMPLATE_ITEM** objaśniają format rozszerzonych zasobów menu.

### Zasoby tabeli komunikatów
Tabela komunikatów zawiera sformatowany tekst do wyświetlenia jako komunikat o błędzie lub w oknie komunikatu. Głównym wzorcem w zasobie tabeli komunikatów jest struktura **MESSAGE_RESOURCE_DATA**.

### Zasoby wersji
Głównym wzorcem w zasobie wersji jest **VS_FIXEDFILEINFO**. Dodatkowe wzorce obejmują **VarFileInfo** do przechowywania danych związanych z informacjami o języku oraz **StringFileInfo** do przechowywania niestandardowych informacji o ciągach.




## Bibliografia

* [Formaty plików zasobów](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



