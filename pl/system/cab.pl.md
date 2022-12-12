{
  "date" : "2021-06-29",
  "keywords" :["CAB", "rozszerzenie", "plik", "format", "system", "Plik szafy systemu Windows", "Microsoft", "Instalator", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Plik szafki Windows",
  "description":"Poznaj format pliku CAB i interfejsy API, które mogą tworzyć i otwierać pliki CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik CAB? ##

Plik z rozszerzeniem .cab należy do pliku szafki systemu Windows, który należy do kategorii plików systemowych. Jest to plik zapisany w formacie pliku archiwum w wersjach systemu Microsoft Windows obsługujących algorytmy kompresji danych, takich jak [LZX](/pl/compression/lzx/), Quantum i [ZIP](/pl/compression/zip/ ). Plik jest niezbędny, gdy użytkownik lub programista chce przechowywać i udostępniać dane i pliki instalacyjne oprogramowania. Funkcje bezstratnej kompresji danych i certyfikacja cyfrowa zawarte w tych plikach czynią ten plik idealnym do przechowywania i udostępniania takich plików. Obsługuje różne instalatory Microsoft, takie jak Device Installer, SetUp API i AdvPak.

## Krótka historia ##

Plik CAB to plik służący do kompresji danych opracowany przez firmę Microsoft. Początkowo nosił nazwę „Diament”, ale potem stał się popularnie znany jako plik CAB, skrót od słowa „Cabinet”

## Specyfikacja techniczna ##

Plik CAB może zwykle zawierać maksymalnie 65535 folderów, z których każdy może zawierać maksymalnie 65536 plików. Mechanizm przechowywania plików CAB oszczędza czas i miejsce, ponieważ zapisuje każdy folder jako skompresowany blok zamiast kompresowania i przechowywania każdego pliku osobno. Puste foldery nie mogą być przechowywane w folderach archiwum CAB. Plik CAB został po raz pierwszy opracowany przez firmę Microsoft i jest używany w różnych instalatorach, takich jak InstallShield, w nieco innym formacie. Pliki CAB są często łączone z samorozpakowującymi się programami. Pliki Microsoft CAB są łatwo rozpoznawalne dzięki unikalnemu znacznikowi, który pomaga w identyfikacji formatu. Unikalnym znacznikiem dla wszystkich plików Microsoft CAB jest czterowyrazowy prefiks MSCF. Widząc ten kod, użytkownik może łatwo odróżnić plik Microsoft CAB od innych plików i odpowiednio go użyć w kompresorach lub wersjach. Pliki można skompresować z większą ilością danych instalacyjnych oprogramowania lub obecne dane można zdekompresować za pomocą odpowiedniego oprogramowania.


## Przykład CAB ##

Poniższy przykład ilustruje relacje między plikami i folderami w strukturze plików CAB:

{{< figure src="../cab.png" alt="Format pliku CAB" >}}

## Odniesienie ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
