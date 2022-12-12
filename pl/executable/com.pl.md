{
  "date" : "2021-06-29",
  "keywords" :["plik com", "co to jest plik com", "plik", "przykład com", "rozszerzenie pliku com", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku COM i interfejsy API, które mogą tworzyć i otwierać pliki COM.",
  "title" :"COM - format pliku poleceń DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik COM?
Pliki COM są po prostu używane do wykonywania zestawu poleceń lub instrukcji. Plik COM składa się z programu wykonywalnego, który można uruchomić z systemu Windows lub MS-DOS. Podobnie jak plik EXE, plik COM jest również zapisywany w formacie binarnym, ale różni się od pliku EXE, ponieważ nie ma nagłówka ani metadanych, a także ma maksymalny rozmiar około 64 KB. Gdy plik COM jest uruchamiany po raz pierwszy w systemie 32-bitowym, pojawia się monit o zainstalowanie składnika NT Virtual DOS Machine (NTVDM). Plik COM można uruchomić w 64-bitowej wersji systemu Microsoft Windows z maszyną wirtualną obsługującą środowisko MS-DOS.

## Format pliku COM
Format pliku COM to binarny format pliku wykonywalnego używany w systemie Microsoft Windows lub MS-DOS. Jego struktura składa się tylko z zestawu instrukcji; nie ma nagłówka i nie zawiera standardowych metadanych. Przechowuje wszystkie swoje dane i kod tylko w jednym segmencie, a jego plik binarny ma maksymalny rozmiar 64 KB. Ten format pliku nie zmienia lokalizacji przy próbie ponownego uruchomienia. Tak więc system operacyjny ładuje go pod wstępnie ustawionym adresem. Ponadto możliwe jest wykonanie pliku COM w obu systemach operacyjnych w postaci **fat binarnego**. Nie ma żadnej faktycznej kompatybilności na poziomie instrukcji. Instrukcje w punkcie wejścia są wybierane tak, aby miały taką samą funkcjonalność, ale różne w obu systemach operacyjnych, i powodują, że uruchomiony program przeskakuje do sekcji używanego systemu operacyjnego. Zasadniczo są to dwa różne programy z tą samą procedurą w jednym pliku, poprzedzone kodem wybierającym ten, którego należy użyć.
### Przykład pliku COM
Podczas wykonywania pliku COM instrukcje są odczytywane od pierwszego bajtu i są wykonywane kolejno, aż do znalezienia ostatniej instrukcji. Oto przykład kodu ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Bibliografia

* [Plik COM - autorstwa Wikipewdia] (https://en.wikipedia.org/wiki/COM_file)

