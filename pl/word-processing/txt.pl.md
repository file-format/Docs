{
  "date" : "2019-10-11",
  "keywords" :["plik txt", "format pliku txt", "co to jest plik txt", "plik", "przykład txt", "rozszerzenie pliku txt", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - plik dokumentu tekstowego",
  "description":"Poznaj format pliku TXT i interfejsy API, które mogą tworzyć i otwierać pliki TXT.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TXT?

Plik z rozszerzeniem .TXT reprezentuje dokument tekstowy zawierający zwykły tekst w postaci linii. Akapity w dokumencie tekstowym są rozpoznawane przez znak powrotu karetki i służą do lepszego uporządkowania zawartości pliku. Standardowy dokument tekstowy można otworzyć w dowolnym edytorze tekstu lub edytorze tekstów w różnych systemach operacyjnych. Cały tekst zawarty w takim pliku jest w formacie czytelnym dla człowieka i reprezentowany przez sekwencję znaków.

Pliki tekstowe mogą przechowywać duże ilości danych, ponieważ nie ma ograniczeń co do rozmiaru zawartości. Jednak edytory tekstu otwierające tak duże pliki muszą być sprytne, aby je załadować i wyświetlić. Prawie wszystkie systemy operacyjne są wyposażone w edytory tekstu, które umożliwiają tworzenie i edytowanie plików tekstowych. Na przykład system operacyjny Windows jest dostarczany w tym celu z Notatnikiem i Wordpadem. Podobnie, MacOS jest wyposażony w TextEdit do tworzenia i edytowania dokumentów tekstowych. Istnieją jednak inne bezpłatne edytory tekstu dostępne w Internecie, które zapewniają możliwość pracy z dokumentami tekstowymi, takimi jak Notepad ++, który jest znacznie bardziej zaawansowany pod względem funkcjonalności.

## Specyfikacje formatu pliku ##

Format pliku tekstowego nie ma żadnych specjalnych specyfikacji formatu pliku. Pliki tekstowe mają typ MIME „text/plain” i mają niewielkie lub żadne formatowanie. Dzięki temu edytory tekstu mogą otwierać takie pliki bez żadnych innych wymagań. Domyślnym zestawem znaków plików tekstowych jest ASCII, który jest używany do tworzenia i wyświetlania zawartości plików tekstowych. Znaki są kodowane przy użyciu zestawu znaków ASCII, ale ogranicza to użycie znaków, takich jak znak funta, dolara i euro, których nie można przedstawić przy użyciu zestawu znaków ASCII. W ten sposób pliki tekstowe można również zapisywać w formacie Unicode, przy czym najczęściej używany jest UTF-8.

### Format pliku tekstowego systemu Windows ###

Pliki tekstowe w systemie operacyjnym Windows składają się z kilku wierszy, z których każdy składa się z sekwencji znaków. Każda linia domyślna użytkownika jest zdefiniowana przez kombinację dwóch znaków, tj. powrotu karetki (CR) i nowego wiersza (LF). Pliki tekstowe systemu Windows mogą być w kodowaniu ANSI, OEM, Unicode lub UTF-8. Kodowanie UTF-16 pomaga zapisywać informacje w pliku tekstowym, który wymaga dwóch bajtów do reprezentacji. Takie pliki zwykle zaczynają się od znacznika kolejności bajtów (BOM), który informuje o endianizmie zawartości pliku. Należy zauważyć, że inne aplikacje w systemie operacyjnym Windows mogą przechowywać informacje w formacie pliku tekstowego, ale z różnymi rozszerzeniami plików, aby reprezentować tekst specyficzny dla aplikacji. Na przykład języki programowania zwykle zapisują kod w pliku tekstowym, ale z własnymi rozszerzeniami.

### Uniksowy format plików tekstowych ###

Wszystkie takie systemy dopracowują plik tekstowy jako plik, którego znaki są zorganizowane w zero lub więcej wierszy. Każda linia jest sekwencją zera lub więcej znaków innych niż znak nowej linii i kończącego znaku nowej linii, zwykle LF.

## Bibliografia ##

* [Format pliku TXT](https://en.wikipedia.org/wiki/Text_file)

