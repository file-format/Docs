{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Dowiedz się o formacie pliku Age of Empires 2 Expansion Replay MGX i interfejsach API, które umożliwiają tworzenie i otwieranie plików MGX.",
  "title" : "Plik MII — format pliku wirtualnego awatara Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-pl",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Czym jest plik MII?

Plik MII to format pliku wirtualnego awatara używany do przechowywania wirtualnych awatarów na konsoli do gier Nintendo Wii. Pliki te zawierają informacje, takie jak wygląd, ruchy i animacje awatara. Można ich używać w grach, aplikacjach społecznościowych i innym oprogramowaniu na Wii. Plik MII zawiera także inne cechy awatara, takie jak płeć, kolor włosów, kolor skóry, rysy twarzy i typ oczu.

Możesz otworzyć plik MII za pomocą [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Format pliku MII

Format pliku MII jest szczegółowo zdefiniowany w [Wii Brew](https://wiibrew.org/wiki/Mii_data). Ciągi znaków w pliku MII są przechowywane w formacie Unicode (UTF-16), big-endian.

### Blok MI

Dane pliku MII są przechowywane na Wiimote w dwóch blokach. Każdy blok ma długość 750 bajtów i 2 bajty CRC, co daje w sumie 752 bajty. Każdy blok zaczyna się od 4-bajtowej wartości (RNCD”), która wydaje się być magiczną liczbą dla formatu pliku MII.

## Jak utworzyć pliki MII?

Istnieje kilka różnych sposobów tworzenia awatarów dla konsoli Nintendo Wii:

1. `Korzystanie z wbudowanego kanału Mii na Wii:` Ten kanał umożliwia tworzenie niestandardowych awatarów przy użyciu różnych narzędzi, w tym rysów twarzy, kształtu ciała i ubioru. Po utworzeniu awatara możesz zapisać go jako plik Mii i używać go w grach i innym oprogramowaniu na Wii.

1. `Korzystanie z aplikacji Mii Maker na Nintendo 3DS:` Aplikacja Mii Maker umożliwia tworzenie niestandardowych awatarów za pomocą ekranu dotykowego i aparatu na Nintendo 3DS. Po utworzeniu awatara możesz zapisać go jako plik Mii i przesłać na Wii za pośrednictwem połączenia bezprzewodowego.

1. `Korzystanie z oprogramowania innych firm:` Niektórzy programiści stworzyli oprogramowanie umożliwiające tworzenie niestandardowych awatarów dla Wii. To oprogramowanie jest zazwyczaj przeznaczone do użytku na komputerze i może wymagać dodatkowych kroków w celu przeniesienia awatara na Twoją Wii.

1. `Korzystanie z gotowych awatarów:` Niektóre gry i inne oprogramowanie na Wii mogą zawierać gotowe awatary, których możesz używać.

We wszystkich przypadkach musisz mieć konto Nintendo, aby utworzyć i zapisać swojego awatara na Wii.

## Bibliografia

* [Edytor mojego awatara](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


