{
  "date" : "2019-12-13",
  "keywords" :["MP3", "plik", "rozszerzenie", "format", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Poznaj format plików MP3 i interfejsy API, które mogą otwierać i tworzyć pliki MP3.",
  "title" :"MP3 - Format Pliku Audio",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## Co to jest plik MP3?

Pliki z rozszerzeniem .mp3 to cyfrowo zakodowane formaty plików audio, które są formalnie oparte na standardzie MPEG-1 Audio Layer III lub MPEG-2 Audio Layer III. Został opracowany przez grupę Moving Picture Experts Group (MPEG), która wykorzystuje kompresję dźwięku warstwy 3. Kompresja osiągana przez format plików MP3 wynosi 1/10 rozmiaru plików .WAV lub .AIF. Format zapewnia zalety przesyłania strumieniowego takich plików audio przez Internet do słuchania online, co wcześniej nie było możliwe ze względu na duże rozmiary plików audio. Jakość dźwięku pliku audio MP3 można kontrolować za pomocą ustawień parametrów, takich jak szybkość transmisji, częstotliwość próbkowania, łączone lub normalne stereo.

## Krótka historia formatu plików MP3

Format MP3 został wynaleziony i opracowany przez niemiecką firmę Fraunhofer-Gesellshart. Algorytm posiada licencjonowane patenty na technologię kompresji, z której korzysta. Oto przydatna oś czasu MP3:

• **1987** — Instytut Fraunhofera w Niemczech rozpoczął badania nad wysokiej jakości kodowaniem audio o niskiej przepływności. Nazwano go projektem EUREKA EU147, Digital Audio Broadcasting.

• **Styczeń 1988** - Powstaje Moving Picture Experts Group (MPEG).

• **Kwiecień 1989** - Fraunhofer otrzymał w Niemczech patent na MP3.

• **1992** - Dieter Seitzer, który pomagał Fraunhoferowi w badaniach, zintegrował swoje kodowanie audio z MPEG-1.

• **1993** - Opublikowano standard MPEG-1.

• **1994** - Opracowano standard MPEG-2, który został opublikowany rok później.

• **listopad 26, 1996** - Wydano amerykański patent na MP3.

• **Wrzesień 1998** – Fraunhofer zaczął egzekwować prawa patentowe. Ktokolwiek użył kodowania audio MP3, zapłacił firmie Fraunhofer opłatę licencyjną.

• **Luty 1999** - SubPop, firma nagraniowa, jako pierwsza w historii dystrybuowała muzykę w formacie MP3.

• **1999** - Pojawiają się pierwsze przenośne odtwarzacze MP3.

## Format plików MP3

Plik MP3 składa się z ramek MP3, gdzie każda ramka składa się z nagłówka i bloku danych. Ramki nie są niezależne i zwykle nie można ich wyodrębnić z dowolnych granic ramek. Bloki danych pliku zawierają informacje o dźwięku w zakresie częstotliwości i amplitud. Słowo synchronizacji w nagłówku identyfikuje początek prawidłowej ramki. Następnie następują 3 bity, gdzie pierwszy bit wskazuje, że jest to standard MPEG, a pozostałe 2 bity wskazują, że używana jest warstwa 3; stąd MPEG-1 Audio Layer 3 lub MP3. Następnie wartości będą się różnić w zależności od pliku MP3.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 definiuje zakres wartości dla każdej sekcji nagłówek wraz ze specyfikacją nagłówka. Większość dzisiejszych plików MP3 zawiera [ID3](https://en.wikipedia.org/wiki/ID3) [metadane](https://en.wikipedia.org/wiki/Metadata), które poprzedzają lub następują po ramkach MP3, jak zaznaczono na schemacie. Strumień danych może zawierać opcjonalną sumę kontrolną.

## Bibliografia ##

* [MP3 – z Wikipedii](https://en.wikipedia.org/wiki/MP3)

