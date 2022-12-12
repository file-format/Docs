{
  "date" : "2019-11-25",
  "keywords" :["plik jpeg", "format pliku jpeg", "co to jest plik jpeg", "plik", "przykład jpeg", "rozszerzenie pliku jpeg", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG — format pliku obrazu",
  "description":"Poznaj format pliku JPEG i interfejsy API, które mogą tworzyć i otwierać pliki JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## Czym jest plik JPEG? ##

JPEG to rodzaj formatu obrazu, który jest zapisywany przy użyciu metody kompresji stratnej. Obraz wyjściowy, będący wynikiem kompresji, jest kompromisem między rozmiarem pamięci a jakością obrazu. Użytkownicy mogą dostosować poziom kompresji, aby osiągnąć żądany poziom jakości, jednocześnie zmniejszając rozmiar pamięci. Jakość obrazu jest pomijalnie ograniczona, jeśli do obrazu zostanie zastosowana kompresja 10:1. Im wyższa wartość kompresji, tym większe pogorszenie jakości obrazu.

## Specyfikacje formatu pliku ##

Format plików graficznych JPEG został znormalizowany przez Joint Photographic Experts Group i stąd nazwa JPEG. Format został wybrany do przechowywania i przesyłania obrazów fotograficznych w Internecie. Prawie wszystkie systemy operacyjne mają teraz przeglądarki obsługujące wizualizację obrazów JPEG, które często są również przechowywane z rozszerzeniem JPG. Nawet przeglądarki internetowe obsługują wizualizację obrazów JPEG. Zanim przejdziemy do specyfikacji formatu plików JPEG, należy wspomnieć o całym procesie tworzenia plików JPEG.

### Kroki kompresji JPEG ###

**Transformacja:** obrazy kolorowe są przekształcane z RGB na obraz luminancji/chrominancji (Oko jest wrażliwe na luminancję, a nie na chrominancję, więc część chrominancji może utracić wiele danych, a tym samym może być mocno skompresowana.

**Próbkowanie w dół:** Próbkowanie w dół jest wykonywane dla składowej kolorowej, a nie dla składowej luminancji. Próbkowanie w dół odbywa się w stosunku 2:1 w poziomie i 1:1 w pionie (2h 1 V). W ten sposób obraz zmniejsza się, ponieważ element „y” nie jest dotykany, nie ma zauważalnej utraty jakości obrazu.

**Organizacja w grupach:** piksele każdego składnika koloru są zorganizowane w grupy 8×2 piksele zwane „jednostkami danych”, jeśli liczba wierszy lub kolumn nie jest wielokrotnością 8, dolny wiersz i kolumny po prawej stronie są powielane.

**Dyskretna transformacja kosinusowa:** Dyskretna transformata kosinusowa (DCT) jest następnie stosowana do każdej jednostki danych w celu utworzenia mapy 8×8 przekształconych komponentów. DCT wiąże się z pewną utratą informacji ze względu na ograniczoną precyzję arytmetyki komputerowej. Oznacza to, że nawet bez mapy nastąpi pewna utrata jakości obrazu, ale zazwyczaj jest ona niewielka.

**Kwantyzacja:** Każdy z 64 przekształconych składników w jednostce danych jest dzielony przez osobną liczbę zwaną „współczynnikiem kwantyzacji (QC)”, a następnie zaokrąglany do liczby całkowitej. W tym miejscu informacje są bezpowrotnie tracone, a duża kontrola jakości powoduje więcej strat. Ogólnie rzecz biorąc, większość narzędzi JPEG pozwala na użycie tabel QC zalecanych przez standard JPEG.

**Kodowanie:** 64 skwantyzowane przekształcone współczynniki (które są teraz liczbami całkowitymi) każdej jednostki danych są kodowane przy użyciu kombinacji kodowania RLE i Huffmana.

**Dodawanie nagłówka:** Ostatni krok polega na dodaniu nagłówka i wszystkich użytych parametrów JPEG oraz wypisaniu wyniku.

Dekoder JPEG wykonuje kroki w odwrotnej kolejności, aby wygenerować oryginalny obraz ze skompresowanego.

### Struktura plików ###

Obraz JPEG jest reprezentowany jako sekwencja segmentów, gdzie każdy segment zaczyna się od znacznika. Każdy znacznik zaczyna się od bajtu 0xFF, po którym następuje flaga znacznika reprezentująca typ znacznika. Ładunek, po którym następuje znacznik, różni się w zależności od typu znacznika. Typowe typy znaczników JPEG są wymienione poniżej:

|Krótka nazwa|Bajty|Ładunek|Nazwa|Komentarze
---|---|---|---|---|
|SOI|0xFF, 0xD8|brak|Początek obrazu|
|S0F0|0xFF, 0xC0|rozmiar zmienny|Początek ramki|
|S0F2|0xFF, 0xC2|rozmiar zmienny|Początek ramki|
|DHT|0xFF, 0xC4|rozmiar zmiennej|Definiuj tablice Huffmana|
|DQT|0xFF, 0xDB|rozmiar zmienny|Definiuj tabele kwantyzacji|
|DRI|0xFF, 0xDD|4 bajty|Określ interwał restartu|
|SOS|0xFF, 0xDA|rozmiar zmienny|Początek skanowania|
|RSTn|0xFF, 0xD//n//(/pl//n//#0..7)|brak|Uruchom ponownie|
|APPn|0xFF, 0xE//n//|rozmiar zmienny|Specyficzne dla aplikacji|
|COM|0xFF, 0xFE|rozmiar zmiennej|Komentarz|
|EOI|0xFF, 0xD9|brak|Koniec obrazu|

W danych zakodowanych entropijnie, po dowolnym bajcie 0xFF, koder wstawia bajt 0x00 przed następnym bajtem, tak że nie wydaje się, że istnieje znacznik tam, gdzie żaden nie jest zamierzony, co zapobiega błędom kadrowania. Dekodery muszą pominąć ten bajt 0x00. Ta technika, zwana [wypychaniem bajtów](https://en.wikipedia.org/wiki/Byte_stuffing) (patrz specyfikacja JPEG, sekcja F.1.2.3), jest stosowana tylko do danych zakodowanych entropijnie, a nie do danych ładunku znaczników . Należy jednak zauważyć, że dane zakodowane entropijnie mają kilka własnych znaczników; w szczególności znaczniki resetowania (0xD0 do 0xD7), które są używane do izolowania niezależnych fragmentów danych zakodowanych entropijnie, aby umożliwić równoległe dekodowanie, a kodery mogą wstawiać te znaczniki resetowania w regularnych odstępach czasu (chociaż nie wszystkie kodery to robią).

