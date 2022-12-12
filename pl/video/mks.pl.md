{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku MKS",
  "keywords" :[ "mks", "matroska wideo", "format mkv", "plik", "format", "wideo"],
  "description":"Poznaj format pliku MKS dla napisów tworzonych tylko przez Matroskę i API, które mogą tworzyć i otwierać pliki MKS.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Czym jest plik MKS?

Pliki MKS są ogólnie znane jako pliki Matroska zawierające tylko napisy. Chociaż Matroska jest ogólnym kontenerem plików, unika przechowywania informacji o określonych formatach. Ponieważ napisy są używane w niektórych kontenerach audio lub wideo, Matroska zwraca uwagę na przechowywanie niektórych popularnych formatów napisów. Pomaga Matrosce zachować spójność tempa wzrostu. Musisz postępować zgodnie z poniższymi punktami, aby zapisać napisy w Matrosce:

- „.mks”. rozszerzenie będzie używane przez plik Matroska (zawierający tylko napisy).
- **CodecPrivate** jest używany do przechowywania wszystkich informacji związanych z kodekami, które są globalne dla całego strumienia.
— Usuń sygnatury czasowe rozpoczęcia i zatrzymania, które są używane w natywnym formacie pamięci masowej z sygnaturami czasowymi. Zamiast tego użyj sygnatury czasowej bloków i czasu trwania.
- Możesz użyć wszystkiego, co ma przezroczystą warstwę, w tym wideo.

## Popularne formaty napisów

Oto kilka krótkich uwag na temat bardziej popularnych formatów napisów przechowywanych w Matrosce:

### Napisy do obrazów
Format napisów VobSub jest pierwszym formatem napisów graficznych, który można zaimportować do Matroski. Ten format jest generowany przez eksport napisów z płyty DVD. Ścieżki powinny być rozdzielone podczas przechowywania w Matrosce, jeśli VobSub składa się z zestawu wielu strumieni.

### Napisy SRT
SRT jest najprostszym i podstawowym ze wszystkich formatów napisów. Składa się z czterech części podanych poniżej:
 



1. Numer wskazujący kolejność napisów.
2. Czas pojawiania się i znikania napisów na ekranie.
3. Same napisy.
4. Pusta linia wskazująca początek następnego napisu.
 



### Napisy SSA/ASS
Sub Station Alpha (SSA) to format pliku używany przez popularny edytor napisów SubStation Alpha. Napisy SSA są szeroko stosowane przez fanów. Posiada możliwość wyświetlania nowoczesnych funkcji np. karaoke, pozycjonowania, stylizacji itp.
 



### Napisy WebVTT
Konsorcjum World Wide Web (W3C) opracowało WebVTT, w skrócie „Web Video Text Tracks Format”. Ten format jest używany do oznaczania zewnętrznych zasobów ścieżki tekstowej w połączeniu z elementem HTML.

### Napisy graficzne prezentacji HDMV
Format napisów graficznych prezentacji HDMV (HDMV PGS) to seria map bitowych iw ogóle nie możemy tego nazwać tekstem. Innymi słowy, można powiedzieć, że jest to po prostu zsynchronizowana sekwencja obrazów graficznych. Aby wyodrębnić informacje, konieczna jest konwersja PGS na SRT.

### Napisy tekstowe HDMV
Tekst HDMV jest znany jako tekstowy format napisów używany na płytach Blu-ray. Matroska zezwala tylko na zestaw znaków UTF-8, gdy przechowuje napisy TextST.

### Cyfrowe napisy do transmisji wideo (DVB).
Format napisów DVB został wprowadzony w celu regulowania transmisji i wyświetlania napisów w kilku językach w sygnałach telewizyjnych. Typowy format napisów pozwoliłby również każdemu widzowi oglądać transmisje DVB z napisami, bez względu na to, jaki jest producent systemów transmisyjnych.


## Bibliografia ##

- [Matroska Napisy](https://www.matroska.org/technical/subtitles.html)

