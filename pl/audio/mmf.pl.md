{
  "date" : "2021-08-09",
  "keywords" :["mmf", "plik", "rozszerzenie", "format", "audio", "smaf", "rozszerzenie mmf", "pliki mmf", "plik muzyki mobilnej", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Dowiedz się o formacie pliku MMF i interfejsach API, które mogą tworzyć i otwierać pliki MMF.",
  "title" :"MMF – mobilny format plików muzycznych",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Czym jest plik FMF?

MMF to rozszerzenie pliku skojarzone z plikiem SMAF. MMF to skrót od Mobile Music File, natomiast SMAF to skrót od Mobile Application Format z muzyką syntetyczną. Pliki MMF w smartfonie zawierają dzwonki systemowe, dźwięk, a także mogą zawierać grafikę i wyświetlacz tekstowy. MMF zawiera ponadto trzy rodzaje parametrów instrumentu, w tym FM, PCM i Stream PCM. Wymienione formaty plików są kompatybilne z platformą systemową Windows. Pliki MMF są klasyfikowane jako pliki danych. Zwykle Microsoft Mail obsługuje pliki MMF. Plik z rozszerzeniem MMF można skopiować na dowolne urządzenie mobilne lub platformę systemową.

Co więcej, pliki te mają znacznie mniejszy rozmiar w porównaniu ze standardowymi plikami w formacie MIDI. Pliki [WAV](/pl/audio/wav/) i [MID](/pl/audio/mid/) można konwertować do formatu MMF, który można następnie udostępniać i rozpowszechniać jako zawartość audio. Pliki te można odbierać pocztą elektroniczną bezpośrednio na telefony i komputery.


## Krótka historia formatu pliku MMF

Yamaha opracowała narzędzia SMAF w postaci plików dźwiękowych, dzięki którym smartfony mogą przechowywać większą liczbę unikalnych dzwonków. Yamaha wprowadziła SMAF wraz z produkcją swoich układów dźwiękowych MA-1, MA-2, MA-3, MA-5 i MA-7 LSI. Wszystkie te formaty stały się dość znane wśród telefonów komórkowych na rynku Azji Wschodniej na początku 2000 roku.

Na poziomie międzynarodowym format MMF został autoryzowany przez firmę Samsung. Za pomocą formatu MMF Samsung był w stanie zaprojektować szeroką gamę dzwonków polifonicznych do wykorzystania w smartfonach Samsung.

Yamaha chciała uczynić format jeszcze bardziej popularnym, dlatego w oficjalnych plikach Yamaha SMAF opublikowała więcej narzędzi kompatybilnych z tym formatem. Dzięki temu użytkownicy mogą teraz łatwo odtwarzać pliki MMF na swoich komputerach.


## Specyfikacje formatu pliku MMF ##

Pliki MMF są podzielone na sekcje danych. Do opisu każdego segmentu używana jest struktura z prefiksem wokół 8-bajtów.
4-bajtowa etykieta zawiera CNTI, OPDA, MSTR, MTR i ATR. Rozmiar danych plus 8 bajtów to rozmiar porcji; cały rozmiar pliku jest obliczany przez zsumowanie wszystkich rozmiarów porcji. Jeśli plik nie został uszkodzony, zsumowany rozmiar pliku powinien być taki sam jak rozmiar nagłówka podstawowego.

### Nagłówek ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Oto przykład pliku MMF:

![](../mmf.png)

## Bibliografia

* [MMF – z Wikipedii](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

