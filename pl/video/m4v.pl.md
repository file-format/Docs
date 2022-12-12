{
  "date" : "2019-10-11",
  "keywords" :["M4V", "plik", "rozszerzenie", "format", "MPEG-4", "Zarządzanie prawami cyfrowymi", "DRM", "Apple", "wideo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"Dowiedz się o formacie plików M4V i interfejsach API, które mogą tworzyć i otwierać pliki M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## Czym jest plik M4V?

Format pliku **M4V**, opracowany przez Apple, to kontener wideo opcjonalnie chroniony za pomocą ochrony przed kopiowaniem Digital Rights Management (DRM) w celu ochrony prywatności lub kopii. Ścieżki wideo i audio są opakowane w pliki kontenerów w celu indeksowania i organizowania strumieni odtwarzania. Ponadto kontenery zapewniają również funkcję rozdziałów podobną do tych na płytach DVD. Apple używa M4V do kodowania wideo w swoim iTunes Store. Chroni nieautoryzowane kopiowanie za pomocą ochrony przed kopiowaniem FairPlay firmy Apple, umożliwiając odtwarzanie plików M4V tylko na autoryzowanych komputerach posiadających konta użyte do zakupu wideo. Jeśli jednak ochrona DRM zostanie usunięta z plików M4V, pliki te można odtwarzać w innych odtwarzaczach wideo, zmieniając rozszerzenie z .m4v na .mp4, dlatego pliki M4V są kojarzone z MPEG-4. M4V używa H.264 do wideo i **[AAC](/pl/audio/aac/)** oraz Dolby Digital do kodowania i dekodowania dźwięku.

## Struktura pliku M4V ##

Pliki M4V mają ciągłe fragmenty z 8-bajtowym nagłówkiem, 4-bajtowym rozmiarem fragmentu i 4-bajtowym typem fragmentu w każdym fragmencie. Pierwsza porcja to „ftype” i ma podtyp o przesunięciu 8. M4V zdefiniowany przez podtyp, który musi być „M4V_”. Kolejne typy chunków to predefiniowane sygnatury: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PIKT”. Iterując kawałki, aż do wykrycia nieznanego typu, tworzymy plik M4V.

Oto badanie próbki: przykładowe dane binarne pliku m4v są sprawdzane przez Hex Viewer i można zauważyć, że zaczynają się od podpisu **ftyp** (hex: 66 74 79 70) z przesunięciem 4, co definiuje QuickTime Typ pliku kontenera. Podtyp pliku to **M4V_** (szesnastkowo: 4D 34 56 20), co wskazuje na typ pliku M4V (MPEG-4). Rozmiar pierwszego bloku to 32 (hex: 00 00 00 20, big-endian, najpierw wysoki bajt), rozmiar znajduje się przy przesunięciu 0. Przy przesunięciu 32 (heks: 20) znajduje się drugi fragment, który ma rozmiar 30 322 (szesnastkowo : 00 00 76 72, big-endian, najpierw dolny bajt) i wpisz **moov** (szesnastkowo: 6D 6F 6F 76). Następna porcja znajduje się pod offsetem 32+30 322#30 354 (hex: 00 00 76 92) i ma rozmiar 8 (hex: 00 00 00 08) i typ **free** (hex: 66 72 65 65).
### Kodeki używane w M4V ###

#### Kodek wideo H.264 ####

H.264 to standard kompresji wideo, który konwertuje cyfrowe wideo do formatu, który wymaga mniej miejsca, gdy wymagana jest transmisja lub przechowywanie. M4V używa H.264 do kompresji wideo. Jego zastosowanie obejmuje DVD, telewizję, wideokonferencje i strumieniowe przesyłanie wideo przez Internet. H.264 składa się z dwóch głównych części: Encoder – który kompresuje wideo, Decoder – który dekompresuje skompresowane wideo z powrotem. Na poniższym rysunku wyróżniono procesy kodowania i dekodowania, a inne procesy są objęte standardem H.264.

##### Proces kodowania i dekodowania wideo w H.264 #####

W przypadku skompresowanego strumienia bitów H.264 koder wideo przeprowadza proces przewidywania, transformacji i kodowania. W tym samym czasie dekoder wykonuje odwrotny proces dekodowania, odwrotnej transformacji i rekonstrukcji, aby odtworzyć plik wideo. H.264 zajmuje połowę rozmiaru MPEG.

#### Kodek audio ####

Advanced Audio Coding (AAC) to kodek audio do stratnej cyfrowej kompresji dźwięku, używany w kontenerze M4V. AAC jest następcą formatu [MP3](/pl/audio/mp3/) i zapewnia lepszą jakość niż MP3 przy tej samej przepływności. Format AAC odrzuca niektóre informacje podczas procesu kompresji, co ma mniejsze znaczenie. AAC to oparty na blokach kodek o zmiennej szybkości transmisji bitów (VBR), w którym każdy blok dekoduje do 1024 próbek w dziedzinie czasu.

### Bibliografia ###

* [Wikipedia - M4V](https://en.wikipedia.org/wiki/M4V)
* [Wikipedia — MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)

