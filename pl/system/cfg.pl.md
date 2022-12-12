{
  "date" : "2021-06-29",
  "keywords" :["CFG", "rozszerzenie", "plik", "format", "system", "konfiguracja", "ustawienia", "programy", "komputer", "aplikacja"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Format Pliku",
  "description":"Poznaj format plików CFG i interfejsy API, które mogą tworzyć i otwierać pliki CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik CFG? ##

Plik z rozszerzeniem .cfg jest rodzajem pliku „ustawień”. Jest to powszechnie używany typ pliku i służy do przechowywania informacji dotyczących konfiguracji i ustawień programów komputerowych. Większość typów plików CFG jest przechowywana w formacie tekstowym i nie należy ich otwierać ręcznie, zamiast tego należy je otwierać za pomocą edytora tekstu. Istnieją jednak różne typy plików CFG, które różnią się formatem, w jakim przechowywane są informacje. Funkcje oferowane przez pliki CFG różnią się w zależności od aplikacji. Niektóre aplikacje komputerowe umożliwiają użytkownikom modyfikowanie lub rozwijanie składni plików konfiguracyjnych za pomocą ingerencji graficznych, podczas gdy inne pozwalają jedynie na modyfikację za pomocą edytora tekstu. Po zmodyfikowaniu tych plików użytkownicy mogą nakazać aplikacji ponowne odczytanie tych plików i zastosowanie modyfikacji w systemie.


## Format pliku CFG ##

Pliki CFG są obsługiwane przez różne systemy operacyjne, takie jak systemy operacyjne Unix i Unix-like, MS-DOS, macOS, Microsoft Windows i IBM OS/2. Format, w jakim te pliki są przechowywane i używane w każdym z tych systemów operacyjnych, jest różny. Większość systemów używa i przechowuje te pliki w czytelnym dla człowieka i edytowalnym formacie zwykłego tekstu, podczas gdy inne przechowują w nim bardziej złożony format, w zależności od wykorzystania plików i wymagań systemu operacyjnego.

W systemach operacyjnych Unix i Unix-like większość plików CFG używa kilku różnych stylów formatowania plików CFG, jednak najbardziej powszechnym formatem jest łatwy do odczytania format zwykłego tekstu, a prawie wszystkie formaty umożliwiają dodawanie i edytowanie komentarzy. Najpopularniejsze rozszerzenia plików CFG w tych systemach operacyjnych to CNF, CONF, CF i INI.

W systemie operacyjnym MS-DOS początkowo istniał tylko jeden format pliku konfiguracyjnego, a mianowicie zwykły tekst, jednak MS-DOS 6 przyniósł ze sobą wprowadzenie formatu pliku konfiguracyjnego INI.

macOS używa standardowego pliku konfiguracyjnego formatu listy właściwości.

W systemie Microsoft Windows pliki konfiguracyjne w stylu zwykłego tekstu INI były ważnym źródłem przechowywania i edytowania informacji, jednak w 1993 r. Wprowadzono nowy system baz danych, co doprowadziło do zmniejszenia wykorzystania plików konfiguracyjnych w systemie Microsoft Windows po 1993 r.


## Przykład CFG ##

Przykładowy plik CFG można zobaczyć poniżej:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
