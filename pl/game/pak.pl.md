{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "format pliku", "co to jest plik pak", "plik", "przykład pak", "Plik pakietu gier wideo", "rozszerzenie"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj plik .pak i interfejsy API, które mogą tworzyć i otwierać pliki PAK.",
  "title" :"Format pliku PAK — plik pakietu gier wideo",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Czym jest plik PAK?

Plik PAK to plik pakietu utworzony przez różne gry wideo w celu archiwizacji danych gry. Zasadniczo jest to format pliku gry. Może to obejmować wiele elementów gry, takich jak grafika, tekstury, dźwięki, obiekty, a także inne dane gry. Archiwum jest w większości zapisywane jako plik .zip i można je rozpakować za pomocą popularnego oprogramowania do dekompresji, takiego jak WinZip i WinRAR. Przykłady gier wideo korzystających z plików PAK to Quake, Hexen, Crysis i Half-Life.

## Format pliku PAK — więcej informacji

W większości przypadków pliki PAK są zapisywane w [formacie pliku ZIP](/pl/compression/zip/). Ale różne aplikacje mogą używać różnych formatów plików do przechowywania tych plików.


## Jak otworzyć pliki PAK?

Możesz otwierać pliki PAK za pomocą aplikacji takich jak [PakExplorer](https://www.quaketerminus.com/tools.shtml) i [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- --------**

## Format pliku PAK — plik obiektu Simutrans

Plik z rozszerzeniem .pak to plik gry symulacyjnej transportu [Simutrans](https://www.simutrans.com/en/). Zawiera obiekty wykorzystywane w symulacji, takie jak wykonane przez użytkownika grafiki i zawartość danych. Może mieć kilka różnych obiektów, takich jak pojazdy do gry, budynki, teren itp. Pliki PAK są generowane za pomocą MakeObject, narzędzia, które kompiluje pliki .dat i obrazy .png w celu tworzenia tych obiektów symulacyjnych. Simutrans pozwala graczom na prowadzenie skutecznego systemu transportowego poprzez konstruowanie i zarządzanie systemami transportowymi dla pasażerów, poczty i towarów drogą lądową

## Jak tworzyć pliki PAK?

Simutrans wymienił przykładowe przykłady tworzenia plików PAK w systemach Windows i Linux.

### System operacyjny Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Bibliografia

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)
