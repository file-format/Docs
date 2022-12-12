{
  "date" : "2022-04-01",
  "keywords" :[ "plik nkit", "format pliku nkit", "co to jest plik nkit", "plik", "przykład nkit", "rozszerzenie pliku nkit", "rozszerzenie", "format", "stopka nkit", "plik format nkita"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Dowiedz się o formacie pliku NKIT i interfejsach API, które mogą tworzyć i otwierać pliki NKIT.",
  "title" :"NKIT - Format pliku obrazu dysku",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Czym jest plik NKIT?

Plik NKIT to obraz dysku danych wyodrębnionych z gier NintendoWii i GameCube. NKIT jest przeznaczony dla formatu Nintendo Toolkit. Wynikowy plik kompresji [ISO](/pl/compression/iso/) wykorzystuje główne dane tych gier do uruchamiania z programami emulującymi, takimi jak Dolphin, Swiss i Nintendont. NKit jest dostępny w formatach surowych (iso) i skompresowanych (gcz), które zostały zaprojektowane z myślą o łatwości odtwarzania i rozmiarze.

## Format pliku NKIT

Format pliku NKit jest formatem bezstratnym i służy do zmniejszania i przywracania obrazów Nintendo Wii i GameCube. Formaty są dostępne w formatach plików ISO i GCZ dla każdej gry GameCube i Wii.

|System |Format |Obsługiwany sprzęt |Obsługiwany delfin |Odtwarzanie 1:1 |Notatki|
---|---|---|---|---|---|
|GameCube| nkit.iso| Tak |Tak| Tak |Tak samo jak skompresowane iso GameCube|
|GameCube| nkit.gcz| Nie| Tak| Tak |GCZ to własny format kompresji z możliwością wyszukiwania bloków | firmy Dolphin
|Wii| nkit.iso| Nie Tak| Tak| Format RVT-H odtwarzalny tylko w Dolphin|
|Wii| nkit.gcz| Nie Tak| Tak| RVT-H w GCZ grywalny tylko w Dolphin|

### Nagłówek NKIT

Nagłówek formatu pliku NKIT jest następujący.

|Odsunięcie |Długość |Nazwa|
---|---|---|
|0x200 |0x4 |Nagłówek NKit „NKIT”|
|0x204 |0x4 |wersja NKit „v01”|
|0x208 |0x4 |Oryginał obrazu źródłowego CRC32|
|0x20C |0x4 |NKit CRC - sprawia, że plik NKit CRC32 jest równy CRC źródłowemu w 0x208 (w 0x4 w GCZ)|
|0x210 |0x4 |Długość obrazu źródłowego|
|0x214 |0x4 |Wymuszony identyfikator śmieci (gdy identyfikator dysku jest inny — rzadko — tylko GameCube)|
|0x218 |0x4 |Wii Zaktualizuj CRC32 partycji, jeśli została usunięta podczas konwersji|

## Bibliografia ##

* [Format pliku NKIT — według gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

