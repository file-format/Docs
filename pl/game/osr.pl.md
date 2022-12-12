{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku OSR i interfejsy API, które mogą tworzyć i otwierać pliki OSR.",
  "title" :"Plik OSR - osu! Format pliku powtórki",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Czym jest plik OSR?

Plik OSR to plik powtórki gry utworzony przez [osu! gra](https://osu.ppy.sh/home). Osu! to gra rytmiczna, w której użytkownicy dopasowują kliknięcia myszką do muzyki. Utwór odtwarzany przez użytkownika, trafienia i chybienia, godzina i data odtworzenia utworu oraz ogólny ranking są zapisywane w pliku OSR. Ten plik OSR można następnie udostępnić innym osobom w celu powtórki. Plik OSR wymaga, aby plik beatmap znajdował się w folderze „Songs”.

**Typ MIME formatu pliku OSR:** x-osu-replay

## Format pliku OSR

Pliki OSR są zapisywane jako pliki binarne z polami danych o stałej i zmiennej długości.

|Typ danych| Formatuj|
---|---|
|Bajt |Tryb gry powtórki (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Liczba całkowita |Wersja gry w momencie utworzenia powtórki (np. 20131216)|
|String |osu! hash MD5 mapy beatowej|
|Ciąg| Nazwa gracza|
|Ciąg| osu! hash MD5 powtórki (zawiera pewne właściwości powtórki)|
|Krótki| Liczba 300s|
|Krótki| Liczba 100 w standardzie, 150 w Taiko, 100 w CTB, 100 w manii|
|Krótki| Liczba 50s w standardzie, małe owoce w CTB, 50s w mania|
|Krótki| Liczba Gekis w standardzie, Max 300s w mania|
|Krótki| Liczba Katusów w standardzie, 200s w manii|
|Krótki| Liczba chybień|
|Całkowita| Całkowity wynik wyświetlany w raporcie wyników|
|Krótki| Najlepsza kombinacja wyświetlana w raporcie wyników|
|Bajt| Perfekcyjna/pełna kombinacja (1 = brak chybień, brak przerw w suwakach i brak przedwcześnie zakończonych sliderów)|
|Całkowita| Użyte mody. Zobacz poniżej listę wartości modów.|
|Ciąg| Wykres słupkowy życia: pary oddzielone przecinkami u/v, gdzie u to czas w milisekundach do początku utworu, a v to wartość zmiennoprzecinkowa od 0 do 1, która reprezentuje ilość życia, jaką masz w danym momencie (0 = pasek życia to pusty, 1= pasek życia jest pełny)|
|Długi| Znacznik czasu (tyknięcia systemu Windows)|
|Całkowita| Długość w bajtach skompresowanych danych powtórki|
|Bajt |Tablica Skompresowane dane powtórki|
|Długi| Identyfikator wyniku online|
|Podwójne| Dodatkowe informacje o modzie. Występuje tylko, jeśli włączona jest praktyka strzelecka.|

## Bibliografia

* [OSU! Gra rytmiczna](https://osu.ppy.sh/home)
* [Format pliku OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

