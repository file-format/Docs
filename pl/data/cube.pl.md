{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Plik CUBE - Plik kostki Gaussa - Co to jest plik .cube i jak go otworzyć?",
  "description" : "Dowiedz się o pliku kostki Gaussa i o tym, jak go otworzyć.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-pl-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Co to jest plik CUBE?

Format pliku CUBE, znany również jako plik Gaussa Cube (.cube), jest używany w chemii obliczeniowej do przechowywania danych molekularnych, w szczególności informacji o gęstości elektronów wynikających z obliczeń chemii kwantowej. Ten format jest powszechnie kojarzony z **pakietem oprogramowania Gaussa**, który jest szeroko stosowany do wykonywania obliczeń struktury elektronicznej od początku.

Pliki Gaussa Cube przechowują dane trójwymiarowe, zazwyczaj reprezentujące gęstość elektronów lub inne właściwości cząsteczek, uzyskane w wyniku obliczeń chemii kwantowej. Plik zawiera sekcję nagłówka z metadanymi (takimi jak pochodzenie, liczba punktów danych wzdłuż każdej osi i odstępy), po której następuje siatka wartości liczbowych reprezentujących interesującą właściwość (np. gęstość elektronów) w każdym punkcie siatki w przestrzeni.

Plik kostki Gaussa (.cube) to zwykły plik tekstowy o określonej strukturze. Nagłówek zawiera informacje o układzie molekularnym i siatce danych, a wartości danych są ułożone w trójwymiarowym formacie siatki. Pliki kostki Gaussa są często używane do wizualizacji właściwości molekularnych za pomocą oprogramowania do wizualizacji molekularnej. Programy takie jak **VMD (Visual Molecular Dynamics)** lub **PyMOL** mogą odczytywać pliki kostki Gaussa w celu wyświetlenia powierzchni molekularnych, gęstości elektronów lub innych obliczonych właściwości.

## Uproszczony przykład pliku kostki Gaussa:

```
Przykład pliku Cube
Wygenerowane przez Gaussa
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,100000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (wartości danych dotyczące gęstości elektronów w każdym punkcie siatki)
```

## O Gaussa

Gaussian to pakiet aplikacji do chemii kwantowej i chemii obliczeniowej. Gaussa skupia się przede wszystkim na metodach chemii kwantowej ab initio, które są bardzo dokładnymi, ale wymagającymi obliczeniowo podejściami do badania struktury elektronowej cząsteczek. Oprogramowanie jest szeroko stosowane w środowiskach badawczych i akademickich do różnych zastosowań, w tym do przewidywania właściwości molekularnych, badania mechanizmów reakcji i badania struktur molekularnych.

## O NWChem

NWChem to oprogramowanie do chemii obliczeniowej typu open source przeznaczone do wysokowydajnych symulacji chemii kwantowej. Wykorzystuje metody ab initio, takie jak teoria Hartree-Focka i funkcjonału gęstości, obsługuje obliczenia równoległe w celu wydajnych obliczeń na klastrach i znajduje zastosowanie w różnych dziedzinach nauki, w tym chemii obliczeniowej, biochemii i materiałoznawstwie. NWChem jest znany ze swojej wszechstronności, umożliwiającej badaczom badanie różnych układów chemicznych, a jego charakter typu open source zachęca społeczność do wnoszenia wkładu i dostosowywania.

## O VMD

VMD, czyli Visual Molecular Dynamics, to potężny i szeroko stosowany program do wizualizacji molekularnej, służący do wyświetlania, analizowania i animowania trajektorii dynamiki molekularnej (MD), a także statycznych struktur molekularnych. Jest szczególnie popularny w dziedzinach chemii obliczeniowej, biologii molekularnej i bioinformatyki strukturalnej. VMD specjalizuje się w wizualizacji struktur molekularnych, zapewniając wysokiej jakości wizualizacje 3D cząsteczek i kompleksów molekularnych. Obsługuje różne formaty plików molekularnych.

## O PyMOL-u

PyMOL to system wizualizacji molekularnej i narzędzie programowe służące do trójwymiarowej wizualizacji struktur molekularnych. Jest szczególnie popularny w dziedzinach biologii strukturalnej, bioinformatyki i chemii obliczeniowej. PyMOL zapewnia wysokiej jakości wizualizacje 3D struktur molekularnych, umożliwiając użytkownikom wizualizację i badanie kształtów, powierzchni i interakcji makrocząsteczek biologicznych.

## Jak otworzyć plik CUBE?

Plik CUBE można otworzyć i odwoływać się do niego za pomocą następujących programów.

- **NWChem** (bezpłatny) dla (Windows, MAC, Linux)

## Bibliografia
* [Format pliku kostki Gaussa](https://paulbourke.net/dataformats/cube/)
