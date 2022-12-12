{
  "date" : "2021-07-12",
  "keywords" :["plik cmd", "co to jest plik cmd", "plik", "przykład cmd", "rozszerzenie pliku cmd", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku CMD i interfejsy API, które mogą tworzyć i otwierać pliki CMD.",
  "title" :"CMD — format pliku poleceń systemu Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Czym jest plik CMD?
Plik CMD składa się ze skryptu zawierającego jedno lub wiele poleceń w postaci zwykłego tekstu, które są uruchamiane w celu wykonania różnych zadań. Jest podobny do pliku [BAT](/pl/plik wykonywalny/bat/), który jest również zwykle używany do przechowywania partii poleceń wykonywalnych. Pliki CMD są szeroko stosowane w systemie operacyjnym Microsoft Windows. Pliki te zostały wprowadzone prawie w latach 90-tych, ale nadal są używane w najnowszym systemie operacyjnym Windows. Pliki te są zwykle zapisywane w celu wykonania więcej niż jednego polecenia w sekwencji.

## Format pliku CMD
CMD to format pliku używany przez programy wykonywalne w stylu CP/M. Jest ogólnie porównywalny z [COM](/pl/executable/com/) w CP/M-80 i [EXE](/pl/executable/exe/) w DOS. Plik CMD zawiera od 1 do 8 grup kodu lub danych oraz 128-bajtowy nagłówek. Każda grupa może mieć rozmiar do 1 MB. Pliki CMD mogą również zawierać informacje o relokacji i rozszerzenia systemu rezydentnego (RSX) w późniejszych wersjach. CMD jest nowicjuszem w porównaniu z plikiem [BAT](/pl/executable/bat/); używany w systemie MS-DOS przed wydaniem systemu Windows w systemie MS-DOS. Chociaż dzisiaj nadal można zapisywać pliki z rozszerzeniem .bat, wiele osób używa rozszerzenia .cmd do zapisywania swoich skryptów wykonywalnych.

### Specyfikacja formatu CMD

Początek nagłówka zawiera listę grup występujących w pliku wraz z ich typami. Każdy typ może być użyty maksymalnie jeden raz. Te typy to:

- Kod
- Dane
- Ekstra
- Stos
- Użytkownik 1
- Użytkownik 2
- Użytkownik 3
- Użytkownik 4
- Wspólny kod

Podobnie jak przedrostek segmentu programu w systemie DOS, pierwsze 256 bajtów grupy danych to zero. Zostaną one wypełnione przez CP/M-86 ze stroną zerową. Jeśli nie ma grupy danych, zamiast niej zostanie użytych pierwszych 256 bajtów grupy kodu.
## Przykład pliku CMD
Poniżej przedstawiono przykład skryptu CMD do wyświetlania informacji systemowych.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Bibliografia

* [Jak napisać skrypt CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [Plik CMD (CP/M) - z Wikipedii](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

