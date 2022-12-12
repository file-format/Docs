{
  "date" : "2019-10-11",
  "keywords" :[ "plik gbr", "format pliku gbr", "co to jest plik gbr", "plik", "przykład gbr", "rozszerzenie pliku gbr", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku GBR - Format pliku Gerber dla PCB",
  "description":"Poznaj format pliku GBR i interfejsy API, które mogą tworzyć i otwierać pliki GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik GBR?

Plik z rozszerzeniem .gbr to format pliku obrazu Gerber do wymiany transferu danych projektu płytki drukowanej (PCB). Został opracowany przez Ucamco. Dane projektowe PCB są głównym elementem wymaganym przez przemysł wytwórczy do obsługi. Plik GRB zawiera dane PCB, takie jak warstwy miedzi, maska lutownicza, legenda oraz dane wiercenia i trasy. Może być używany do przesyłania danych, takich jak charakterystyka produkcji PCB, w tym grubość lub wykończenie, w znormalizowanym formacie. Wszystkie systemy projektowania PCB generują pliki Gerber, które mogą być obsługiwane przez systemy wytwarzania PCB. Pliki GBR stały się de facto standardem przesyłania danych projektowych płytek drukowanych (PCB). Firma Ucamco udostępniła [darmową przeglądarkę online](https://gerber-viewer.ucamco.com/) do otwierania i przeglądania plików w formatach GBR.

## Format pliku GBR

GBR to czytelny dla człowieka format UTF-8, który składa się z zaledwie 27 poleceń. Dzięki tej krótkiej liście poleceń i zwartości GBR jest łatwy do debugowania. Gerber w swej istocie jest otwartym formatem wektorowym dla binarnych obrazów 2D. Meta-informacje są przesyłane wraz z obrazami za pośrednictwem atrybutów. Pojedynczy plik GRB określa pojedynczy obraz i nie wymaga żadnych towarzyszących plików ani parametrów zewnętrznych do interpretacji. Jeden obraz wymaga tylko jednego pliku. Używa 7-bitowych znaków ASCII dla wszystkich poleceń i nazw zdefiniowanych w specyfikacji, które można wydrukować. To w pełni obejmuje pełne generowanie obrazu.

### Przykładowy plik GBR

Poniżej przedstawiono przykładowy plik Gerber, który tworzy okrąg o średnicy 1,5 mm wyśrodkowany na początku układu współrzędnych. W każdej linii jest jedno polecenie.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Bibliografia

* [Format Gerber](https://www.ucamco.com/en/gerber)

