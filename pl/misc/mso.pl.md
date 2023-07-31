{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO — plik referencyjny makr pakietu Microsoft Office",
  "description":"Poznaj plik MSO i interfejsy API, które mogą tworzyć i otwierać pliki MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Czym jest plik MSSO?

Plik MSO to format pliku kontenera danych, który jest tworzony podczas wysyłania wiadomości HTML za pomocą programu Microsoft Outlook. Dzieje się tak głównie w przypadku aplikacji pakietu Microsoft Office 2000. W większości przypadków do wiadomości e-mail jest dołączony plik o nazwie **Oledata.mso**. Odbiorca wiadomości e-mail po otwarciu takiej wiadomości może poprawnie wyświetlić plik, nawet jeśli nie ma zainstalowanego tego samego oprogramowania. Pliki MSO odnoszą się do [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Format pliku Microsoft MSO

Pliki MSO są zapisywane w formacie Microsoft Compound Document File Format (MCDF), który jest również znany jako łączenie i osadzanie obiektów (OLE) lub Component Object Model (COM) w formacie pliku binarnego implementacji złożonego pliku składowania złożonego.

### Struktura formatu plików MSO

Wewnętrzna struktura formatu plików MSO jest dobrze zdefiniowana w [Struktury](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) sekcja dokumentacji MCDF. Tabela alokacji plików (FAT) zarządza alokacją sektorów i łańcuchami sektorów. Zawiera tablicę 32-bitowych numerów sektorów. Każdy indeks w tablicy reprezentuje numer sektora, podczas gdy jego wartość reprezentuje następny sektor w łańcuchu lub wartość specjalną.

## Bibliografia

* [Pamięć masowa o strukturze COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

