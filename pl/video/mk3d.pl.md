{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku MK3D",
  "keywords" :[ "mk3d", "matroska wideo", "format mkv", "stereoskopowy 3d", "StereoMode", "wideo", "plik", "format" ],
  "description":"Dowiedz się o formacie plików MK3D dla stereoskopowych filmów 3D stworzonych przez Matroska i API, które mogą tworzyć i otwierać pliki MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Czym jest plik MK3D? ##

Pliki MK3D należą do rodziny formatów wideo Matroska. Te pliki to właściwie **stereoskopowe filmy 3D** utworzone przy użyciu formatu Matroska 3D. Kontener pliku MKV używa wartości pola StereoMode do zdefiniowania typu stereoskopowego materiału wideo 3D. Dostępna jest również wartość StereoMode do wyświetlania starych stereofonicznych filmów 3D poprzez oddzielenie kolorów cyjan i czerwieni (AnaGlyph)

## Szczegóły techniczne ##
Filmy 3D można kompresować na dwa sposoby:

- Oddzielna ścieżka dla każdego oka.
- Połącz każde śledzenie wzroku w jedną ścieżkę.

Kontener plików MKV obsługuje oba te elementy.

W przypadku filmów jednościeżkowych, które są łatwiejsze z materiałem 3D w środku, musisz ustawić pole **StereoMode**, które decyduje, czy samoloty są montowane na ścieżce mono, czy też lewej i prawej. Możesz użyć jednej z następujących wartości pola StereoMode:

|Wartość | Opis |
|---|---|
|0| mono|
|1| obok siebie (lewe oko jest pierwsze)|
|2| góra-dół (prawe oko jest pierwsze)|
|3| góra-dół (lewe oko jest pierwsze)|
|4| szachownica (po prawej jest pierwsza)|
|5| szachownica (lewa jest pierwsza)|
|6| wiersz przeplatany (prawy jest pierwszy)|
|7| wiersz przeplatany (lewy jest pierwszy)|
|8| kolumna przeplatana (prawa jest pierwsza)|
|9| kolumna przeplatana (lewa jest pierwsza)|
|10| anaglif (cyjan/czerwony)|
|11| obok siebie (prawe oko jest pierwsze)|
|12| anaglif (zielony/purpurowy)|
|13| oba oczy splecione w jednym Bloku (lewe oko jest pierwsze) (tryb sekwencyjny pól)|
|14| oba oczy splecione w jednym bloku (prawe oko jest pierwsze) (tryb sekwencyjny pól)|

W przypadku wielu ścieżek kontener MKV musi oddzielnie decydować o funkcjonalności każdej ścieżki. **TrackOperation** z **TrackCombinePlanes** są używane do wykonania zadania.


## Bibliografia ##

- [Uwagi dotyczące specyfikacji Matroska](https://www.matroska.org/technical/notes.html)
- [Obsługa kontenerów plików MKV dla wideo stereo 3D i plików MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- akta/)

