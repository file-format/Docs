{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Dowiedz się o formacie pliku MCR i interfejsach API, które umożliwiają tworzenie i otwieranie plików MCR.",
  "title": "MCR — format pliku regionu Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-plr"
}
},
  "lastmod": "2022-12-14"
}

## Czym jest plik MCR?

Format pliku Minecraft MCR to format danych używany przez Minecraft do przechowywania fragmentów terenu świata Minecraft. Opiera się na formacie NBT (Named Binary Tag), który został opracowany przez twórców popularnego silnika gier typu open source, Minecraft Forge. Typ pliku MCR został wprowadzony na samym początku, a później został zastąpiony przez [MCA file format](/game/mca/).

## Format pliku MCR

Format pliku MCR składa się z serii nazwanych znaczników binarnych, z których każdy zawiera określony typ danych. Tag najwyższego poziomu to tag Poziom”, który zawiera wszystkie dane dotyczące pojedynczego poziomu gry. W tagu Level znajduje się kilka innych nazwanych tagów, które przechowują różne typy danych, np. tag Data”, który przechowuje informacje o świecie gry, oraz tagi Entities” i TileEntities”, które przechowują dane o odpowiednio obiekty gry i byty kafelków na świecie.

## Co znajduje się w formacie pliku MCR?

W formacie pliku Minecraft MCR region to obszar świata gry o wymiarach 32x32 bloków. Format MCR dzieli świat gry na regiony, aby efektywniej zarządzać danymi i umożliwić szybsze ładowanie i zapisywanie poziomów gry. Każdy region jest przechowywany w osobnym pliku, a format pliku MCR wykorzystuje system współrzędnych do określenia pozycji każdego regionu w świecie gry. Współrzędne regionu są określone przez współrzędne blokowe lewego dolnego rogu regionu. Na przykład region o współrzędnych (-1,0) będzie zlokalizowany o jeden region na lewo i zero regionów w dół od początku świata gry.

## Specyfikacje formatu pliku MCR

Specyfikacje formatu pliku MCR są publicznie dostępne. Specyfikacje formatu NBT, na którym oparty jest format MCR, są dostępne na stronie internetowej Minecraft Forge. Dodatkowo [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) zawiera również szczegółowe informacje na temat formatu pliku MCR, w tym jego struktury i różnych obsługiwanych typów danych.

### Skompresowane dane w plikach MCR

Format pliku Minecraft MCR obsługuje kompresję. Format pliku MCR opiera się na [NBT format](https://minecraft.fandom.com/wiki/NBT_format), który umożliwia przechowywanie danych w formie skompresowanej. Pomaga to zmniejszyć rozmiar plików MCR i usprawnić ich przesyłanie i przechowywanie. Jest to ważna cecha formatu pliku MCR, ponieważ umożliwia graczom udostępnianie innym dużych danych terenowych z gry Minecraft World.

## Bibliografia

* [Edytor świata Minecrafta](https://www.mcedit.net/)

* [O Minecrafcie](https://www.minecraft.net/)

* [Format pliku regionu](https://minecraft.fandom.com/wiki/Region_file_format)

* [Format NBT](https://minecraft.fandom.com/wiki/NBT_format)


